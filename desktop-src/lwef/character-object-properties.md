---
title: Propiedades del objeto de carácter
description: Propiedades del objeto de carácter
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6212d6f0539b7fcb29faa883e6d88101952c12f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420539"
---
# <a name="character-object-properties"></a>Propiedades del objeto de carácter

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) expone las siguientes propiedades:

-   [**Active**](active-property.md)
-   [**AutoPopupMenu**](autopopupmenu-property.md)
-   [**Descripción**](description-property.md)
-   [**ExtraData**](extradata-property.md)
-   [**VOLUMEN**](guid-property.md)
-   [**HasOtherClients**](hasotherclients-property.md)
-   [**Height**](height-property.md)
-   [**IDDelContextoDeAyuda**](helpcontextid-property-ch.md)
-   [**HelpFile**](helpfile-property.md)
-   [**HelpModeOn**](helpmodeon-property.md)
-   [**Inactivo**](idleon-property.md)
-   [**LanguageID**](languageid-property.md)
-   [**Salido**](left-property.md)
-   [**MoveCause**](movecause-property.md)
-   [**Name**](name-property.md)
-   [**Altooriginal**](originalheight-property.md)
-   [**Anchooriginal**](originalwidth-property.md)
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
-   [**Width**](width-property-co.md)

Tenga en cuenta que las propiedades [**altura**](height-property.md), [**izquierda**](left-property.md), [**superior**](top-property.md)y [**ancho**](width-property-co.md) de un carácter difieren de las que puede admitir el entorno de programación para la colocación del control. Las propiedades de [**caracteres**](/windows/desktop/lwef/the-characters-object) se aplican a la presentación visible de un carácter, no a la ubicación del control de Microsoft Agent.

Al igual que con los métodos de objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) , puede tener acceso a las propiedades de un carácter mediante la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) o simplificar la sintaxis declarando una variable de objeto y estableciéndolo en un carácter de la colección. En el ejemplo siguiente, test1 y test2 se establecerán en el mismo valor:


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



Dado que el servidor carga un carácter de forma asincrónica, asegúrese de que se ha cargado el carácter antes de consultar sus propiedades, por ejemplo, mediante el evento [**RequestComplete**](requestcomplete-event.md) . De lo contrario, las propiedades pueden devolver valores incorrectos.

 

 