---
description: Especifica las marcas de enlace que se van a usar al asignar las superficies de Microsoft Direct3D 11 para los ejemplos de medios.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: MF_SA_D3D11_BINDFLAGS atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360766"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a><span data-ttu-id="321b5-103">MF \_ SA \_ D3D11 \_ BINDFLAGS atributo</span><span class="sxs-lookup"><span data-stu-id="321b5-103">MF\_SA\_D3D11\_BINDFLAGS attribute</span></span>

<span data-ttu-id="321b5-104">Especifica las marcas de enlace que se van a usar al asignar las superficies de Microsoft Direct3D 11 para los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="321b5-104">Specifies the binding flags to use when allocating Microsoft Direct3D 11 surfaces for media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="321b5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="321b5-105">Data type</span></span>

<span data-ttu-id="321b5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="321b5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="321b5-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="321b5-107">Remarks</span></span>

<span data-ttu-id="321b5-108">El valor de este atributo es **una operación OR bit a bit** de marcas de [**\_ \_ marcador de enlace D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="321b5-108">The value of this attribute is a bitwise **OR** of [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) flags.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="321b5-109">Microsoft Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="321b5-109">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="321b5-110">En este contexto, el atributo solo se aplica cuando la transformación de Microsoft Media Foundation (MFT) devuelve **true** para el atributo de [ \_ reconocimiento de SA \_ \_ D3D11 de MF](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="321b5-110">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="321b5-111">Si una MFT es compatible con Direct3D 11, este atributo proporciona una sugerencia a la MFT al asignar las superficies de Microsoft Direct3D para la salida.</span><span class="sxs-lookup"><span data-stu-id="321b5-111">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="321b5-112">Establezca el atributo de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="321b5-112">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="321b5-113">Llame a [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obtener el almacén de atributos de MFT.</span><span class="sxs-lookup"><span data-stu-id="321b5-113">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="321b5-114">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="321b5-114">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="321b5-115">La canalización Media Foundation establece el atributo antes de que se inicie el streaming.</span><span class="sxs-lookup"><span data-stu-id="321b5-115">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="321b5-116">La MFT debe intentar respetar la configuración cuando asigna superficies.</span><span class="sxs-lookup"><span data-stu-id="321b5-116">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="321b5-117">Si eso no es posible, el MFT puede omitir el atributo, en lugar de generar un error en la asignación.</span><span class="sxs-lookup"><span data-stu-id="321b5-117">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="321b5-118">Además, si la MFT requiere superficies de Direct3D para la entrada, puede exponer este atributo como una sugerencia sobre cómo se deben asignar las superficies de entrada.</span><span class="sxs-lookup"><span data-stu-id="321b5-118">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="321b5-119">Consulte el atributo como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="321b5-119">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="321b5-120">Llame a [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obtener los atributos del flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="321b5-120">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="321b5-121">Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="321b5-121">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="321b5-122">Asignador de ejemplo</span><span class="sxs-lookup"><span data-stu-id="321b5-122">Sample Allocator</span></span>

<span data-ttu-id="321b5-123">Este atributo se puede establecer en el asignador de ejemplo de vídeo, en el método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="321b5-123">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="321b5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="321b5-124">Requirements</span></span>



| <span data-ttu-id="321b5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="321b5-125">Requirement</span></span> | <span data-ttu-id="321b5-126">Value</span><span class="sxs-lookup"><span data-stu-id="321b5-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="321b5-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="321b5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="321b5-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="321b5-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="321b5-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="321b5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="321b5-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="321b5-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="321b5-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="321b5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="321b5-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="321b5-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321b5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="321b5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321b5-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="321b5-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
