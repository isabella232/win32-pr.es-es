---
title: Constantes de WINBIO_PROPERTY_TYPE (Winbio. h)
description: Especifique el origen de la información de la propiedad en la función WinBioGetProperty.
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4a1420af18bfa4d2ba5d0457b22cd5f77e7b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493144"
---
# <a name="winbio_property_type-constants"></a><span data-ttu-id="69a15-103">Constantes de tipo de \_ propiedad WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="69a15-103">WINBIO\_PROPERTY\_TYPE Constants</span></span>

<span data-ttu-id="69a15-104">Las constantes **de \_ \_ tipo de propiedad WINBIO** siguientes se pueden usar para especificar el origen de la información de la propiedad en la función [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) .</span><span class="sxs-lookup"><span data-stu-id="69a15-104">The following **WINBIO\_PROPERTY\_TYPE** constants can be used to specify the source of the property information in the [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) function.</span></span>

<dl> <dt>

<span data-ttu-id="69a15-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**\_sesión de \_ tipo de propiedad WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="69a15-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO\_PROPERTY\_TYPE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="69a15-106">La propiedad se aplica a una sesión biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="69a15-106">The property applies to a specific biometric session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69a15-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**\_plantilla de \_ tipo de propiedad WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="69a15-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO\_PROPERTY\_TYPE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="69a15-108">La propiedad se aplica a una plantilla biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="69a15-108">The property applies to a specific biometric template.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69a15-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**\_unidad de \_ tipo de propiedad WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="69a15-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO\_PROPERTY\_TYPE\_UNIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="69a15-110">La propiedad se aplica a una unidad biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="69a15-110">The property applies to a specific biometric unit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69a15-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**\_cuenta de \_ tipo de propiedad WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="69a15-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO\_PROPERTY\_TYPE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="69a15-112">La propiedad se aplica a una cuenta de usuario específica que tenga una inscripción biométrica.</span><span class="sxs-lookup"><span data-stu-id="69a15-112">The property applies to a specific user account that has a biometric enrollment.</span></span> <span data-ttu-id="69a15-113">Este valor se admite a partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="69a15-113">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69a15-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69a15-114">Requirements</span></span>



| <span data-ttu-id="69a15-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="69a15-115">Requirement</span></span> | <span data-ttu-id="69a15-116">Value</span><span class="sxs-lookup"><span data-stu-id="69a15-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a15-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69a15-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69a15-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="69a15-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="69a15-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69a15-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69a15-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="69a15-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="69a15-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69a15-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="69a15-122"><dt>Winbio. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69a15-122"><dt>Winbio.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69a15-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="69a15-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a15-124">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="69a15-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="69a15-125">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="69a15-125">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





