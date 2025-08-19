# Urlaub & Anwesenheitssimulation – Blueprint

## Übersicht
Diese Blueprint simuliert Anwesenheit während Abwesenheit oder Urlaub.  
Sie steuert Jalousien und Lichter zu zufälligen Zeiten innerhalb von Zeitfenstern und kann optional auf Wetter reagieren.  
Zusätzlich können Benachrichtigungen (z. B. via Telegram) versendet werden.

## Funktionen
- **Morgenroutine:**  
  - Öffnet ausgewählte Jalousien morgens in einem Zeitfenster (z. B. 07:00–07:30).  
  - Start wird zufällig innerhalb des Fensters gewählt.  
  - Zwischen einzelnen Jalousien kann eine Wartezeit konfiguriert werden.  

- **Abendroutine:**  
  - Schließt ausgewählte Jalousien abends in einem Zeitfenster (z. B. 20:00–21:00).  
  - Optional werden Lichter zufällig eingeschaltet (einzeln mit einstellbarer Wahrscheinlichkeit).  
  - Dauer pro Licht ist zufällig (innerhalb eines definierten Bereichs).  

- **Wetter-Logik (optional):**  
  - Prüft alle 15 Minuten, ob Helligkeit/Temperatur hoch genug ist.  
  - Schließt tagsüber ausgewählte Jalousien, um Aufheizen zu verhindern.  
  - Öffnet diese wieder, wenn Temperatur/Helligkeit sinkt oder die Sonne tief steht.  

- **Benachrichtigungen (optional):**  
  - Meldungen via `notify.*`-Service (z. B. Telegram-Gruppe).  
  - Info bei Morgen-/Abendaktionen sowie wetterbedingtem Schließen/Öffnen.  

## Einrichtung
1. Datei speichern unter:  
