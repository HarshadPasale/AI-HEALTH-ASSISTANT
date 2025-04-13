# AI-HEALTH-ASSISTANT
import streamlit as st

st.set_page_config(page_title="AI Health Assistant", page_icon="🩺")
st.title("🩺 AI Health Assistant")
st.write("Describe your symptoms to get basic health tips!")

user_input = st.text_area("Enter your symptoms:")

if st.button("Get Advice"):
    if user_input:
        with st.spinner("Thinking..."):
            # Dummy responses
            if "fever" in user_input.lower():
                reply = "It looks like you're experiencing fever. Stay hydrated, rest well, and monitor your temperature. Consult a doctor if it continues."
            elif "cough" in user_input.lower():
                reply = "For cough, try warm fluids and avoid cold drinks. If it lasts more than a few days, consider seeing a doctor."
            elif "headache" in user_input.lower():
                reply = "Headaches can be caused by stress or dehydration. Drink water and take a short break. If it persists, seek medical advice."
            else:
                reply = "Thank you for sharing your symptoms. It’s best to rest, drink plenty of fluids, and contact a medical professional if things don't improve."
            
            st.success(reply)
    else:
        st.warning("Please enter your symptoms first!")

st.markdown("---")
st.caption("⚠️ This is a demo app and not actual medical advice.")
