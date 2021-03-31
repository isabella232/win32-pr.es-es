---
description: Establece el umbral en el que el codificador considera que un campo de vídeo es redundante.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propiedad AVEncVideoInverseTelecineThreshold (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805395"
---
# <a name="avencvideoinversetelecinethreshold-property"></a><span data-ttu-id="18340-103">Propiedad AVEncVideoInverseTelecineThreshold</span><span class="sxs-lookup"><span data-stu-id="18340-103">AVEncVideoInverseTelecineThreshold property</span></span>

<span data-ttu-id="18340-104">Establece el umbral en el que el codificador considera que un campo de vídeo es redundante.</span><span class="sxs-lookup"><span data-stu-id="18340-104">Sets the threshold at which the encoder considers a video field redundant.</span></span>

<span data-ttu-id="18340-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="18340-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="18340-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="18340-106">Data type</span></span>

<span data-ttu-id="18340-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="18340-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="18340-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="18340-108">Property GUID</span></span>

<span data-ttu-id="18340-109">**CODECAPI \_ AVEncVideoInverseTelecineThreshold**</span><span class="sxs-lookup"><span data-stu-id="18340-109">**CODECAPI\_AVEncVideoInverseTelecineThreshold**</span></span>

## <a name="property-value"></a><span data-ttu-id="18340-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="18340-110">Property value</span></span>

<span data-ttu-id="18340-111">El valor de esta propiedad tiene el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="18340-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="18340-112">Value</span><span class="sxs-lookup"><span data-stu-id="18340-112">Value</span></span> | <span data-ttu-id="18340-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="18340-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="18340-114">0</span><span class="sxs-lookup"><span data-stu-id="18340-114">0</span></span>     | <span data-ttu-id="18340-115">Es menos probable que el codificador tenga en cuenta los campos de vídeo redundantes.</span><span class="sxs-lookup"><span data-stu-id="18340-115">The encoder is less likely to consider video fields redundant.</span></span> |
| <span data-ttu-id="18340-116">100</span><span class="sxs-lookup"><span data-stu-id="18340-116">100</span></span>   | <span data-ttu-id="18340-117">Es más probable que el codificador tenga en cuenta los campos de vídeo redundantes.</span><span class="sxs-lookup"><span data-stu-id="18340-117">The encoder is more likely to consider video fields redundant.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="18340-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18340-118">Remarks</span></span>

<span data-ttu-id="18340-119">Establezca esta propiedad si el codificador está realizando telecine inversa con un origen de vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="18340-119">Set this property if the encoder is performing inverse telecine with an analog video source.</span></span>

## <a name="requirements"></a><span data-ttu-id="18340-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18340-120">Requirements</span></span>



| <span data-ttu-id="18340-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="18340-121">Requirement</span></span> | <span data-ttu-id="18340-122">Value</span><span class="sxs-lookup"><span data-stu-id="18340-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18340-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18340-123">Minimum supported client</span></span><br/> | <span data-ttu-id="18340-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="18340-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="18340-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18340-125">Minimum supported server</span></span><br/> | <span data-ttu-id="18340-126">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="18340-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="18340-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18340-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="18340-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="18340-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18340-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="18340-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18340-130">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="18340-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="18340-131">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="18340-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




