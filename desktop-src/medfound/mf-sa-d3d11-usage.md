---
description: Especifica cómo asignar las superficies de Microsoft Direct3D 11 para los ejemplos de medios.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: MF_SA_D3D11_USAGE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275691"
---
# <a name="mf_sa_d3d11_usage-attribute"></a><span data-ttu-id="879dc-103">MF \_ SA \_ D3D11 \_ atributo Usage</span><span class="sxs-lookup"><span data-stu-id="879dc-103">MF\_SA\_D3D11\_USAGE attribute</span></span>

<span data-ttu-id="879dc-104">Especifica cómo asignar las superficies de Microsoft Direct3D 11 para los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="879dc-104">Specifies how to allocate Microsoft Direct3D 11 surfaces for media samples.</span></span> <span data-ttu-id="879dc-105">El uso refleja directamente si una muestra es accesible por la CPU o la GPU.</span><span class="sxs-lookup"><span data-stu-id="879dc-105">The usage directly reflects whether a sample is accessible by the CPU or GPU.</span></span>

## <a name="data-type"></a><span data-ttu-id="879dc-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="879dc-106">Data type</span></span>

<span data-ttu-id="879dc-107">**D3D11 \_ USO** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="879dc-107">**D3D11\_USAGE** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="879dc-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="879dc-108">Remarks</span></span>

<span data-ttu-id="879dc-109">El valor de este atributo es un valor de [**\_ uso de D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .</span><span class="sxs-lookup"><span data-stu-id="879dc-109">The value of this attribute is a [**D3D11\_USAGE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) value.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="879dc-110">Microsoft Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="879dc-110">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="879dc-111">En este contexto, el atributo solo se aplica cuando la transformación de Microsoft Media Foundation (MFT) devuelve **true** para el atributo de [ \_ reconocimiento de SA \_ \_ D3D11 de MF](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="879dc-111">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="879dc-112">Si una MFT es compatible con Direct3D 11, este atributo proporciona una sugerencia a la MFT al asignar las superficies de Microsoft Direct3D para la salida.</span><span class="sxs-lookup"><span data-stu-id="879dc-112">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="879dc-113">Establezca el atributo de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="879dc-113">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="879dc-114">Llame a [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obtener el almacén de atributos de MFT.</span><span class="sxs-lookup"><span data-stu-id="879dc-114">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="879dc-115">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="879dc-115">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="879dc-116">La canalización Media Foundation establece el atributo antes de que se inicie el streaming.</span><span class="sxs-lookup"><span data-stu-id="879dc-116">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="879dc-117">La MFT debe intentar respetar la configuración cuando asigna superficies.</span><span class="sxs-lookup"><span data-stu-id="879dc-117">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="879dc-118">Si eso no es posible, el MFT puede omitir el atributo, en lugar de generar un error en la asignación.</span><span class="sxs-lookup"><span data-stu-id="879dc-118">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="879dc-119">Además, si la MFT requiere superficies de Direct3D para la entrada, puede exponer este atributo como una sugerencia sobre cómo se deben asignar las superficies de entrada.</span><span class="sxs-lookup"><span data-stu-id="879dc-119">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="879dc-120">Consulte el atributo como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="879dc-120">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="879dc-121">Llame a [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obtener los atributos del flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="879dc-121">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="879dc-122">Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="879dc-122">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="879dc-123">Asignador de ejemplo</span><span class="sxs-lookup"><span data-stu-id="879dc-123">Sample Allocator</span></span>

<span data-ttu-id="879dc-124">Este atributo se puede establecer en el asignador de ejemplo de vídeo, en el método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="879dc-124">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="879dc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="879dc-125">Requirements</span></span>



| <span data-ttu-id="879dc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="879dc-126">Requirement</span></span> | <span data-ttu-id="879dc-127">Value</span><span class="sxs-lookup"><span data-stu-id="879dc-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="879dc-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="879dc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="879dc-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="879dc-129">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="879dc-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="879dc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="879dc-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="879dc-131">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="879dc-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="879dc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="879dc-133"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="879dc-133"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="879dc-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="879dc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="879dc-135">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="879dc-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
