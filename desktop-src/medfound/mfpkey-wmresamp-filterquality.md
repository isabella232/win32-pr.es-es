---
description: Especifica la calidad de la salida.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: Propiedad MFPKEY_WMRESAMP_FILTERQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275847"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a><span data-ttu-id="93352-103">\_ \_ Propiedad FILTERQUALITY de MFPKEY WMRESAMP</span><span class="sxs-lookup"><span data-stu-id="93352-103">MFPKEY\_WMRESAMP\_FILTERQUALITY Property</span></span>

<span data-ttu-id="93352-104">Especifica la calidad de la salida.</span><span class="sxs-lookup"><span data-stu-id="93352-104">Specifies the quality of the output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="93352-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="93352-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="93352-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="93352-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="93352-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="93352-107">Data Type</span></span>

<span data-ttu-id="93352-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="93352-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="93352-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="93352-109">Applies To</span></span>

-   [<span data-ttu-id="93352-110">DSP de remuestreador de audio</span><span class="sxs-lookup"><span data-stu-id="93352-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="93352-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93352-111">Remarks</span></span>

<span data-ttu-id="93352-112">El intervalo válido de esta propiedad es de 1 a 60, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="93352-112">The valid range of this property is 1 to 60, inclusive.</span></span> <span data-ttu-id="93352-113">Los valores más altos producen una salida de mayor calidad, pero introducen más latencia.</span><span class="sxs-lookup"><span data-stu-id="93352-113">Higher values produce higher-quality output, but introduce more latency.</span></span> <span data-ttu-id="93352-114">Un valor de 1 es esencialmente el mismo que el de la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="93352-114">A value of 1 is essentially the same as linear interpolation.</span></span>

## <a name="requirements"></a><span data-ttu-id="93352-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93352-115">Requirements</span></span>



| <span data-ttu-id="93352-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="93352-116">Requirement</span></span> | <span data-ttu-id="93352-117">Value</span><span class="sxs-lookup"><span data-stu-id="93352-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93352-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93352-118">Minimum supported client</span></span><br/> | <span data-ttu-id="93352-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="93352-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="93352-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93352-120">Minimum supported server</span></span><br/> | <span data-ttu-id="93352-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="93352-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93352-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93352-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="93352-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="93352-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93352-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="93352-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93352-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="93352-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
