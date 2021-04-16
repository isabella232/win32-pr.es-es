---
title: Identificadores de peso de filtro (Fwpmu. h)
description: Filtrar los identificadores de peso utilizados por el motor de filtrado de base (BFE) para calcular los pesos de los filtros generados automáticamente.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686150"
---
# <a name="filter-weight-identifiers"></a><span data-ttu-id="215e3-103">Identificadores de peso de filtro</span><span class="sxs-lookup"><span data-stu-id="215e3-103">Filter Weight Identifiers</span></span>

<span data-ttu-id="215e3-104">A continuación se enumeran los identificadores de peso de filtro utilizados por el motor de filtrado de base (BFE) para calcular los pesos de los filtros generados automáticamente.</span><span class="sxs-lookup"><span data-stu-id="215e3-104">The filter weight identifiers used by the Base Filtering Engine (BFE) to compute auto-generated filter weights are listed below.</span></span>

<span data-ttu-id="215e3-105">Vea [filtrar asignación de peso](filter-weight-assignment.md) para obtener más información sobre la generación de pesos del filtro.</span><span class="sxs-lookup"><span data-stu-id="215e3-105">See [Filter Weight Assignment](filter-weight-assignment.md) for more information on filter weight generation.</span></span>

<dl> <dt>

<span data-ttu-id="215e3-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM \_ \_ bits de ponderación automática \_**</span><span class="sxs-lookup"><span data-stu-id="215e3-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM\_AUTO\_WEIGHT\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="215e3-107">(60)</span><span class="sxs-lookup"><span data-stu-id="215e3-107">(60)</span></span>
</dt> <dt>



<span data-ttu-id="215e3-108">Número de bits usados para pesos de filtro generados automáticamente.</span><span class="sxs-lookup"><span data-stu-id="215e3-108">Number of bits used for auto-generated filter weights.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="215e3-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM \_ de \_ peso automático \_ máximo**</span><span class="sxs-lookup"><span data-stu-id="215e3-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM\_AUTO\_WEIGHT\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="215e3-110">(**MAXUINT64** >> 4)</span><span class="sxs-lookup"><span data-stu-id="215e3-110">(**MAXUINT64** >> 4)</span></span>
</dt> <dt>



<span data-ttu-id="215e3-111">Peso máximo de filtro generado automáticamente.</span><span class="sxs-lookup"><span data-stu-id="215e3-111">Maximum auto-generated filter weight.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="215e3-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="215e3-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="215e3-113">0XC</span><span class="sxs-lookup"><span data-stu-id="215e3-113">(0xC)</span></span>
</dt> <dt>



<span data-ttu-id="215e3-114">BFE asigna un peso con este valor de intervalo a los filtros IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="215e3-114">BFE assigns a weight with this range value to IKE and AuthIP filters.</span></span>

<span data-ttu-id="215e3-115">Consulte [exenciones de IKE/AuthIP](ike-exemptions.md) para obtener más información sobre los filtros IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="215e3-115">See [IKE/AuthIP Exemptions](ike-exemptions.md) for more information on IKE/AuthIP filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="215e3-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**intervalo de peso de FWPM de \_ \_ \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="215e3-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM\_WEIGHT\_RANGE\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="215e3-117">(0x0)</span><span class="sxs-lookup"><span data-stu-id="215e3-117">(0x0)</span></span>
</dt> <dt>



<span data-ttu-id="215e3-118">BFE asigna un peso con este valor de intervalo a los filtros de la Directiva de IPsec.</span><span class="sxs-lookup"><span data-stu-id="215e3-118">BFE assigns a weight with this range value to IPsec policy filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="215e3-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**\_ \_ rango máximo de peso de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="215e3-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM\_WEIGHT\_RANGE\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="215e3-120">(**MAXUINT64** >> 60)</span><span class="sxs-lookup"><span data-stu-id="215e3-120">(**MAXUINT64** >> 60)</span></span>
</dt> <dt>



<span data-ttu-id="215e3-121">Valor máximo permitido para el intervalo de peso del filtro.</span><span class="sxs-lookup"><span data-stu-id="215e3-121">Maximum allowed filter weight range value.</span></span>


</dt> </dl> </dd> </dl>

> [!Note]  
> <span data-ttu-id="215e3-122">**MAXUINT64** representa el mayor valor posible de **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="215e3-122">**MAXUINT64** represents the largest possible value of **UINT64**.</span></span> <span data-ttu-id="215e3-123">El valor de esta constante es 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="215e3-123">The value of this constant is 0xFFFFFFFFFFFFFFFF.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="215e3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="215e3-124">Requirements</span></span>



| <span data-ttu-id="215e3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="215e3-125">Requirement</span></span> | <span data-ttu-id="215e3-126">Value</span><span class="sxs-lookup"><span data-stu-id="215e3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="215e3-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="215e3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="215e3-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="215e3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="215e3-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="215e3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="215e3-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="215e3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="215e3-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="215e3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="215e3-132"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="215e3-132"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





