# Personal Safe

# Project Abstract

“Personal Safe” password manager will be developed as a lightweight application to securely store and manage passwords. It will allow users to create a master account, then add, retrieve, and organize all their login credentials, which will all be encrypted and decrypted locally on their own personal device. There are plenty of password managers like LastPass and 1Password, but unlike “Personal Safe”, many of them rely on cloud storage which introduces risks if their servers are compromised. This project is different because all encryption happens on the client side, meaning data never leaves the user’s device in a plain form. The intended users are everyday people who want better security or people who are just serious about their privacy. Ultimately, this project will provide a security tool for users wanting to protect their passwords.

# Conceptual Design

The initial design concept for “Personal Safe” is a client-side password manager created with Python 3 using tkinter for GUI and JSON/AES encrypted local storage. It would run on multiple platforms including windows, macOS, and Linux. The initial design would ensure that any credentials would remain fully under the user’s control and balances security with ease of use. Some of the features would include a master account, adding/deleting credentials, a password generator, a strength meter, secure local storage, the ability to copy to clipboard, and optional encrypted import/export for backups.

https://uml.planttext.com/plantuml/png/TP71Ri8m38QV8EzWSM87n2l0IZLDOX8QWhkNc1AHnf7ZZbNJtdtfOQ9CvUB3__ss_Dkhh2ZQjS4OzHe83fcWmb8s7Xl1rfX09mLb4D-S5PmNikev6hJAClZ5c473s9J-sOuaSyG0UppH3BxDu8350kQL42h16sOjojfQxg8-tVYM6nzX2OSOs5xWY5sunnFYsZdOOSvN5WTrLEb7i7PU7zCD1Ihh_9UFdgxBT_ga4k6lTuGhJlrjPZbB5NpwOBmplL0a6R9E3JXJoJ41wg_4ecKVAtrISl2CzjAbaUErVU3uCMP5qPKt_W80

https://uml.planttext.com/plantuml/png/VPB1QiCm38QVmE_WOmBf2_GmEhOnTYWCIdij8XR1r75IIscRjv-SjCaSrbria3x_-YLvGmo1kzefnPOTwXsUE_GbwdSBLO1QAIYv2NfF65GyzEf5V-w_jk2Xmh3Mw5c2DL2yMY2wDi6ecOZyQzkkTUTTKvwoaVo-WxbIaepCJge8F-cw1aoMgpIiLmyryHZwbj5iaQZGDJ8OO9ZatcAscTGC1dl1umdxXO524pZELSBFPUPtpvK78yTQV6J25Qcrfygj0okZk_67vs2H9lq3T8x7_k-fRCdArFvQHOYx8zONYzT_Lr7XeDHdLXQGbarIGsos_9ZP08pl5WvIudTb0QDbcPSbQQUV_QaDUYC_y0S0

https://uml.planttext.com/plantuml/png/TLHTRjim33w1xw17UqqkO0n5XxOe2Yp0W25x3HYRTOJQaYVHwOnXTnz5oOcTf4yIF_7d8qNomHCu6hesoqXJY-gn1U_LauR6GPTbbOZV-bxzpPHQgoCCBPNgLpW4Q0PTgfVjwmOCDEW4gzpOaotLenl9pXyyMST2gNx6o_djJhd1v8NSMbkzf-jWHEZ04xeVJEN3khfaFwx8_atiX4pYXuQSHb-gxzhJrydYcT7nNXIqtmMNo5xsrhOI1UgeaJEpXKaauR2pHumQckssszUdHA-lWIvULkgsbmRfmiM5ccXv15STyjy3kZ7cUJkLK_8BF1LXYY22VAku4d7mw0nqCwIVbrKGOocKS189caI2aVlqmyY9iqd8dtI7WdQsrczw0Pzupdj1QDwf6fq-ukuTnriVl58UGgljHoPJf5Fiq4Y3xJhqFcVhzBPIVGlQ4FwPMJr7NQmth9oYVc8TW0k3KzXJ6il6JVNkWGxXC-aG_n2EcCkWRAvTXZW4N1_WAkcAffQ7EkTe-IUwisu_pregep_O3-xfHa_p8u34Jq3lRCSPXzaOTs_MTNbntK0lQD01fvVSDb76l4NJXFoujAlGFhkXxz75yOc07xkzRNs4YjWuiuevSR11EbEkhCDyqNY5193NDyHw3ppseYRusMbOHNQzJXieZluNbfUZD6dD5jC4BPRI15xiemc-gitCO9PLbZsWgNc9_WS0


# Background

“Personal Safe” will enable users to generate, store, and manage passwords securely, with any encryption and decryption performed locally on their device. This approach ensures that any sensitive data never leaves the device in plain text, while reducing risks from breaches of centralized servers. The main features will include a master account login, password storage and retrieval, a password generator, a strength meter, and an optional encrypted export for any backups.

While proprietary products like LastPass and 1Password are useful, they heavily rely on cloud storage, which can make them targets. Other open-source options like Bitwarden and KeePass provide flexibility, but they come with harder setups and even partially rely on external infrastructure. This project won't reuse any of their source code but it will likely need to borrow some design inspiration. Its main difference between those other products is the focus on full client-side encryption and user-controlled storage, which combines usability with even more protection.

https://www.lastpass.com/password-manager#:~:text=Cloud%2Dbased%20apps%20are%20password%20managers%20which%20store,include%20LastPass%2C%201Password%2C%20Nordpass%2C%20Dashlane%2C%20and%20others.

https://1password.com/?utm_source=google&utm_medium=cpc&utm_campaign=10693428634&utm_content=452812895249&utm_term=1password%20password%20manager&gclsrc=aw.ds&gad_source=1&gad_campaignid=10693428634&gbraid=0AAAAAD_PA5-J-g3PnHGa8_6FT2WxzPKry&gclid=CjwKCAjwlaTGBhANEiwAoRgXBQqp28Oib6dEir1f8TSqRLfgNMBTGBtzcvoPeK38JpCro1TvJ6fE5xoC4CEQAvD_BwE


# Proof of Concept

https://github.com/JLupold/personal-safe.git

# Required Resources

This password manager will be developed using Python 3, which I’m familiar with. I’ll also use the tkinter library to create a simple GUI for entering and viewing passwords, and the json and base64 libraries to store encrypted passwords locally. For encryption I’ll implement a XOR-based method for this prototype, but I’ll most likely be added stronger encryption later using the cryptography library if I need to. The project can be run on any computer without the need for special hardware, and any necessary Python libraries are either built-in or installed relatively easily.
