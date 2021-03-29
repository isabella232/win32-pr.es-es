---
description: Establece un identificador para una ventana de reproducción de vídeo para el motor multimedia.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: MF_MEDIA_ENGINE_PLAYBACK_HWND atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003340"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a><span data-ttu-id="07420-103">MF \_ \_ \_ atributo HWND de reproducción del motor de multimedia MF \_</span><span class="sxs-lookup"><span data-stu-id="07420-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND attribute</span></span>

<span data-ttu-id="07420-104">Establece un identificador para una ventana de reproducción de vídeo para el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="07420-104">Sets a handle to a video playback window for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="07420-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="07420-105">Data type</span></span>

<span data-ttu-id="07420-106">**HWnd** almacenado como **UINT64**</span><span class="sxs-lookup"><span data-stu-id="07420-106">**HWND** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="07420-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="07420-107">Get/set</span></span>

<span data-ttu-id="07420-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="07420-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="07420-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="07420-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="remarks"></a><span data-ttu-id="07420-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07420-110">Remarks</span></span>

<span data-ttu-id="07420-111">Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="07420-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="07420-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07420-112">Requirements</span></span>



| <span data-ttu-id="07420-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="07420-113">Requirement</span></span> | <span data-ttu-id="07420-114">Value</span><span class="sxs-lookup"><span data-stu-id="07420-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="07420-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07420-115">Minimum supported client</span></span><br/> | <span data-ttu-id="07420-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="07420-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="07420-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07420-117">Minimum supported server</span></span><br/> | <span data-ttu-id="07420-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="07420-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="07420-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07420-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="07420-120"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="07420-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07420-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="07420-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07420-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07420-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




