---
title: Evento AgentPropertyChange
description: Evento AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075504"
---
# <a name="agentpropertychange-event"></a><span data-ttu-id="71acf-103">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="71acf-103">AgentPropertyChange Event</span></span>

<span data-ttu-id="71acf-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="71acf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="71acf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="71acf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="71acf-106">Se produce cuando el usuario cambia una propiedad en la ventana Opciones de carácter avanzadas.</span><span class="sxs-lookup"><span data-stu-id="71acf-106">Occurs when the user changes a property in the Advanced Character Options window.</span></span>

</dd> <dt>

<span data-ttu-id="71acf-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="71acf-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="71acf-108">**Sub** *Agent. \*\* \* \* AgentPropertyChange*</span><span class="sxs-lookup"><span data-stu-id="71acf-108">**Sub** *agent.\*\*\*AgentPropertyChange*\*</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="71acf-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71acf-109">Remarks</span></span>

<span data-ttu-id="71acf-110">Este evento indica que el usuario ha cambiado y aplicado cualquier propiedad incluida en la ventana opción de carácter avanzado.</span><span class="sxs-lookup"><span data-stu-id="71acf-110">This event indicates when the user has changed and applied any property included in the Advanced Character Option window.</span></span>

<span data-ttu-id="71acf-111">En el código para controlar este evento, puede consultar los valores de propiedad específicos de los objetos [AudioOutput](the-audiooutput-object.md) o [SpeechInput](the-speechinput-object.md) .</span><span class="sxs-lookup"><span data-stu-id="71acf-111">In your code for this handling this event, you can query for the specific property settings of [AudioOutput](the-audiooutput-object.md) or [SpeechInput](the-speechinput-object.md) objects.</span></span>

### <a name="see-also"></a><span data-ttu-id="71acf-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="71acf-112">See Also</span></span>

[<span data-ttu-id="71acf-113">**Evento DefaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="71acf-113">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




