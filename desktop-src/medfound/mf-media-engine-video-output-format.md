---
description: Establece el formato de representación y destino para el motor multimedia.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820202"
---
# <a name="mf_media_engine_video_output_format-attribute"></a><span data-ttu-id="03e0b-103">\_Atributo de \_ \_ formato de salida de vídeo del motor de \_ multimedia MF \_</span><span class="sxs-lookup"><span data-stu-id="03e0b-103">MF\_MEDIA\_ENGINE\_VIDEO\_OUTPUT\_FORMAT attribute</span></span>

<span data-ttu-id="03e0b-104">Establece el formato de representación y destino para el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="03e0b-104">Sets the render-target format for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="03e0b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="03e0b-105">Data type</span></span>

<span data-ttu-id="03e0b-106">**DXGI \_ FORMATO** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="03e0b-106">**DXGI\_FORMAT** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="03e0b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03e0b-107">Remarks</span></span>

<span data-ttu-id="03e0b-108">Establezca este atributo si crea el motor multimedia en modo de servidor de tramas.</span><span class="sxs-lookup"><span data-stu-id="03e0b-108">Set this attribute if you create the Media Engine in frame-server mode.</span></span> <span data-ttu-id="03e0b-109">Para obtener más información, vea [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="03e0b-109">For more information, see [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="03e0b-110">El valor del atributo es un valor [de \_ formato de DXGI](../direct3d9/d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="03e0b-110">The value of the attribute is a [DXGI\_FORMAT](../direct3d9/d3dformat.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03e0b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03e0b-111">Requirements</span></span>



| <span data-ttu-id="03e0b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="03e0b-112">Requirement</span></span> | <span data-ttu-id="03e0b-113">Value</span><span class="sxs-lookup"><span data-stu-id="03e0b-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="03e0b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e0b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="03e0b-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="03e0b-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="03e0b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e0b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="03e0b-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="03e0b-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="03e0b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03e0b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="03e0b-119"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="03e0b-119"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03e0b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="03e0b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e0b-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03e0b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
