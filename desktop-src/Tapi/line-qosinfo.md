---
description: El mensaje QOSINFO de la línea de TSPI \_ hace que TAPI desencadene un evento de QoS. Consulte ITQOSEvent para obtener información adicional.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Mensaje de LINE_QOSINFO (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680365"
---
# <a name="line_qosinfo-message"></a><span data-ttu-id="07967-104">Mensaje de línea \_ QOSINFO</span><span class="sxs-lookup"><span data-stu-id="07967-104">LINE\_QOSINFO message</span></span>

<span data-ttu-id="07967-105">El mensaje **\_ QOSINFO** de la línea de TSPI hace que TAPI desencadene un evento de QoS.</span><span class="sxs-lookup"><span data-stu-id="07967-105">The TSPI **LINE\_QOSINFO** message causes TAPI to fire a QOS event.</span></span> <span data-ttu-id="07967-106">Consulte [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="07967-106">See [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) for additional information.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="07967-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07967-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07967-108">*htLine*</span><span class="sxs-lookup"><span data-stu-id="07967-108">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="07967-109">Identificador de TAPI de la línea.</span><span class="sxs-lookup"><span data-stu-id="07967-109">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="07967-110">*htCall*</span><span class="sxs-lookup"><span data-stu-id="07967-110">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="07967-111">Identificador de TAPI de la llamada.</span><span class="sxs-lookup"><span data-stu-id="07967-111">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="07967-112">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="07967-112">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="07967-113">La línea de valor \_ QOSINFO.</span><span class="sxs-lookup"><span data-stu-id="07967-113">The value LINE\_QOSINFO.</span></span>

</dd> <dt>

<span data-ttu-id="07967-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="07967-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="07967-115">Miembro del enumerador [**de \_ eventos QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) que identifica el tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="07967-115">A member of the [**QOS\_EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) enumerator that identifies the type of event.</span></span>

</dd> <dt>

<span data-ttu-id="07967-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="07967-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="07967-117">Constante de [tipo de medio](./tapiprotocol--constants.md) que identifica los medios de la llamada asociada a este evento.</span><span class="sxs-lookup"><span data-stu-id="07967-117">A [media type](./tapiprotocol--constants.md) constant that identifies the media of the call associated with this event.</span></span>

</dd> <dt>

<span data-ttu-id="07967-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="07967-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="07967-119">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="07967-119">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07967-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07967-120">Requirements</span></span>



| <span data-ttu-id="07967-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="07967-121">Requirement</span></span> | <span data-ttu-id="07967-122">Value</span><span class="sxs-lookup"><span data-stu-id="07967-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="07967-123">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="07967-123">TAPI version</span></span><br/> | <span data-ttu-id="07967-124">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="07967-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="07967-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07967-125">Header</span></span><br/>       | <dl> <span data-ttu-id="07967-126"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="07967-126"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07967-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="07967-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07967-128">**\_evento QoS**</span><span class="sxs-lookup"><span data-stu-id="07967-128">**QOS\_EVENT**</span></span>](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[<span data-ttu-id="07967-129">**ITQOSEvent**</span><span class="sxs-lookup"><span data-stu-id="07967-129">**ITQOSEvent**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

