---
title: Métodos de objeto Character
description: Métodos de objeto Character
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c0fbcfe26e198984fd4a4d8c6c67858085e41178786d2cb78d2938231fdf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480319"
---
# <a name="character-object-methods"></a>Métodos de objeto Character

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El servidor también expone métodos para cada carácter de una [**colección Characters.**](/windows/desktop/lwef/the-characters-object) Se admiten los métodos siguientes:

-   [**Activar**](activate-method.md)
-   [**GestureAt**](gestureat-method.md)
-   [**Obtener**](get-method.md)
-   [**Ocultar**](hide-method.md)
-   [**Interrupción**](interrupt-method.md)
-   [**Escucha**](listen-method.md)
-   [**Moveto**](moveto-method.md)
-   [**Reproducir**](play-method.md)
-   [**Mostrar**](show-method.md)
-   [**ShowPopupMenu**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Stop**](stop-method.md)
-   [**Soundmixer.stopall**](stopall-method.md)
-   [**Pensar**](think-method.md)
-   [**Esperar**](wait-method.md)

Para usar un método, haga referencia al carácter de la colección. En VBScript y Visual Basic, para ello, especifique el identificador de un carácter:


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



Para simplificar la sintaxis del código, puede definir una variable de objeto y establecerla para que haga referencia a un objeto de carácter en la [**colección Characters.**](/windows/desktop/lwef/the-characters-object) a continuación, puede usar la variable para hacer referencia a métodos o propiedades del carácter. En el ejemplo siguiente se muestra cómo puede hacerlo mediante la instrucción Visual Basic Set:


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



En Visual Basic 5.0, también puede crear la referencia declarando la variable como un [**objeto Character:**](/windows/desktop/lwef/the-characters-object)


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



Declarar el objeto de tipo IAgentCtlCharacterEx habilita el enlace temprano en el objeto, lo que da como resultado un mejor rendimiento.

En VBScript, no se puede declarar una referencia como un tipo determinado. Sin embargo, simplemente puede declarar la referencia de variable:


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



Algunos lenguajes de programación no admiten colecciones. Sin embargo, puede acceder a [**los métodos**](/windows/desktop/lwef/the-characters-object) de un objeto Character con el [**método Character:**](character-method.md)


```
   agent.Characters.Character("CharacterID").method
```



Además, también puede crear una referencia al objeto [**Character**](/windows/desktop/lwef/the-characters-object) para que el código de script sea más fácil de seguir:


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 