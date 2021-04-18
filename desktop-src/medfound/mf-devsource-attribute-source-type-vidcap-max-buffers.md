---
description: Especifica el número máximo de fotogramas que el origen de captura de vídeo almacenará en búfer.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686970"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a><span data-ttu-id="e23d5-103">\_Tipo de origen de atributo MF DEVSOURCE atributo \_ \_ \_ \_ VIDCAP \_ Max \_ buffers</span><span class="sxs-lookup"><span data-stu-id="e23d5-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_MAX\_BUFFERS attribute</span></span>

<span data-ttu-id="e23d5-104">Especifica el número máximo de fotogramas que el origen de captura de vídeo almacenará en búfer.</span><span class="sxs-lookup"><span data-stu-id="e23d5-104">Specifies the maximum number of frames that the video capture source will buffer.</span></span>

## <a name="data-type"></a><span data-ttu-id="e23d5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e23d5-105">Data type</span></span>

<span data-ttu-id="e23d5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e23d5-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e23d5-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="e23d5-107">Get/set</span></span>

<span data-ttu-id="e23d5-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e23d5-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e23d5-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e23d5-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e23d5-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e23d5-110">Remarks</span></span>

<span data-ttu-id="e23d5-111">De forma predeterminada, el origen de captura de vídeo almacena en búfer un máximo de un fotograma cada vez.</span><span class="sxs-lookup"><span data-stu-id="e23d5-111">By default, the video capture source buffers a maximum of one frame at a time.</span></span> <span data-ttu-id="e23d5-112">Puede aumentar el límite del búfer estableciendo este atributo.</span><span class="sxs-lookup"><span data-stu-id="e23d5-112">You can increase the buffer limit by setting this attribute.</span></span>

<span data-ttu-id="e23d5-113">La manera correcta de establecer este atributo depende de la función que se usa para crear el origen de medios:</span><span class="sxs-lookup"><span data-stu-id="e23d5-113">The correct way to set this attribute depends on the function used to create the media source:</span></span>

-   <span data-ttu-id="e23d5-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): establezca el atributo mediante el parámetro *pAttributes* de la función.</span><span class="sxs-lookup"><span data-stu-id="e23d5-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="e23d5-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): establezca el atributo mediante el parámetro *pAttributes* de la función.</span><span class="sxs-lookup"><span data-stu-id="e23d5-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="e23d5-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): establezca el atributo en el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devuelto por la función.</span><span class="sxs-lookup"><span data-stu-id="e23d5-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Set the attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned by the function.</span></span> <span data-ttu-id="e23d5-117">Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="e23d5-117">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="e23d5-118">El atributo solo se aplica a los dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e23d5-118">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="e23d5-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e23d5-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e23d5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e23d5-120">Requirements</span></span>



| <span data-ttu-id="e23d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e23d5-121">Requirement</span></span> | <span data-ttu-id="e23d5-122">Value</span><span class="sxs-lookup"><span data-stu-id="e23d5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e23d5-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e23d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e23d5-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e23d5-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e23d5-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e23d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e23d5-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e23d5-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e23d5-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e23d5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e23d5-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e23d5-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e23d5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e23d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e23d5-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e23d5-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e23d5-131">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="e23d5-131">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="e23d5-132">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e23d5-132">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




