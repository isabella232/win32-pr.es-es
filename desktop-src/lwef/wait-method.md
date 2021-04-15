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
# <a name="wait-method"></a><span data-ttu-id="a31e9-103">Wait (Método)</span><span class="sxs-lookup"><span data-stu-id="a31e9-103">Wait Method</span></span>

<span data-ttu-id="a31e9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a31e9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a31e9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="a31e9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a31e9-106">Hace que la cola de animación del carácter especificado espere hasta que se complete la solicitud de animación especificada.</span><span class="sxs-lookup"><span data-stu-id="a31e9-106">Causes the animation queue for the specified character to wait until the specified animation request completes.</span></span>

</dd> <dt>

<span data-ttu-id="a31e9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="a31e9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a31e9-108">*agente ***. Caracteres ("*** CharacterID ***").*** Solicitud de espera*</span><span class="sxs-lookup"><span data-stu-id="a31e9-108">*agent ***.Characters ("*** CharacterID ***").Wait*** Request*</span></span>



| <span data-ttu-id="a31e9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a31e9-109">Part</span></span>      | <span data-ttu-id="a31e9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a31e9-110">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a31e9-111">*Solicitud*</span><span class="sxs-lookup"><span data-stu-id="a31e9-111">*Request*</span></span> | <span data-ttu-id="a31e9-112">Objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) que especifica una animación determinada.</span><span class="sxs-lookup"><span data-stu-id="a31e9-112">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation..</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a31e9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a31e9-113">Remarks</span></span>

<span data-ttu-id="a31e9-114">Use este método solo cuando admita varios caracteres (simultáneos) y esté intentando secuenciar la interacción de los caracteres.</span><span class="sxs-lookup"><span data-stu-id="a31e9-114">Use this method only when you support multiple (simultaneous) characters and are trying to sequence the interaction of characters.</span></span> <span data-ttu-id="a31e9-115">(Para un solo carácter, cada solicitud de animación se reproduce secuencialmente, una vez completada la solicitud anterior). Si tiene dos caracteres y desea que la solicitud de animación de un carácter espere hasta que se complete la animación de otro carácter, establezca el método **Wait** en el objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) de animación del otro carácter.</span><span class="sxs-lookup"><span data-stu-id="a31e9-115">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and you want a character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="a31e9-116">Para especificar el parámetro de solicitud, debe crear una variable y asignar la solicitud de animación que desea interrumpir:</span><span class="sxs-lookup"><span data-stu-id="a31e9-116">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


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



<span data-ttu-id="a31e9-117">También puede simplificar el código simplemente llamando a **Wait** directamente, mediante una solicitud de animación específica.</span><span class="sxs-lookup"><span data-stu-id="a31e9-117">You can also streamline your code by just calling **Wait** directly, using a specific animation request.</span></span>


```
   Robby.Wait Genie.Play "GestureRight"
```



<span data-ttu-id="a31e9-118">Esto evita tener que declarar explícitamente un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="a31e9-118">This avoids having to explicitly declare a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 