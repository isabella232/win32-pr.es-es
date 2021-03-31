---
description: Especifica la categoría de dispositivos para un dispositivo de captura de vídeo.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154632"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a><span data-ttu-id="69886-103">\_Tipo de origen de atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ categoría VIDCAP</span><span class="sxs-lookup"><span data-stu-id="69886-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_CATEGORY attribute</span></span>

<span data-ttu-id="69886-104">Especifica la categoría de dispositivos para un dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69886-104">Specifies the device category for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="69886-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="69886-105">Data type</span></span>

<span data-ttu-id="69886-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="69886-106">**GUID**</span></span>

<span data-ttu-id="69886-107">Se define el siguiente valor.</span><span class="sxs-lookup"><span data-stu-id="69886-107">The following value is defined.</span></span>



| <span data-ttu-id="69886-108">Value</span><span class="sxs-lookup"><span data-stu-id="69886-108">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="69886-109">Significado</span><span class="sxs-lookup"><span data-stu-id="69886-109">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <span data-ttu-id="69886-110"><dt>**CLSID \_ VideoInputDeviceCategory**</dt></span><span class="sxs-lookup"><span data-stu-id="69886-110"><dt>**CLSID\_VideoInputDeviceCategory**</dt></span></span> </dl> | <span data-ttu-id="69886-111">Dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69886-111">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="69886-112">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="69886-112">Get/set</span></span>

<span data-ttu-id="69886-113">Para obtener este atributo, llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="69886-113">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="69886-114">Para establecer este atributo, llame a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="69886-114">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="69886-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69886-115">Remarks</span></span>

<span data-ttu-id="69886-116">Use este atributo como entrada de la función [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) al enumerar los dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69886-116">Use this attribute as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function when enumerating video capture devices.</span></span>

<span data-ttu-id="69886-117">Además, este atributo se establece en los objetos de activación devueltos por las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="69886-117">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="69886-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="69886-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="69886-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="69886-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="69886-120">El atributo solo se aplica a los dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69886-120">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="69886-121">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="69886-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="69886-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69886-122">Requirements</span></span>



| <span data-ttu-id="69886-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="69886-123">Requirement</span></span> | <span data-ttu-id="69886-124">Value</span><span class="sxs-lookup"><span data-stu-id="69886-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69886-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69886-125">Minimum supported client</span></span><br/> | <span data-ttu-id="69886-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="69886-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="69886-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69886-127">Minimum supported server</span></span><br/> | <span data-ttu-id="69886-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="69886-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="69886-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69886-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="69886-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69886-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69886-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="69886-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69886-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69886-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="69886-133">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="69886-133">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="69886-134">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="69886-134">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




