# Performance Audit 

Dit is een Performance audit op de site van DOA, de dierenopvang van Amsterdam. 

[INSTRUCTIONS](https://github.com/fdnd-task/performance-audit/blob/main/docs/INSTRUCTIONS.md)
 

## DOA - Dierenopvang Amsterdam

Ik heb de site van DOA als eerste getest. De site is een home page voor het stichting, met informatie over vacatures, dieren die een huis zoeken, en statistieken over het stichting. Er zijn meerdere forms, links, en carousels, allemaal met hover states of scroll animaties.
![image](https://github.com/user-attachments/assets/cf11e6a6-88ce-40d4-a981-892141912909)
![Screenshot 2025-04-14 131000](https://github.com/user-attachments/assets/350300da-a269-4c39-81e2-2748ab02b5bb)
![Screenshot 2025-04-14 131015](https://github.com/user-attachments/assets/f7fe6ee6-9684-4a66-b988-3b76ce72f6ea)

## Performance test
*Lighthouse score op mobiel* 
![image](https://github.com/user-attachments/assets/ed76bcf9-3e89-477d-b12f-ca2ffc3853cb)

*Lighthouse score op desktop* 
![image](https://github.com/user-attachments/assets/a249bd82-9753-4454-ab48-129afad7a812)

*Core Web Vitals Assessment*

*PageSpeed Insights*
![image](https://github.com/user-attachments/assets/d1d4d25c-276f-42b6-80fc-861707e0ac5a)

*WebPageTest*
![image](https://github.com/user-attachments/assets/2e5d5044-9591-49dc-945d-27490b3bb62c)
![image](https://github.com/user-attachments/assets/1ef315f6-0d37-48e9-afbd-8bb8e18e091f)
![image](https://github.com/user-attachments/assets/1c288d23-1df4-47a6-abce-26439f67a0a7)

## Samenvatting
De testbevindingen zijn goed, behalve de Total Blocking Time. De javascript duurt ook lang om in te laden, vooral die van visualwebsiteoptimizer.com. Er is ook een image die veel later is ingeladen, van 2. doamsterdam.nl. 
Er is ook een hele grote CPU spike van de script parsing en layout setup van 29. ct.pinterest.com aan het einde van het laden van de pagina.
Zoals verwacht is de meest van de bandwidth gebruikt aan het begin van het renderen, met een spike bij het laden van de javascript van gstatic.com.
De browser Main Thread en Long Tasks zijn bijna hetzelfde, met een grote spike bij het laden van 14, 15, 16, 17, 18 en 19. Dit betekend dat de CPU misschien een block is voor het laden van de rest van de pagina.

