---
description: Especifica el rol de dispositivo para un dispositivo de captura de audio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082350"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a><span data-ttu-id="4b10d-103">Tipo de origen de atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ \_ rol AUDCAP</span><span class="sxs-lookup"><span data-stu-id="4b10d-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ROLE attribute</span></span>

<span data-ttu-id="4b10d-104">Especifica el rol de dispositivo para un dispositivo de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="4b10d-104">Specifies the device role for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="4b10d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4b10d-105">Data type</span></span>

<span data-ttu-id="4b10d-106">**ERole** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4b10d-106">**ERole** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4b10d-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="4b10d-107">Get/set</span></span>

<span data-ttu-id="4b10d-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4b10d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4b10d-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4b10d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b10d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b10d-110">Remarks</span></span>

<span data-ttu-id="4b10d-111">El tipo de enumeración **eRole** se documenta en la documentación básica de la API de audio.</span><span class="sxs-lookup"><span data-stu-id="4b10d-111">The **eRole** enumeration type is documented in the Core Audio API documentation.</span></span>

<span data-ttu-id="4b10d-112">El valor del atributo especifica un rol de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4b10d-112">The value of the attribute specifies a device role.</span></span> <span data-ttu-id="4b10d-113">Este atributo se utiliza con las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="4b10d-113">This attribute is used with the following functions.</span></span>

<span data-ttu-id="4b10d-114">Este atributo se puede usar como entrada para las funciones [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) y [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="4b10d-114">This attribute can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="4b10d-115">Si se especifica el atributo, la función crea un origen de medios que usa el dispositivo de captura de audio predeterminado para el rol de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4b10d-115">If the attribute is specified, the function creates a media source that uses the default audio capture device for the specified device role.</span></span>

<span data-ttu-id="4b10d-116">Este atributo también se puede usar como entrada para la función [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="4b10d-116">This attribute can also be used as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="4b10d-117">Si se especifica el atributo, la enumeración se restringe al rol de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4b10d-117">If the attribute is specified, the enumeration is restricted to the specified device role.</span></span> <span data-ttu-id="4b10d-118">Además, cada objeto de activación devuelto por la función **MFEnumDeviceSources** contiene este atributo.</span><span class="sxs-lookup"><span data-stu-id="4b10d-118">In addition, each activation object returned by the **MFEnumDeviceSources** function contains this attribute.</span></span> <span data-ttu-id="4b10d-119">El objeto de activación usa el atributo internamente al crear el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="4b10d-119">The attribute is then used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="4b10d-120">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4b10d-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b10d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b10d-121">Requirements</span></span>



| <span data-ttu-id="4b10d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b10d-122">Requirement</span></span> | <span data-ttu-id="4b10d-123">Value</span><span class="sxs-lookup"><span data-stu-id="4b10d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b10d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b10d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4b10d-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b10d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b10d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b10d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4b10d-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b10d-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4b10d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b10d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b10d-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b10d-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b10d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b10d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b10d-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b10d-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b10d-132">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="4b10d-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="4b10d-133">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4b10d-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




