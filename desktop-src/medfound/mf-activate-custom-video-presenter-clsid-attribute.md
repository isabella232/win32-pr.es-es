---
description: CLSID de un presentador de vídeo personalizado para el receptor de medios de representador de vídeo mejorado (EVR).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696606"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a><span data-ttu-id="88e2f-103">MF \_ activar \_ \_ \_ atributo CLSID del presentador de vídeo personalizado \_</span><span class="sxs-lookup"><span data-stu-id="88e2f-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID attribute</span></span>

<span data-ttu-id="88e2f-104">CLSID de un presentador de vídeo personalizado para el receptor de medios de representador de vídeo mejorado (EVR).</span><span class="sxs-lookup"><span data-stu-id="88e2f-104">CLSID of a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="88e2f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="88e2f-105">Data type</span></span>

<span data-ttu-id="88e2f-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="88e2f-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="88e2f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88e2f-107">Remarks</span></span>

<span data-ttu-id="88e2f-108">Si va a crear EVR a través de un objeto de activación, puede usar este atributo para establecer un presentador de vídeo personalizado en EVR.</span><span class="sxs-lookup"><span data-stu-id="88e2f-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="88e2f-109">Use este atributo como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="88e2f-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="88e2f-110">Llame a la función [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear un objeto de activación para EVR.</span><span class="sxs-lookup"><span data-stu-id="88e2f-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="88e2f-111">La función devuelve un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="88e2f-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="88e2f-112">Establezca este attribue en el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) llamando a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="88e2f-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="88e2f-113">El valor del atributo es el CLSID del presentador de vídeo personalizado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88e2f-113">The value of the attribute is the CLSID of the application's custom video presenter.</span></span>

<span data-ttu-id="88e2f-114">Si se establece este atributo, EVR llama a **CoCreateInstance** con el CLSID especificado para crear el presentador de vídeo personalizado.</span><span class="sxs-lookup"><span data-stu-id="88e2f-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video presenter.</span></span> <span data-ttu-id="88e2f-115">El presentador de vídeo debe exponer la interfaz [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) .</span><span class="sxs-lookup"><span data-stu-id="88e2f-115">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span> <span data-ttu-id="88e2f-116">El presentador se crea como un servidor COM en proceso.</span><span class="sxs-lookup"><span data-stu-id="88e2f-116">The presenter is created as an in-process COM server.</span></span>

<span data-ttu-id="88e2f-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="88e2f-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e2f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88e2f-118">Requirements</span></span>



| <span data-ttu-id="88e2f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="88e2f-119">Requirement</span></span> | <span data-ttu-id="88e2f-120">Value</span><span class="sxs-lookup"><span data-stu-id="88e2f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88e2f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88e2f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="88e2f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="88e2f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="88e2f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88e2f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="88e2f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="88e2f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="88e2f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88e2f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="88e2f-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="88e2f-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e2f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="88e2f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e2f-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="88e2f-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="88e2f-129">Atributos de representador de vídeo mejorados</span><span class="sxs-lookup"><span data-stu-id="88e2f-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="88e2f-130">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="88e2f-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="88e2f-131">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="88e2f-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="88e2f-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="88e2f-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="88e2f-133">Objetos de activación</span><span class="sxs-lookup"><span data-stu-id="88e2f-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="88e2f-134">Cómo escribir un presentador de EVR</span><span class="sxs-lookup"><span data-stu-id="88e2f-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




