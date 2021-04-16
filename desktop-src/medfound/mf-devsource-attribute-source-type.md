---
description: Especifica un tipo de dispositivo, como captura de audio o captura de vídeo.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705747"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a><span data-ttu-id="44221-103">Atributo \_ de \_ \_ tipo de origen de atributo MF DEVSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="44221-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE attribute</span></span>

<span data-ttu-id="44221-104">Especifica el tipo de un dispositivo, como captura de audio o captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="44221-104">Specifies a device's type, such as audio capture or video capture.</span></span>

## <a name="data-type"></a><span data-ttu-id="44221-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="44221-105">Data type</span></span>

<span data-ttu-id="44221-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="44221-106">**GUID**</span></span>

<span data-ttu-id="44221-107">Se definen los siguientes valores para este atributo:</span><span class="sxs-lookup"><span data-stu-id="44221-107">The following values are defined for this attribute:</span></span>



| <span data-ttu-id="44221-108">Value</span><span class="sxs-lookup"><span data-stu-id="44221-108">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="44221-109">Significado</span><span class="sxs-lookup"><span data-stu-id="44221-109">Meaning</span></span>                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <span data-ttu-id="44221-110"><dt>**\_tipo de origen del atributo MF DEVSOURCE \_ \_ \_ \_ \_ GUID AUDCAP**</dt></span><span class="sxs-lookup"><span data-stu-id="44221-110"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="44221-111">Dispositivo de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="44221-111">Audio capture device.</span></span><br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <span data-ttu-id="44221-112"><dt>**\_tipo de origen de atributo MF DEVSOURCE de \_ \_ \_ \_ VIDCAP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="44221-112"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="44221-113">Dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="44221-113">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="44221-114">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="44221-114">Get/set</span></span>

<span data-ttu-id="44221-115">Para obtener este atributo, llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="44221-115">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="44221-116">Para establecer este atributo, llame a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="44221-116">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="44221-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44221-117">Remarks</span></span>

<span data-ttu-id="44221-118">Utilice este atributo como entrada para las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="44221-118">Use this attribute as input to the following functions:</span></span>

-   [<span data-ttu-id="44221-119">**MFCreateDeviceSource**</span><span class="sxs-lookup"><span data-stu-id="44221-119">**MFCreateDeviceSource**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [<span data-ttu-id="44221-120">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="44221-120">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="44221-121">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="44221-121">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="44221-122">Además, este atributo se establece en los objetos de activación devueltos por la función [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="44221-122">In addition, this attribute is set on the activation objects returned by the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span>

<span data-ttu-id="44221-123">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="44221-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="44221-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44221-124">Requirements</span></span>



| <span data-ttu-id="44221-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="44221-125">Requirement</span></span> | <span data-ttu-id="44221-126">Value</span><span class="sxs-lookup"><span data-stu-id="44221-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44221-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44221-127">Minimum supported client</span></span><br/> | <span data-ttu-id="44221-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="44221-128">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="44221-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44221-129">Minimum supported server</span></span><br/> | <span data-ttu-id="44221-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="44221-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="44221-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44221-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="44221-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44221-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44221-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="44221-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44221-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44221-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44221-135">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="44221-135">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="44221-136">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="44221-136">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




