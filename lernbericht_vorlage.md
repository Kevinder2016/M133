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

## Verifikation

✍️ Erklären Sie kurz und bündig, inwiefern die von Ihnen verwendeten Medien zeigen, was Sie gelernt haben.

# Reflektion zum Arbeitsprozess

👍 Überlegen Sie sich jeweils etwas, was gut an Ihrer Arbeit lief; 

👎 und etwas, was nicht gut lief.

**VBV**: ✍️ Formulieren Sie davon ausgehend einen *handelbaren* Verbesserungsvorschlag.
