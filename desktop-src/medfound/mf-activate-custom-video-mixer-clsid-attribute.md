---
description: CLSID de un mezclador de vídeo personalizado para el receptor de medios de representador de vídeo mejorado (EVR).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360388"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a><span data-ttu-id="566bf-103">MF \_ activar \_ el \_ \_ atributo CLSID del mezclador de vídeo personalizado \_</span><span class="sxs-lookup"><span data-stu-id="566bf-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID attribute</span></span>

<span data-ttu-id="566bf-104">CLSID de un mezclador de vídeo personalizado para el receptor de medios de representador de vídeo mejorado (EVR).</span><span class="sxs-lookup"><span data-stu-id="566bf-104">CLSID of a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="566bf-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="566bf-105">Data type</span></span>

<span data-ttu-id="566bf-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="566bf-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="566bf-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="566bf-107">Remarks</span></span>

<span data-ttu-id="566bf-108">Si va a crear EVR a través de un objeto de activación, puede usar este atributo para establecer un mezclador de vídeo personalizado en EVR.</span><span class="sxs-lookup"><span data-stu-id="566bf-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="566bf-109">Use este atributo como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="566bf-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="566bf-110">Llame a la función [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear un objeto de activación para EVR.</span><span class="sxs-lookup"><span data-stu-id="566bf-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="566bf-111">La función devuelve un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="566bf-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="566bf-112">Establezca este attribue en el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) llamando a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="566bf-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="566bf-113">El valor del atributo es el CLSID del mezclador de vídeo personalizado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="566bf-113">The value of the attribute is the CLSID of the application's custom video mixer.</span></span>

<span data-ttu-id="566bf-114">Si se establece este atributo, EVR llama a **CoCreateInstance** con el CLSID especificado para crear el mezclador de vídeo personalizado.</span><span class="sxs-lookup"><span data-stu-id="566bf-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video mixer.</span></span> <span data-ttu-id="566bf-115">El mezclador de vídeo debe exponer la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="566bf-115">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="566bf-116">El mezclador se crea como un servidor COM en proceso.</span><span class="sxs-lookup"><span data-stu-id="566bf-116">The mixer is created as an in-process COM server.</span></span>

<span data-ttu-id="566bf-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="566bf-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="566bf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="566bf-118">Requirements</span></span>



| <span data-ttu-id="566bf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="566bf-119">Requirement</span></span> | <span data-ttu-id="566bf-120">Value</span><span class="sxs-lookup"><span data-stu-id="566bf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="566bf-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="566bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="566bf-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="566bf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="566bf-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="566bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="566bf-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="566bf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="566bf-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="566bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="566bf-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="566bf-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="566bf-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="566bf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="566bf-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="566bf-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="566bf-129">Atributos de representador de vídeo mejorados</span><span class="sxs-lookup"><span data-stu-id="566bf-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="566bf-130">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="566bf-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="566bf-131">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="566bf-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="566bf-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="566bf-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="566bf-133">Objetos de activación</span><span class="sxs-lookup"><span data-stu-id="566bf-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




