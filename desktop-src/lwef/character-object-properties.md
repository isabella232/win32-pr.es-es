---
title: Propiedades del objeto character
description: Propiedades del objeto character
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c80e16bdb35d3fdfd8687eb15f200d2005ab75027e4dcc786f883d21232af4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610695"
---
# <a name="character-object-properties"></a>Propiedades del objeto character

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El [**objeto Character**](/windows/desktop/lwef/the-characters-object) expone las siguientes propiedades:

-   [**Activo**](active-property.md)
-   [**AutoPopupMenu**](autopopupmenu-property.md)
-   [**Descripción**](description-property.md)
-   [**ExtraData**](extradata-property.md)
-   [**Guid**](guid-property.md)
-   [**HasOtherClients**](hasotherclients-property.md)
-   [**Alto**](height-property.md)
-   [**HelpContextID**](helpcontextid-property-ch.md)
-   [**Helpfile**](helpfile-property.md)
-   [**HelpModeOn**](helpmodeon-property.md)
-   [**IdleOn**](idleon-property.md)
-   [**Languageid**](languageid-property.md)
-   [**Izquierda**](left-property.md)
-   [**MoveCause**](movecause-property.md)
-   [**Nombre**](name-property.md)
-   [**OriginalHeight**](originalheight-property.md)
-   [**OriginalWidth**](originalwidth-property.md)
-   [**Inclinación**](pitch-property.md)
-   [**SoundEffectsOn**](soundeffectson-property.md)
-   [**Velocidad**](speed-property.md)
-   [**SRModeID**](srmodeid-property.md)
-   [**SRStatus**](srstatus-property.md)
-   [**Arriba**](top-property.md)
-   [**TTSModeID**](ttsmodeid-property.md)
-   [**Versión**](version-property.md)
-   [**VisibilityCause**](visibilitycause-property.md)
-   [**Visible**](visible-property-cob.md)
-   [**Ancho**](width-property-co.md)

Tenga en cuenta que las propiedades [**Height**](height-property.md), [**Left**](left-property.md), [**Top**](top-property.md)y [**Width**](width-property-co.md) de un carácter difieren de las que puede ser compatible con el entorno de programación para la colocación del control. Las [**propiedades**](/windows/desktop/lwef/the-characters-object) Character se aplican a la presentación visible de un carácter, no a la ubicación del control Microsoft Agent.

Al igual que con [**los métodos**](/windows/desktop/lwef/the-characters-object) de objeto Character, puede acceder a las propiedades de un carácter mediante la colección [**Characters**](/windows/desktop/lwef/the-characters-object) o simplificar la sintaxis declarando una variable de objeto y estableciendo en un carácter de la colección. En el ejemplo siguiente, Test1 y Test2 se establecerán en el mismo valor:


```
   Dim Genie 
   Dim MyRequest
   
   Sub window_Onload

   Agent.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   Genie.MoveTo 15,15
   Set MyRequest = Genie.Show()

   End Sub

   Sub Agent_RequestComplete(ByVal Request)

   If Request = MyRequest Then 
      Test1 = Agent.Characters("Genie").Top
      Test2 = Genie.Top
      MsgBox "Test 1 is " + cstr(Test1) + "and Test 2 is " + cstr(Test2)
   End If

   End Sub
```



Dado que el servidor carga un carácter de forma asincrónica, asegúrese de que el carácter se ha cargado antes de consultar sus propiedades, por ejemplo, mediante el [**evento RequestComplete.**](requestcomplete-event.md) De lo contrario, las propiedades pueden devolver valores incorrectos.

 

 