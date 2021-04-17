---
description: Especifica si un origen de captura de vídeo es un dispositivo de hardware o un dispositivo de software.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648259"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a><span data-ttu-id="a19b9-103">Tipo de origen de atributo de MF \_ DEVSOURCE \_ atributo de origen de \_ \_ \_ HW de VIDCAP \_ \_</span><span class="sxs-lookup"><span data-stu-id="a19b9-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_HW\_SOURCE attribute</span></span>

<span data-ttu-id="a19b9-104">Especifica si un origen de captura de vídeo es un dispositivo de hardware o un dispositivo de software.</span><span class="sxs-lookup"><span data-stu-id="a19b9-104">Specifies whether a video capture source is a hardware device or a software device.</span></span>

## <a name="data-type"></a><span data-ttu-id="a19b9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a19b9-105">Data type</span></span>

<span data-ttu-id="a19b9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a19b9-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a19b9-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="a19b9-107">Get/set</span></span>

<span data-ttu-id="a19b9-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a19b9-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a19b9-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a19b9-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="a19b9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a19b9-110">Remarks</span></span>

<span data-ttu-id="a19b9-111">Si el valor es **true**, el origen de captura es un dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="a19b9-111">If the value is **TRUE**, the capture source is a hardware device.</span></span> <span data-ttu-id="a19b9-112">Si el valor es **false**, se trata de un dispositivo de software.</span><span class="sxs-lookup"><span data-stu-id="a19b9-112">If the value is **FALSE**, it is a software device.</span></span> <span data-ttu-id="a19b9-113">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a19b9-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="a19b9-114">Este atributo se establece en los objetos de activación devueltos por las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="a19b9-114">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="a19b9-115">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="a19b9-115">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="a19b9-116">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="a19b9-116">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="a19b9-117">El atributo solo se aplica a los dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a19b9-117">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="a19b9-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a19b9-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a19b9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a19b9-119">Requirements</span></span>



| <span data-ttu-id="a19b9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a19b9-120">Requirement</span></span> | <span data-ttu-id="a19b9-121">Value</span><span class="sxs-lookup"><span data-stu-id="a19b9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a19b9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a19b9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a19b9-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a19b9-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a19b9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a19b9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a19b9-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a19b9-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a19b9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a19b9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a19b9-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a19b9-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a19b9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a19b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a19b9-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a19b9-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a19b9-130">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="a19b9-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="a19b9-131">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a19b9-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




