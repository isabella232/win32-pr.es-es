---
title: Wait (Método)
description: Wait (Método)
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81949957146756e989fcb577a1bdd5a0c9a2a6fd60932220e39950327ba3061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715715"
---
# <a name="wait-method"></a>Wait (Método)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Hace que la cola de animación del carácter especificado espere hasta que se complete la solicitud de animación especificada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Solicitud de_ * _espera_



| Parte      | Descripción                                                                     |
|-----------|---------------------------------------------------------------------------------|
| *Solicitud* | Objeto [**Request**](/windows/desktop/lwef/the-request-object) que especifica una animación determinada. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use este método solo cuando admita varios caracteres (simultáneos) y esté intentando secuenciar la interacción de caracteres. (Para un solo carácter, cada solicitud de animación se reproduce secuencialmente, una vez completada la solicitud anterior). Si tiene dos caracteres y desea que la solicitud de animación de un carácter espere hasta que se complete la animación del otro carácter, establezca el método **Wait** en el objeto Request de animación del [**otro**](/windows/desktop/lwef/the-request-object) carácter. Para especificar el parámetro de solicitud, debe crear una variable y asignar la solicitud de animación que desea interrumpir:


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



Esto evita tener que declarar explícitamente un [**objeto Request.**](/windows/desktop/lwef/the-request-object)

 

 