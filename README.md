# OMEN Alpha: Stavíme vlastní počítač

_Samozřejmě osmibitový a s tak historickým duchem, jak to jen jde._

[![I sell on Tindie](https://d2ss6ovg47m0r5.cloudfront.net/badges/tindie-larges.png)](https://www.tindie.com/stores/parallaxis/?ref=offsite_badges&utm_source=sellers_parallaxis&utm_medium=badges&utm_campaign=badge_large)

- [Essential ICs on AliExpress](https://alitronik.com/omen-alpha-pack/)
- [Essential ICs on eBay](https://alitronik.com/omen-alpha-pack-ebay/)

[BOM - Seznam součástek](./BOM.md)


Když jsem přemýšlel o tom, jak pojmout svou další knihy, bylo mi jasné, že suchý výklad nebude stačit. Tedy, on by stačil, ale já nejsem zrovna příznivcem teoretických učebnic bez přesahu do praxe. Bylo tedy samozřejmé, že nějakou konstrukci chci.

Ano, můžu vzít nějaký reálný osmibit a ukazovat na něm, jak se věci mají, možná vás i ponouknout ke stavbě repliky, ale touto cestou se mi moc jít nechtělo. Říkám si, že na vlastní konstrukci, která bude tak jednoduchá, jak jen to lze, půjde ilustrovat požadované věci mnohem líp.

Zvolil jsem tedy cestu konstrukce naprosto jednoduchých počítačů, které mají splňovat několik bodů:

1. Budou používat součástky, které se dají běžně koupit.
2. Nebudou se ortodoxně držet konstrukcí z 80. let - tedy když chci použít paměť, použiju moderní 128x8bit statickou RAM, což je jeden čip, a nebudu konstruovat zapojení z osmi čipů dynamické RAM a dalších tří IO kolem dokola.
3. Budou v duchu starých osmibitových časů, tedy jednoduché periferie - klávesnice, displej, reproduktor - a minimální softwarové vybavení.
4. Bude jednoduché psát pro ně software.
5. Klidně vynechám samotný starý procesor a potřebné funkce si naemuluju v moderním jednočipu. Nebo použiju jednočip místo periferií. No stress.

A maje tyto body na paměti jsem sednul a připravil několik konstrukcí, které jsou vhodné pro začátečníky - a tak vznikla "značka OMEN".

## OMEN?

Nojo. _Osmibitový Mikropočítač pro Elektronické Nadšence_. OMEN. A značení pomocí hláskového kódu: Alpha, Bravo, Charlie, Delta...

**OMEN Alpha** je jednoduchý počítač ve stylu jednodeskových strojů z konce 70. let s procesorem 8085. Obsahuje jen to nezbytné minimum, ovládáte jej pomocí terminálu, nebo pomocí připojené hexadecimální klávesnice a sedmisegmentového displeje.

