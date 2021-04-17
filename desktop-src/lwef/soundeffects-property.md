---
title: Propiedad SoundEffects
description: Propiedad SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714159"
---
# <a name="soundeffects-property"></a><span data-ttu-id="53e18-103">Propiedad SoundEffects</span><span class="sxs-lookup"><span data-stu-id="53e18-103">SoundEffects Property</span></span>

<span data-ttu-id="53e18-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53e18-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="53e18-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="53e18-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="53e18-106">Devuelve un valor booleano que indica si los efectos de sonido (. WAV) los archivos configurados como parte de las acciones de un carácter se reproducirán.</span><span class="sxs-lookup"><span data-stu-id="53e18-106">Returns a Boolean indicating whether sound effects (.WAV) files configured as part of a character's actions will play.</span></span>

</dd> <dt>

<span data-ttu-id="53e18-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="53e18-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="53e18-108">*agente \* \* *. AudioOutput.SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="53e18-108">*agent\*\*\*.AudioOutput.SoundEffects*\*</span></span>



| <span data-ttu-id="53e18-109">Value</span><span class="sxs-lookup"><span data-stu-id="53e18-109">Value</span></span>     | <span data-ttu-id="53e18-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="53e18-110">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="53e18-111">**True**</span><span class="sxs-lookup"><span data-stu-id="53e18-111">**True**</span></span>  | <span data-ttu-id="53e18-112">Los efectos de sonido de carácter están habilitados.</span><span class="sxs-lookup"><span data-stu-id="53e18-112">Character sound effects are enabled.</span></span> |
| <span data-ttu-id="53e18-113">**False**</span><span class="sxs-lookup"><span data-stu-id="53e18-113">**False**</span></span> | <span data-ttu-id="53e18-114">El efecto de sonido de caracteres está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="53e18-114">Character sound effect are disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53e18-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53e18-115">Remarks</span></span>

<span data-ttu-id="53e18-116">Esta propiedad refleja la opción reproducir efectos sonoros de caracteres en la página salida de la hoja de propiedades del agente (opciones avanzadas de caracteres).</span><span class="sxs-lookup"><span data-stu-id="53e18-116">This property reflects the Play Character Sound Effects option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="53e18-117">Cuando la propiedad **SoundEffects** devuelve **true**, se reproducirán los efectos de sonido incluidos en la definición de un carácter.</span><span class="sxs-lookup"><span data-stu-id="53e18-117">When the **SoundEffects** property returns **True**, sound effects included in a character's definition will be played.</span></span> <span data-ttu-id="53e18-118">Si **es false**, los efectos sonoros no se reproducirán.</span><span class="sxs-lookup"><span data-stu-id="53e18-118">When **False**, the sound effects will not be played.</span></span> <span data-ttu-id="53e18-119">El valor de la propiedad afecta a todos los caracteres y es de solo lectura; solo el usuario puede establecer este valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="53e18-119">The property setting affects all characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="53e18-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53e18-120">See Also</span></span>

[<span data-ttu-id="53e18-121">**Evento AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="53e18-121">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




