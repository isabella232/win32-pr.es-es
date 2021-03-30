---
description: Especifica el número de búferes que crea el asignador de ejemplo de vídeo para cada ejemplo de vídeo.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: MF_SA_BUFFERS_PER_SAMPLE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811030"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a><span data-ttu-id="34fe2-103">\_Búferes de SA MF \_ \_ por \_ atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="34fe2-103">MF\_SA\_BUFFERS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="34fe2-104">Especifica el número de búferes que crea el asignador de ejemplo de vídeo para cada ejemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="34fe2-104">Specifies how many buffers the video-sample allocator creates for each video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="34fe2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="34fe2-105">Data type</span></span>

<span data-ttu-id="34fe2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="34fe2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="34fe2-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34fe2-107">Remarks</span></span>

<span data-ttu-id="34fe2-108">Si usa la interfaz [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para asignar ejemplos de vídeo, puede usar este atributo para crear ejemplos de vídeo que contengan varios búferes.</span><span class="sxs-lookup"><span data-stu-id="34fe2-108">If you use the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate video samples, you can use this attribute to create video samples that contain multiple buffers.</span></span> <span data-ttu-id="34fe2-109">Por ejemplo, si el valor del atributo es 2, el asignador crea dos búferes de vídeo para cada ejemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="34fe2-109">For example, if the attribute value is 2, the allocator creates two video buffers for each video sample.</span></span> <span data-ttu-id="34fe2-110">Establezca el atributo en el parámetro *pAttributes* del método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="34fe2-110">Set the attribute in the *pAttributes* parameter of the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

<span data-ttu-id="34fe2-111">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="34fe2-111">The default value is 1.</span></span> <span data-ttu-id="34fe2-112">Si no se establece el atributo, el asignador crea muestras de vídeo que contienen un solo búfer por muestra.</span><span class="sxs-lookup"><span data-stu-id="34fe2-112">If the attribute is not set, the allocator creates video samples that contain a single buffer per sample.</span></span>

<span data-ttu-id="34fe2-113">Este atributo está pensado principalmente para Media Foundation transformaciones (MFTs) que admiten la salida 3D estéreo en la situación siguiente:</span><span class="sxs-lookup"><span data-stu-id="34fe2-113">This attribute is primarily intended for Media Foundation transforms (MFTs) that support stereo 3D output, in the following situation:</span></span>

-   <span data-ttu-id="34fe2-114">MFT es compatible con Microsoft DirectX Graphics Infrastructure (DXGI).</span><span class="sxs-lookup"><span data-stu-id="34fe2-114">The MFT supports Microsoft DirectX Graphics Infrastructure (DXGI).</span></span>
-   <span data-ttu-id="34fe2-115">La MFT asigna sus propios ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="34fe2-115">The MFT allocates its own output samples.</span></span>
-   <span data-ttu-id="34fe2-116">MFT usa la interfaz [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para asignar los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="34fe2-116">The MFT uses the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate the output samples.</span></span>
-   <span data-ttu-id="34fe2-117">El formato de vídeo 3D utiliza un búfer independiente para cada vista.</span><span class="sxs-lookup"><span data-stu-id="34fe2-117">The 3D video format uses a separate buffer for each view.</span></span>

<span data-ttu-id="34fe2-118">Si todos estos criterios son verdaderos, el MFT debe establecer el valor del atributo en 2 (un búfer por vista).</span><span class="sxs-lookup"><span data-stu-id="34fe2-118">If all of these criteria are true, the MFT should set the attribute value to 2 (one buffer per view).</span></span>

## <a name="requirements"></a><span data-ttu-id="34fe2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34fe2-119">Requirements</span></span>



| <span data-ttu-id="34fe2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="34fe2-120">Requirement</span></span> | <span data-ttu-id="34fe2-121">Value</span><span class="sxs-lookup"><span data-stu-id="34fe2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="34fe2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34fe2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="34fe2-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="34fe2-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="34fe2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34fe2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="34fe2-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="34fe2-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="34fe2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34fe2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="34fe2-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="34fe2-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34fe2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="34fe2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34fe2-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34fe2-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




