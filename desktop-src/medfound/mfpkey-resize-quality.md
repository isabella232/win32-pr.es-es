---
description: Especifica si se debe usar un algoritmo que genere vídeo de mayor calidad o un algoritmo más rápido.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: Propiedad MFPKEY_RESIZE_QUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715872"
---
# <a name="mfpkey_resize_quality-property"></a><span data-ttu-id="70b92-103">MFPKEY \_ propiedad de calidad de REdimensionamiento \_</span><span class="sxs-lookup"><span data-stu-id="70b92-103">MFPKEY\_RESIZE\_QUALITY Property</span></span>

<span data-ttu-id="70b92-104">Especifica si se debe usar un algoritmo que genere vídeo de mayor calidad o un algoritmo más rápido.</span><span class="sxs-lookup"><span data-stu-id="70b92-104">Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="70b92-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="70b92-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="70b92-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="70b92-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="70b92-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="70b92-107">Data Type</span></span>

<span data-ttu-id="70b92-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="70b92-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="70b92-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="70b92-109">Applies To</span></span>

-   [<span data-ttu-id="70b92-110">Vídeo de tamaño DSP</span><span class="sxs-lookup"><span data-stu-id="70b92-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="70b92-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70b92-111">Remarks</span></span>

<span data-ttu-id="70b92-112">Utilice uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="70b92-112">Use one of the following values:</span></span>



| <span data-ttu-id="70b92-113">Value</span><span class="sxs-lookup"><span data-stu-id="70b92-113">Value</span></span>     | <span data-ttu-id="70b92-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="70b92-114">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="70b92-115">VT \_ falso</span><span class="sxs-lookup"><span data-stu-id="70b92-115">VT\_FALSE</span></span> | <span data-ttu-id="70b92-116">Algoritmo más rápido</span><span class="sxs-lookup"><span data-stu-id="70b92-116">Faster algorithm</span></span>     |
| <span data-ttu-id="70b92-117">VT \_ true</span><span class="sxs-lookup"><span data-stu-id="70b92-117">VT\_TRUE</span></span>  | <span data-ttu-id="70b92-118">Vídeo de mayor calidad</span><span class="sxs-lookup"><span data-stu-id="70b92-118">Higher-quality video</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="70b92-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70b92-119">Requirements</span></span>



| <span data-ttu-id="70b92-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="70b92-120">Requirement</span></span> | <span data-ttu-id="70b92-121">Value</span><span class="sxs-lookup"><span data-stu-id="70b92-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70b92-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70b92-122">Minimum supported client</span></span><br/> | <span data-ttu-id="70b92-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="70b92-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="70b92-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70b92-124">Minimum supported server</span></span><br/> | <span data-ttu-id="70b92-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="70b92-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70b92-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70b92-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="70b92-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="70b92-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70b92-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="70b92-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b92-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70b92-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
