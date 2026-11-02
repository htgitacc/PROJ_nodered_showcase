# Node-RED portfigyelő

Üzemben tartott gépek figyelése **Node-RED 4** és **FlowFuse Dashboard 2.0** felületen: melyik port hallgat, melyik folyamathoz tartozik, és hogyan áll a gép.

A nyers socketlista helyett a dashboard kategóriát és aktivitást mutat. Egy Windows hub gyűjt helyben, egy Ubuntu agent körülbelül félpercenként küldi a távoli gép állapotát.

Ez a **helyi** párja a szerveren futó Node-RED port-figyelőnek. A szerveres példány nem nyilvános, ezért nincs rá link; a portfólióban a két projekt egy kártyán szerepel.

## Felület

- **Listeners** — helyi és távoli LISTEN portok, a fejlesztői eszközök kiemelve. A Caddy site-ok kártyán: a mögöttes port, a helyi HTTPS válasz (5xx sárga) és a tanúsítvány lejárata.
- **Cron** — megnevezett ütemezett feladatok kártyán. A szín a legutóbbi siker ideje, nem az, hogy a cron démon fut.
- **Host metrics** — a távoli gép memóriája, terhelése és hálózata. 1, 6 és 24 óra nyers minta, 7 nap 10 perces átlag.

## Hogyan áll össze

A mintavétel Node.js programban fut, a flow ütemezi és megjeleníti. A grafikonok a hubon gyűlnek. A távoli agent a pillanatképet küldi, az idősort a hub tartja.

## Képernyőképek

A felület képei ide kerülnek.
