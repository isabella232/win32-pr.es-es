---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994350"
---
# <a name="deactivateinput-event"></a><span data-ttu-id="26e62-103">Evento DeactivateInput</span><span class="sxs-lookup"><span data-stu-id="26e62-103">DeactivateInput Event</span></span>

<span data-ttu-id="26e62-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="26e62-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="26e62-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="26e62-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="26e62-106">Se produce cuando un cliente deja de ser de entrada y no está activo.</span><span class="sxs-lookup"><span data-stu-id="26e62-106">Occurs when a client becomes non-input-active.</span></span>

</dd> <dt>

<span data-ttu-id="26e62-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="26e62-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="26e62-108">**Sub** *Agent \* \* \* \_ DeactivateInput* \*  **(ByVal** \*CharacterID \*\* \* *)*</span><span class="sxs-lookup"><span data-stu-id="26e62-108">**Sub** *agent\*\*\*\_DeactivateInput*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="26e62-109">Parte</span><span class="sxs-lookup"><span data-stu-id="26e62-109">Part</span></span>          | <span data-ttu-id="26e62-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="26e62-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="26e62-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="26e62-111">*CharacterID*</span></span> | <span data-ttu-id="26e62-112">Devuelve el identificador del carácter que hace que el cliente se convierta en no de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="26e62-112">Returns the ID of the character that makes the client become non-input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="26e62-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26e62-113">Remarks</span></span>

<span data-ttu-id="26e62-114">Un cliente que no es de entrada-activo ya no recibe eventos de mouse o de voz del servidor (a menos que vuelva a ser de entrada-activo).</span><span class="sxs-lookup"><span data-stu-id="26e62-114">A non-input-active client no longer receives mouse or speech events from the server (unless it becomes input-active again).</span></span> <span data-ttu-id="26e62-115">El servidor envía este evento solo al cliente que no es de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="26e62-115">The server sends this event only to the client that becomes non-input-active.</span></span>

<span data-ttu-id="26e62-116">Este evento se produce cuando la aplicación cliente es de entrada y el usuario elige el título de otro cliente en el menú emergente de un carácter o en la ventana comandos de voz, o bien se llama al método [**Activar**](activate-method.md) y se establece el parámetro de **Estado** en 0.</span><span class="sxs-lookup"><span data-stu-id="26e62-116">This event occurs when your client application is input-active and the user chooses the caption of another client in a character's pop-up menu or the Voice Commands Window or you call the [**Activate**](activate-method.md) method and set the **State** parameter to 0.</span></span> <span data-ttu-id="26e62-117">También se puede producir cuando el usuario selecciona el nombre de otro carácter haciendo clic o hablando.</span><span class="sxs-lookup"><span data-stu-id="26e62-117">It may also occur when the user selects the name of another character by clicking or speaking.</span></span> <span data-ttu-id="26e62-118">También recibirá este evento cuando el carácter esté oculto u otro carácter esté visible.</span><span class="sxs-lookup"><span data-stu-id="26e62-118">You also get this event when your character is hidden or another character becomes visible.</span></span>

### <a name="see-also"></a><span data-ttu-id="26e62-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="26e62-119">See Also</span></span>

[<span data-ttu-id="26e62-120">**Evento ActivateInput**</span><span class="sxs-lookup"><span data-stu-id="26e62-120">**ActivateInput event**</span></span>](activateinput-event.md)


 

 




