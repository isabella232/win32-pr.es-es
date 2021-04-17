---
title: Método STOP (características heredadas del entorno de Windows)
description: Stop (Método)
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705107"
---
# <a name="stop-method-legacy-windows-environment-features"></a><span data-ttu-id="b76b1-103">Método STOP (características heredadas del entorno de Windows)</span><span class="sxs-lookup"><span data-stu-id="b76b1-103">Stop Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="b76b1-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b76b1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b76b1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="b76b1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b76b1-106">Detiene la animación para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="b76b1-106">Stops the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="b76b1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="b76b1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b76b1-108">\*agente \***. Caracteres ("**_CharacterID_\*_"). Detener_ \*  \[ *solicitud*\]</span><span class="sxs-lookup"><span data-stu-id="b76b1-108">*agent\***.Characters ("**_CharacterID_*_").Stop_\* \[*Request*\]</span></span>



| <span data-ttu-id="b76b1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b76b1-109">Part</span></span>      | <span data-ttu-id="b76b1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b76b1-110">Description</span></span>                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b76b1-111">*Solicitud*</span><span class="sxs-lookup"><span data-stu-id="b76b1-111">*Request*</span></span> | <span data-ttu-id="b76b1-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b76b1-112">Optional.</span></span> <span data-ttu-id="b76b1-113">Objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) que especifica una llamada de animación determinada.</span><span class="sxs-lookup"><span data-stu-id="b76b1-113">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b76b1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b76b1-114">Remarks</span></span>

<span data-ttu-id="b76b1-115">Para especificar el parámetro de solicitud, debe crear una variable y asignar la solicitud de animación que desea detener.</span><span class="sxs-lookup"><span data-stu-id="b76b1-115">To specify the request parameter, you must create a variable and assign the animation request you want to stop.</span></span> <span data-ttu-id="b76b1-116">Si no establece el parámetro de **solicitud** , el servidor detiene todas las animaciones para el carácter, incluidas las llamadas [**Get**](get-method.md) en cola, y borra su cola de animación a menos que el carácter esté reproduciendo actualmente la animación que se **oculta** o se **muestra** .</span><span class="sxs-lookup"><span data-stu-id="b76b1-116">If you don't set the **Request** parameter, the server stops all animations for the character, including queued [**Get**](get-method.md) calls, and clears its animation queue unless the character is currently playing its **Hiding** or **Showing** animation.</span></span> <span data-ttu-id="b76b1-117">Este método no detiene las llamadas **Get** que no estén en cola.</span><span class="sxs-lookup"><span data-stu-id="b76b1-117">This method does not stop non-queued **Get** calls.</span></span>

<span data-ttu-id="b76b1-118">Para detener una animación concreta o una llamada [**Get**](get-method.md) , declare una variable de objeto y asigne la solicitud de animación a esa variable:</span><span class="sxs-lookup"><span data-stu-id="b76b1-118">To stop a specific animation or [**Get**](get-method.md) call, declare an object variable and assign your animation request to that variable:</span></span>


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



<span data-ttu-id="b76b1-119">Este método no generará un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="b76b1-119">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="b76b1-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b76b1-120">See Also</span></span>

[<span data-ttu-id="b76b1-121">**StopAll (método)**</span><span class="sxs-lookup"><span data-stu-id="b76b1-121">**StopAll method**</span></span>](stopall-method.md)


 

 
