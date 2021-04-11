---
description: Especifica un objeto de activación que crea un mezclador de vídeo personalizado para el receptor de medios de representador de vídeo mejorado (EVR).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155573"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a><span data-ttu-id="64d4a-103">MF \_ activar \_ el \_ atributo de activación del mezclador de vídeo personalizado \_ \_</span><span class="sxs-lookup"><span data-stu-id="64d4a-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_ACTIVATE attribute</span></span>

<span data-ttu-id="64d4a-104">Especifica un objeto de activación que crea un mezclador de vídeo personalizado para el receptor de medios de representador de vídeo mejorado (EVR).</span><span class="sxs-lookup"><span data-stu-id="64d4a-104">Specifies an activation object that creates a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="64d4a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="64d4a-105">Data type</span></span>

<span data-ttu-id="64d4a-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="64d4a-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="64d4a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64d4a-107">Remarks</span></span>

<span data-ttu-id="64d4a-108">Si va a crear EVR a través de un objeto de activación, puede usar este atributo para establecer un mezclador de vídeo personalizado en EVR.</span><span class="sxs-lookup"><span data-stu-id="64d4a-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="64d4a-109">Use este atributo como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="64d4a-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="64d4a-110">Llame a la función [_ *MFCreateVideoRendererActivate* \*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear un objeto de activación para EVR.</span><span class="sxs-lookup"><span data-stu-id="64d4a-110">Call the [_ *MFCreateVideoRendererActivate*\*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="64d4a-111">La función devuelve un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="64d4a-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="64d4a-112">Establezca este atributo en el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) llamando a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="64d4a-112">Set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="64d4a-113">El valor del atributo es un puntero a un objeto de activación implementado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="64d4a-113">The value of the attribute is a pointer to an activation object implemented by the caller.</span></span> <span data-ttu-id="64d4a-114">El objeto de activación del llamador debe exponer la interfaz **IMFActivate** .</span><span class="sxs-lookup"><span data-stu-id="64d4a-114">The caller's activation object must expose the **IMFActivate** interface.</span></span>

<span data-ttu-id="64d4a-115">Si establece este atributo, EVR llama a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para crear el mezclador de vídeo personalizado.</span><span class="sxs-lookup"><span data-stu-id="64d4a-115">If you set this attribute, the EVR calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the custom video mixer.</span></span> <span data-ttu-id="64d4a-116">El mezclador de vídeo debe exponer la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="64d4a-116">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span>

<span data-ttu-id="64d4a-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="64d4a-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d4a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d4a-118">Requirements</span></span>



| <span data-ttu-id="64d4a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d4a-119">Requirement</span></span> | <span data-ttu-id="64d4a-120">Value</span><span class="sxs-lookup"><span data-stu-id="64d4a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64d4a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64d4a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="64d4a-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64d4a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="64d4a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64d4a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="64d4a-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="64d4a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="64d4a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64d4a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d4a-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64d4a-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d4a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="64d4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d4a-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64d4a-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="64d4a-129">Atributos de representador de vídeo mejorados</span><span class="sxs-lookup"><span data-stu-id="64d4a-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="64d4a-130">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="64d4a-130">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="64d4a-131">**IMFAttributes:: Setunknown (**</span><span class="sxs-lookup"><span data-stu-id="64d4a-131">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="64d4a-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="64d4a-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="64d4a-133">Objetos de activación</span><span class="sxs-lookup"><span data-stu-id="64d4a-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




