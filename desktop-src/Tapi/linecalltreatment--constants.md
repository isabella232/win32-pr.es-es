---
description: Las \_ constantes LINECALLTREATMENT muestran los tratamientos de las llamadas que no tienen respuesta o están en espera. A excepción de la validación de parámetros básica, el tratamiento de llamadas es un paso directo por TAPI al proveedor de servicios.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Constantes de LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690922"
---
# <a name="linecalltreatment_-constants"></a><span data-ttu-id="ff576-104">Constantes de LINECALLTREATMENT \_</span><span class="sxs-lookup"><span data-stu-id="ff576-104">LINECALLTREATMENT\_ Constants</span></span>

<span data-ttu-id="ff576-105">Las **constantes \_ LINECALLTREATMENT** muestran los tratamientos de las llamadas que no tienen respuesta o están en espera.</span><span class="sxs-lookup"><span data-stu-id="ff576-105">The **LINECALLTREATMENT\_** constants list treatments for calls that are unanswered or on hold.</span></span> <span data-ttu-id="ff576-106">A excepción de la validación de parámetros básica, el tratamiento de llamadas es un paso directo por TAPI al proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="ff576-106">Except for basic parameter validation, call treatment is a straight pass-through by TAPI to the service provider.</span></span>

<dl> <dt>

<span data-ttu-id="ff576-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="ff576-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff576-108">Cuando la llamada no está conectada activamente a un dispositivo (oferta o en suspensión), la parte escucha la señal de ocupación.</span><span class="sxs-lookup"><span data-stu-id="ff576-108">When the call is not actively connected to a device (offering or onhold), the party hears busy signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff576-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**\_música LINECALLTREATMENT**</span><span class="sxs-lookup"><span data-stu-id="ff576-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT\_MUSIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff576-110">Cuando la llamada no está conectada activamente a un dispositivo (oferta o en suspensión), la parte escucha la música.</span><span class="sxs-lookup"><span data-stu-id="ff576-110">When the call is not actively connected to a device (offering or onhold), the party hears music.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff576-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**\_timbre LINECALLTREATMENT**</span><span class="sxs-lookup"><span data-stu-id="ff576-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff576-112">Cuando la llamada no está conectada activamente a un dispositivo (oferta o en suspensión), la parte escucha el tono de timbre.</span><span class="sxs-lookup"><span data-stu-id="ff576-112">When the call is not actively connected to a device (offering or onhold), the party hears ringback tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff576-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**silencio de LINECALLTREATMENT \_**</span><span class="sxs-lookup"><span data-stu-id="ff576-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT\_SILENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff576-114">Cuando la llamada no está conectada activamente a un dispositivo (oferta o en suspensión), la parte escucha el silencio.</span><span class="sxs-lookup"><span data-stu-id="ff576-114">When the call is not actively connected to a device (offering or onhold), the party hears silence.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff576-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff576-115">Remarks</span></span>

<span data-ttu-id="ff576-116">El valor 0x00000000 está reservado para indicar que el proveedor de servicios no admite los tratamientos de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ff576-116">The value 0x00000000 is reserved to indicate that the service provider does not support call treatments.</span></span> <span data-ttu-id="ff576-117">Los valores del intervalo de 0x00000005 a 0x000000FF se reservan para una definición futura.</span><span class="sxs-lookup"><span data-stu-id="ff576-117">Values in the range 0x00000005 through 0x000000FF are reserved for future definition.</span></span> <span data-ttu-id="ff576-118">Los valores en el intervalo de 0x00000100 a 0xFFFFFFFF están reservados para la asignación por proveedores de servicios y pueden incluir la identificación de selecciones musicales o anuncios grabados específicos.</span><span class="sxs-lookup"><span data-stu-id="ff576-118">Values in the range 0x00000100 through 0xFFFFFFFF are reserved for assignment by service providers, and may include identification of specific musical selections or recorded announcements.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff576-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff576-119">Requirements</span></span>



| <span data-ttu-id="ff576-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff576-120">Requirement</span></span> | <span data-ttu-id="ff576-121">Value</span><span class="sxs-lookup"><span data-stu-id="ff576-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ff576-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ff576-122">TAPI version</span></span><br/> | <span data-ttu-id="ff576-123">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ff576-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ff576-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff576-124">Header</span></span><br/>       | <dl> <span data-ttu-id="ff576-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff576-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




