---
description: Especifica cómo crear un presentador personalizado para el representador de vídeo mejorado (EVR).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082969"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a><span data-ttu-id="abd62-103">MF \_ activar \_ \_ atributo de \_ marcadores de presentador de vídeo personalizado \_</span><span class="sxs-lookup"><span data-stu-id="abd62-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_FLAGS attribute</span></span>

<span data-ttu-id="abd62-104">Especifica cómo crear un presentador personalizado para el representador de vídeo mejorado (EVR).</span><span class="sxs-lookup"><span data-stu-id="abd62-104">Specifies how to create a custom presenter for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="abd62-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="abd62-105">Data type</span></span>

<span data-ttu-id="abd62-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="abd62-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="abd62-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abd62-107">Remarks</span></span>

<span data-ttu-id="abd62-108">Puede establecer este atributo en el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Obtenido de la función [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="abd62-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="abd62-109">El valor de este atributo es **una operación OR bit a bit** de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="abd62-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="abd62-110">Value</span><span class="sxs-lookup"><span data-stu-id="abd62-110">Value</span></span>                                          | <span data-ttu-id="abd62-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="abd62-111">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd62-112">**MF \_ activar \_ el \_ presentador personalizado \_ ALLOWFAIL**</span><span class="sxs-lookup"><span data-stu-id="abd62-112">**MF\_ACTIVATE\_CUSTOM\_PRESENTER\_ALLOWFAIL**</span></span> | <span data-ttu-id="abd62-113">Si el método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no puede crear el presentador personalizado de la aplicación, usa el presentador de EVR predeterminado en su lugar.</span><span class="sxs-lookup"><span data-stu-id="abd62-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom presenter, it uses the default EVR presenter instead.</span></span> <span data-ttu-id="abd62-114">De forma predeterminada, si se produce un error en el objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) cuando intenta crear el presentador personalizado, se produce un error en el método **ActivateObject** .</span><span class="sxs-lookup"><span data-stu-id="abd62-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom presenter, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="abd62-115">Las aplicaciones pueden usar el atributo [**\_ \_ \_ \_ \_ CLSID del presentador de vídeo personalizado MF**](mf-activate-custom-video-presenter-clsid-attribute.md) para especificar un presentador personalizado para el EVR.</span><span class="sxs-lookup"><span data-stu-id="abd62-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) attribute to specify a custom presenter for the EVR.</span></span>

<span data-ttu-id="abd62-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="abd62-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="abd62-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abd62-117">Requirements</span></span>



| <span data-ttu-id="abd62-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd62-118">Requirement</span></span> | <span data-ttu-id="abd62-119">Value</span><span class="sxs-lookup"><span data-stu-id="abd62-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="abd62-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abd62-120">Minimum supported client</span></span><br/> | <span data-ttu-id="abd62-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="abd62-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="abd62-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abd62-122">Minimum supported server</span></span><br/> | <span data-ttu-id="abd62-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="abd62-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="abd62-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abd62-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd62-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="abd62-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abd62-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="abd62-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd62-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="abd62-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="abd62-128">Atributos de representador de vídeo mejorados</span><span class="sxs-lookup"><span data-stu-id="abd62-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="abd62-129">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="abd62-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="abd62-130">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="abd62-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="abd62-131">Objetos de activación</span><span class="sxs-lookup"><span data-stu-id="abd62-131">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="abd62-132">Cómo escribir un presentador de EVR</span><span class="sxs-lookup"><span data-stu-id="abd62-132">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




