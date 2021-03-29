---
description: Especifica cómo crear un mezclador personalizado para el representador de vídeo mejorado (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815515"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a><span data-ttu-id="3a13c-103">MF \_ activar \_ \_ atributo de \_ marcas de mezclador de vídeo personalizado \_</span><span class="sxs-lookup"><span data-stu-id="3a13c-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_FLAGS attribute</span></span>

<span data-ttu-id="3a13c-104">Especifica cómo crear un mezclador personalizado para el representador de vídeo mejorado (EVR).</span><span class="sxs-lookup"><span data-stu-id="3a13c-104">Specifies how to create a custom mixer for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="3a13c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3a13c-105">Data type</span></span>

<span data-ttu-id="3a13c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3a13c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3a13c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a13c-107">Remarks</span></span>

<span data-ttu-id="3a13c-108">Puede establecer este atributo en el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Obtenido de la función [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="3a13c-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="3a13c-109">El valor de este atributo es **una operación OR bit a bit** de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a13c-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="3a13c-110">Value</span><span class="sxs-lookup"><span data-stu-id="3a13c-110">Value</span></span>                                      | <span data-ttu-id="3a13c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a13c-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a13c-112">**MF \_ activar \_ \_ mezclador personalizado \_ ALLOWFAIL**</span><span class="sxs-lookup"><span data-stu-id="3a13c-112">**MF\_ACTIVATE\_CUSTOM\_MIXER\_ALLOWFAIL**</span></span> | <span data-ttu-id="3a13c-113">Si el método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no puede crear el mezclador personalizado de la aplicación, utiliza el mezclador de EVR predeterminado en su lugar.</span><span class="sxs-lookup"><span data-stu-id="3a13c-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom mixer, it uses the default EVR mixer instead.</span></span> <span data-ttu-id="3a13c-114">De forma predeterminada, si se produce un error en el objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) cuando intenta crear el mezclador personalizado, se produce un error en el método **ActivateObject** .</span><span class="sxs-lookup"><span data-stu-id="3a13c-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom mixer, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="3a13c-115">Las aplicaciones pueden usar el atributo [**MF \_ activar \_ mezclador de \_ vídeo personalizado \_ \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) para especificar un mezclador personalizado para el EVR.</span><span class="sxs-lookup"><span data-stu-id="3a13c-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) attribute to specify a custom mixer for the EVR.</span></span>

<span data-ttu-id="3a13c-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3a13c-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a13c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a13c-117">Requirements</span></span>



| <span data-ttu-id="3a13c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a13c-118">Requirement</span></span> | <span data-ttu-id="3a13c-119">Value</span><span class="sxs-lookup"><span data-stu-id="3a13c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a13c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a13c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a13c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a13c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a13c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a13c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a13c-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a13c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a13c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a13c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a13c-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a13c-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a13c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a13c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a13c-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a13c-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a13c-128">Atributos de representador de vídeo mejorados</span><span class="sxs-lookup"><span data-stu-id="3a13c-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a13c-129">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a13c-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3a13c-130">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a13c-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3a13c-131">Objetos de activación</span><span class="sxs-lookup"><span data-stu-id="3a13c-131">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




