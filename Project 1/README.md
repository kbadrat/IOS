# Úloha IOS (2021)
## Popis úlohy
Cílem úlohy je vytvořit skript pro analýzu záznamu systému pro obchodování na burze. Skript bude filtrovat záznamy a poskytovat statistiky podle zadání úživatele.

## Zjednodušený úvod do problematiky
Na burze se obchoduje s cennými papíry (např. akcie společností, dluhopisy), komoditami (např. ropa, zelí) apod. Každý obchodovaný artikl má jednoznačný identifikátor, tzv. ticker (např. akcie firmy Intel mají na burze NASDAQ ticker INTC, bitcoin může mít přiřazený ticker BTC). Cena artiklů se mění v čase. Obchodník na burze vstupuje do pozic, buď tak, že koupí artikl a očekává, že jeho cena poroste, aby jej pak prodal za vyšší cenu (tzv. dlouhá pozice), nebo že artikl prodá a očekává, že jeho cena klesne, aby jej poté mohl koupit levněji (tzv. krátká pozice). Obchodník může prodat i artikl, který právě nevlastní (v reálu to funguje tak, že si ho od někoho, kdo ho vlastní, “vypůjčí”, prodá jej, a potom ho koupí za nižší cenu a “vrátí”). V našem případě budeme uvažovat, že obchodníkův systém posílá na burzu příkazy k nákupu (buy) nebo prodeji (sell) určitého množství jednotek artiklu označeného nějakým tickerem.

