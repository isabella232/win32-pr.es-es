---
description: Recupera las métricas de calidad de la cancelación de eco acústico (AEC) del DSP de captura de voz.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: Propiedad MFPKEY_WMAAECMA_QUALITY_METRICS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696691"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a><span data-ttu-id="7bf37-103">\_Propiedad de \_ \_ métricas de calidad de MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="7bf37-103">MFPKEY\_WMAAECMA\_QUALITY\_METRICS Property</span></span>

<span data-ttu-id="7bf37-104">Recupera las métricas de calidad de la cancelación de eco acústico (AEC) del DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="7bf37-104">Retrieves quality metrics on acoustic echo cancellation (AEC) from the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7bf37-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7bf37-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7bf37-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="7bf37-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7bf37-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7bf37-107">Data Type</span></span>

<span data-ttu-id="7bf37-108">BLOB de VT \_</span><span class="sxs-lookup"><span data-stu-id="7bf37-108">VT\_BLOB</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf37-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bf37-109">Remarks</span></span>

<span data-ttu-id="7bf37-110">El valor de esta propiedad es una estructura de [ \_ struct AecQualityMetrics](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) .</span><span class="sxs-lookup"><span data-stu-id="7bf37-110">The value of this property is an [AecQualityMetrics\_Struct](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) structure.</span></span> <span data-ttu-id="7bf37-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7bf37-111">This property is read-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf37-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bf37-112">Requirements</span></span>



| <span data-ttu-id="7bf37-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bf37-113">Requirement</span></span> | <span data-ttu-id="7bf37-114">Value</span><span class="sxs-lookup"><span data-stu-id="7bf37-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf37-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bf37-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf37-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7bf37-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7bf37-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bf37-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf37-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bf37-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7bf37-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bf37-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf37-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf37-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf37-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bf37-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf37-122">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7bf37-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7bf37-123">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="7bf37-123">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
