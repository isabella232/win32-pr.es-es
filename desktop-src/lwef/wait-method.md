---
title: Wait (Método)
description: Wait (Método)
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714351"
---
# <a name="wait-method"></a>Wait (Método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Hace que la cola de animación del carácter especificado espere hasta que se complete la solicitud de animación especificada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID ***").*** Solicitud de espera*



| Parte      | Descripción                                                                     |
|-----------|---------------------------------------------------------------------------------|
| *Solicitud* | Objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) que especifica una animación determinada. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use este método solo cuando admita varios caracteres (simultáneos) y esté intentando secuenciar la interacción de los caracteres. (Para un solo carácter, cada solicitud de animación se reproduce secuencialmente, una vez completada la solicitud anterior). Si tiene dos caracteres y desea que la solicitud de animación de un carácter espere hasta que se complete la animación de otro carácter, establezca el método **Wait** en el objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) de animación del otro carácter. Para especificar el parámetro de solicitud, debe crear una variable y asignar la solicitud de animación que desea interrumpir:


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



También puede simplificar el código simplemente llamando a **Wait** directamente, mediante una solicitud de animación específica.


```
   Robby.Wait Genie.Play "GestureRight"
```



Esto evita tener que declarar explícitamente un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .

 

 