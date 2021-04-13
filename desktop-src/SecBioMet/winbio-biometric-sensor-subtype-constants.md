---
title: Constantes de WINBIO_BIOMETRIC_SENSOR_SUBTYPE (Winbio \_ Types. h)
description: Especifique una máscara de máscara para las capacidades del sensor incorporado.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422173"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a><span data-ttu-id="8dcb7-103">WINBIO \_ constantes de \_ subtipo del sensor biométrico \_</span><span class="sxs-lookup"><span data-stu-id="8dcb7-103">WINBIO\_BIOMETRIC\_SENSOR\_SUBTYPE Constants</span></span>

<span data-ttu-id="8dcb7-104">Las constantes siguientes se pueden usar como una máscara de máscara para el parámetro *Capabilities* de la estructura de esquema de la [**\_ unidad \_ WINBIO**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="8dcb7-104">The following constants can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="8dcb7-105">Estos se refieren a las capacidades del sensor incorporado.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-105">These refer to the onboard sensor capabilities.</span></span>



| <span data-ttu-id="8dcb7-106">Constante</span><span class="sxs-lookup"><span data-stu-id="8dcb7-106">Constant</span></span>                                                                                                                                                                                                            | <span data-ttu-id="8dcb7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8dcb7-107">Description</span></span>                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <span data-ttu-id="8dcb7-108"><dt>**subtipo de sensor de WINBIO \_ \_ \_ desconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="8dcb7-108"><dt>**WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN**</dt></span></span> </dl>     | <span data-ttu-id="8dcb7-109">No se conocen los subtipos de sensor.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-109">The sensor sub types is not known.</span></span><br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <span data-ttu-id="8dcb7-110"><dt>**WINBIO \_ de \_ subtipo de sensor FP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8dcb7-110"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE**</dt></span></span> </dl> | <span data-ttu-id="8dcb7-111">El sensor admite los deslizamientos de huella digital.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-111">The sensor supports fingerprint swipes.</span></span><br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <span data-ttu-id="8dcb7-112"><dt>**\_toque de \_ subtipo de sensor FP \_ \_ de WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="8dcb7-112"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH**</dt></span></span> </dl> | <span data-ttu-id="8dcb7-113">El sensor es compatible con los dedos.</span><span class="sxs-lookup"><span data-stu-id="8dcb7-113">The sensor supports finger touches.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="8dcb7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dcb7-114">Requirements</span></span>



| <span data-ttu-id="8dcb7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dcb7-115">Requirement</span></span> | <span data-ttu-id="8dcb7-116">Value</span><span class="sxs-lookup"><span data-stu-id="8dcb7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dcb7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8dcb7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8dcb7-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8dcb7-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="8dcb7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8dcb7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8dcb7-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8dcb7-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8dcb7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8dcb7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dcb7-122"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8dcb7-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dcb7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8dcb7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dcb7-124">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="8dcb7-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="8dcb7-125">**esquema de la \_ unidad WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="8dcb7-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





