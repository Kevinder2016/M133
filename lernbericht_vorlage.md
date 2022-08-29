# Lern-Bericht
von Kevin Frühwirth

## Einleitung

Es geht darum wie man die Session-ID mithilfe von JSF anzeigen kann.

## Was habe ich gelernt?

Ich habe gelernt wie man die SessionID mit Java code generiert und dann in JSF mit xhtml anzeigen kann.

## Beschreibung

```java
    public String getSessionID(){
    FacesContext fCtx = FacesContext.getCurrentInstance();
    HttpSession session = (HttpSession) fCtx.getExternalContext().getSession(false);
    return session.getId();    
    }
```

```xhtml
    <h:outputLabel value="Ihre Sitzung wurde eröffnet #{helloManagedBean.sessionID}"/> 
```

![image](https://user-images.githubusercontent.com/69578309/187229314-f7dde777-a861-4c99-8abc-4e4bf0834895.png)


## Verifikation

Der Screenshot zeigt das die Session ausgegeben wurde. Im java code sieht man wie die SessionID mit einer getter Funktion zurückgegeben wird, diese Information nutzt man dann im xhtml wo diese Funktion aufgerufen wird und die SessionID dann angezeigt wird.

# Reflektion zum Arbeitsprozess

👍 Die Arbeit an diesem Projekt ist sehr gut gelaufen, es war alles sehr Verständlich. Der Code für die SessionID Funktion die, die SessionID ausgibt war schon vorgegeben, was die Aufgabe nochmal vereinfachte. Man musste nurnoch den Code richtig implementieren und die getter Funktion im xhtml aufrufen.

👎 Ich war Anfangs kurz Verwirrt, weil ich nicht gemerkt habe das, das return statement im vorgegebene Code gefehlt hat.

**VBV**: Ich möchte mich bei der Fehlersuche in der Zukunft verbessern damit ich direkt erkennen kann was der Fehler ist, wie in diesem Fall das fehlende Return statement.
