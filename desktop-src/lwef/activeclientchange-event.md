---
title: Evento ActiveClientChange
description: Evento ActiveClientChange
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268770"
---
# <a name="activeclientchange-event"></a><span data-ttu-id="e9122-103">Evento ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="e9122-103">ActiveClientChange Event</span></span>

<span data-ttu-id="e9122-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9122-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e9122-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="e9122-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e9122-106">Se produce cuando cambia el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="e9122-106">Occurs when the active client of the character changes.</span></span>

</dd> <dt>

<span data-ttu-id="e9122-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="e9122-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e9122-108"> *Subagente.* ActiveClientChange (ByVal *CharacterID*, ByVal *activo* **)**</span><span class="sxs-lookup"><span data-stu-id="e9122-108">**Sub** *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**</span></span>



| <span data-ttu-id="e9122-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e9122-109">Part</span></span>          | <span data-ttu-id="e9122-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9122-110">Description</span></span>                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9122-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="e9122-111">*CharacterID*</span></span> | <span data-ttu-id="e9122-112">Devuelve el identificador del carácter para el que se produjo el evento.</span><span class="sxs-lookup"><span data-stu-id="e9122-112">Returns the ID of the character for which the event occurred.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="e9122-113">*Activo*</span><span class="sxs-lookup"><span data-stu-id="e9122-113">*Active*</span></span>      | <span data-ttu-id="e9122-114">Valor booleano que indica si el cliente se ha convertido en activo o no activo.</span><span class="sxs-lookup"><span data-stu-id="e9122-114">A Boolean value that indicates whether the client became active or not active.</span></span> <span data-ttu-id="e9122-115">**True** La aplicación cliente se convierte en el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="e9122-115">**True** The client application became the active client of the character.</span></span> <br/> <span data-ttu-id="e9122-116">**False** La aplicación cliente ya no es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="e9122-116">**False** The client application is no longer the active client of the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="e9122-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9122-117">Remarks</span></span>

<span data-ttu-id="e9122-118">Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="e9122-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="e9122-119">Del mismo modo, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente de entrada-activo) recibe eventos de [comando](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="e9122-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [Command](command-event.md) events.</span></span>

<span data-ttu-id="e9122-120">Cuando el cliente activo de un carácter cambia, este evento devuelve el identificador de ese carácter y **es true** si la aplicación se convierte en el cliente activo del carácter o en **false** si ya no es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="e9122-120">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="e9122-121">Una aplicación cliente puede recibir este evento cuando el usuario selecciona la entrada de una aplicación cliente en el menú emergente del carácter o mediante el comando de voz, cuando la aplicación cliente cambia su estado activo o cuando otra aplicación cliente cierra su conexión con el agente.</span><span class="sxs-lookup"><span data-stu-id="e9122-121">A client application may receive this event when the user selects a client application's entry in character's pop-up menu or by voice command, when the client application changes its active status, or when another client application quits its connection to Agent.</span></span> <span data-ttu-id="e9122-122">El agente envía este evento solo a las aplicaciones cliente que se ven afectadas directamente; Esto se convierte en el cliente activo o se detiene en el cliente activo.</span><span class="sxs-lookup"><span data-stu-id="e9122-122">Agent sends this event only to the client applications that are directly affected; that either become the active client or stop being the active client.</span></span>

### <a name="see-also"></a><span data-ttu-id="e9122-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e9122-123">See Also</span></span>

<span data-ttu-id="e9122-124">[\* \* \* \* ActivateInput \* \* Event \*](activateinput-event.md)\*, [\* \* \* \* Active \* \* Property \* \*](active-property.md), \* \* \* \* [DeactivateInput \* \* Event \* \*](deactivateinput-event.md), [\* \* \* \* Activate \* \* Method \* \*](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="e9122-124">[\*\*\*\*ActivateInput\*\* event\*\*](activateinput-event.md), [\*\*\*\*Active\*\* property\*\*](active-property.md), [\*\*\*\*DeactivateInput\*\* event\*\*](deactivateinput-event.md), [\*\*\*\*Activate\*\* method\*\*](activate-method.md)</span></span>


 

 





