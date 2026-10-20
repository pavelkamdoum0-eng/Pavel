# :earth_americas: GDP dashboard template

A simple Streamlit app showing the GDP of different countries in the world.

[![Open in Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://gdp-dashboard-template.streamlit.app/)

### How to run it on your own machine

1. Install the requirements

   ```
   $ pip install -r requirements.txt
   ```

2. Run the app

   ```
   $ streamlit run streamlit_app.py
   ```
import streamlit as st

st.set_page_config(page_title="SAFE Bet Pavel")

st.title("⚽ SAFE Bet - Pavel")
st.success("App connectée ✅")

domicile = st.text_input("Equipe Domicile")
exterieur = st.text_input("Equipe Exterieur")
forme = st.slider("Victoires domicile sur 5 derniers", 0, 5, 4)

if st.button("ANALYSER SAFE"):
    if forme >= 3:
            st.success(f"✅ SAFE: {domicile} ne perd pas (1X)")
                    st.success("✅ SAFE: Plus de 1.5 buts")
                        else:
                                st.error("❌ Match risqué")