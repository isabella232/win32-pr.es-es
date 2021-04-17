---
description: Identificador de la ventana de recorte de vídeo.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: MF_ACTIVATE_VIDEO_WINDOW atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678108"
---
# <a name="mf_activate_video_window-attribute"></a><span data-ttu-id="2af23-103">MF \_ activar el atributo de la \_ ventana de vídeo \_</span><span class="sxs-lookup"><span data-stu-id="2af23-103">MF\_ACTIVATE\_VIDEO\_WINDOW attribute</span></span>

<span data-ttu-id="2af23-104">Identificador de la ventana de recorte de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2af23-104">Handle to the video clipping window.</span></span>

## <a name="data-type"></a><span data-ttu-id="2af23-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2af23-105">Data type</span></span>

<span data-ttu-id="2af23-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="2af23-106">**UINT64**</span></span>

<span data-ttu-id="2af23-107">Tratar como **DWORD \_ ptr** (**hWnd**).</span><span class="sxs-lookup"><span data-stu-id="2af23-107">Treat as **DWORD\_PTR** (**HWND**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2af23-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2af23-108">Remarks</span></span>

<span data-ttu-id="2af23-109">Este atributo se aplica al objeto de activación para el representador de vídeo mejorado (EVR).</span><span class="sxs-lookup"><span data-stu-id="2af23-109">This attribute applies to the activation object for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="2af23-110">El valor se establece automáticamente cuando se llama a [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear el objeto de activación EVR.</span><span class="sxs-lookup"><span data-stu-id="2af23-110">The value is set automatically when you call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the EVR activation object.</span></span>

<span data-ttu-id="2af23-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2af23-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2af23-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2af23-112">Requirements</span></span>



| <span data-ttu-id="2af23-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2af23-113">Requirement</span></span> | <span data-ttu-id="2af23-114">Value</span><span class="sxs-lookup"><span data-stu-id="2af23-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2af23-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2af23-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2af23-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2af23-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2af23-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2af23-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2af23-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2af23-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2af23-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2af23-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2af23-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2af23-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2af23-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="2af23-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2af23-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2af23-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2af23-123">Atributos de representador de vídeo mejorados</span><span class="sxs-lookup"><span data-stu-id="2af23-123">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="2af23-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="2af23-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="2af23-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="2af23-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="2af23-126">Objetos de activación</span><span class="sxs-lookup"><span data-stu-id="2af23-126">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




