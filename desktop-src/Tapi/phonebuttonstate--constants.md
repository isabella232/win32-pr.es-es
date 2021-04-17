---
description: Las constantes de marcador de bits PHONEBUTTONSTATE describen las posiciones de los botones.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Constantes de PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691111"
---
# <a name="phonebuttonstate_-constants"></a><span data-ttu-id="fedf2-103">Constantes de PHONEBUTTONSTATE_</span><span class="sxs-lookup"><span data-stu-id="fedf2-103">PHONEBUTTONSTATE_ Constants</span></span>

<span data-ttu-id="fedf2-104">Las constantes de marcador de bits **PHONEBUTTONSTATE_** describen las posiciones del botón.</span><span class="sxs-lookup"><span data-stu-id="fedf2-104">The **PHONEBUTTONSTATE_** bit-flag constants describe the button's positions.</span></span>

<dl> <dt>

<span data-ttu-id="fedf2-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span><span class="sxs-lookup"><span data-stu-id="fedf2-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fedf2-106">El botón está en el estado "inactivo" (presionado).</span><span class="sxs-lookup"><span data-stu-id="fedf2-106">The button is in the "down" state (pressed down).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fedf2-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="fedf2-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fedf2-108">Indica que el proveedor de servicios no conoce el estado activo o inactivo del botón y que no se conocerá en el futuro.</span><span class="sxs-lookup"><span data-stu-id="fedf2-108">Indicates that the up or down state of the button is not known to the service provider, and will not become known at a future time.</span></span> <span data-ttu-id="fedf2-109">(Versiones de TAPI 1,4 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="fedf2-109">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fedf2-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="fedf2-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fedf2-111">Indica que en este momento no se conoce el estado arriba o abajo del botón, pero se puede conocer en el futuro.</span><span class="sxs-lookup"><span data-stu-id="fedf2-111">Indicates that the up or down state of the button is not known at this time, but may become known at a future time.</span></span> <span data-ttu-id="fedf2-112">(Versiones de TAPI 1,4 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="fedf2-112">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fedf2-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span><span class="sxs-lookup"><span data-stu-id="fedf2-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fedf2-114">El botón está en el estado "activo".</span><span class="sxs-lookup"><span data-stu-id="fedf2-114">The button is in the "up" state.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fedf2-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fedf2-115">Remarks</span></span>

<span data-ttu-id="fedf2-116">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="fedf2-116">No extensibility.</span></span> <span data-ttu-id="fedf2-117">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="fedf2-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="fedf2-118">Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en el teléfono y no utilizar los valores de PHONEBUTTONSTATE_ que la versión negociada no admite.</span><span class="sxs-lookup"><span data-stu-id="fedf2-118">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the phone, and to not use those PHONEBUTTONSTATE_ values that the negotiated version does not support.</span></span>

## <a name="requirements"></a><span data-ttu-id="fedf2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fedf2-119">Requirements</span></span>



| <span data-ttu-id="fedf2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fedf2-120">Requirement</span></span> | <span data-ttu-id="fedf2-121">Value</span><span class="sxs-lookup"><span data-stu-id="fedf2-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fedf2-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="fedf2-122">TAPI version</span></span><br/> | <span data-ttu-id="fedf2-123">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="fedf2-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fedf2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fedf2-124">Header</span></span><br/>       | <dl> <span data-ttu-id="fedf2-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fedf2-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




