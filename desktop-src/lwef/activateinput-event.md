---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076241"
---
# <a name="activateinput-event"></a><span data-ttu-id="5d0fc-103">Evento ActivateInput</span><span class="sxs-lookup"><span data-stu-id="5d0fc-103">ActivateInput Event</span></span>

<span data-ttu-id="5d0fc-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d0fc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5d0fc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="5d0fc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5d0fc-106">Se produce cuando un cliente pasa a ser de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="5d0fc-106">Occurs when a client becomes input-active.</span></span>

</dd> <dt>

<span data-ttu-id="5d0fc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="5d0fc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5d0fc-108">**Sub** *Agent* \_ ActivateInput **(ByVal** \*CharacterID \*\* \* *)*</span><span class="sxs-lookup"><span data-stu-id="5d0fc-108">**Sub** *agent*\_ActivateInput **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="5d0fc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5d0fc-109">Part</span></span>          | <span data-ttu-id="5d0fc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d0fc-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5d0fc-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="5d0fc-111">*CharacterID*</span></span> | <span data-ttu-id="5d0fc-112">Devuelve el identificador del carácter a través del cual el cliente pasa a ser de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="5d0fc-112">Returns the ID of the character through which the client becomes input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5d0fc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d0fc-113">Remarks</span></span>

<span data-ttu-id="5d0fc-114">El cliente de entrada-activo recibe los eventos de entrada de mouse y voz proporcionados por el servidor.</span><span class="sxs-lookup"><span data-stu-id="5d0fc-114">The input-active client receives mouse and speech input events supplied by the server.</span></span> <span data-ttu-id="5d0fc-115">El servidor envía este evento solo al cliente que pasa a ser de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="5d0fc-115">The server sends this event only to the client that becomes input-active.</span></span>

<span data-ttu-id="5d0fc-116">Este evento puede producirse cuando el usuario cambia al objeto de [comando](the-command-object.md) , por ejemplo, al elegir la entrada del objeto de comando en la ventana comandos o en el menú emergente de un carácter.</span><span class="sxs-lookup"><span data-stu-id="5d0fc-116">This event can occur when the user switches to your [Command](the-command-object.md) object, for example, by choosing your Command object entry in the Commands Window or in the pop-up menu for a character.</span></span> <span data-ttu-id="5d0fc-117">También se puede producir cuando el usuario selecciona un carácter (al hacer clic o hablar su nombre), cuando se hace visible un carácter y cuando se oculta el carácter de otra aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="5d0fc-117">It can also occur when the user selects a character (by clicking or speaking its name), when a character becomes visible, and when the character of another client application becomes hidden.</span></span> <span data-ttu-id="5d0fc-118">También puede llamar al [método Activate](activate-method.md) (con el **Estado** establecido en 2) para crear explícitamente el carácter más alto, lo que hace que la aplicación cliente se convierta en entrada-activa y desencadene este evento.</span><span class="sxs-lookup"><span data-stu-id="5d0fc-118">You can also call the [Activate Method](activate-method.md) (with **State** set to 2) to explicitly make the character topmost, which results in your client application becoming input-active and triggers this event.</span></span> <span data-ttu-id="5d0fc-119">Sin embargo, este evento no se produce si se usa el método activar método únicamente para especificar si el cliente es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="5d0fc-119">However, this event does not occur if you use the Activate Method method only to specify whether your client is the active client of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="5d0fc-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5d0fc-120">See Also</span></span>

<span data-ttu-id="5d0fc-121">[Evento **DeactivateInput**](deactivateinput-event.md), [método **Activate**](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="5d0fc-121">[**DeactivateInput** event](deactivateinput-event.md), [**Activate** method](activate-method.md)</span></span>


 

 




