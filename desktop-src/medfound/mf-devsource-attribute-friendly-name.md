---
description: Especifica el nombre para mostrar de un dispositivo.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696600"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a><span data-ttu-id="0f33e-103">\_Atributo de \_ \_ nombre descriptivo de atributo MF DEVSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="0f33e-103">MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME attribute</span></span>

<span data-ttu-id="0f33e-104">Especifica el nombre para mostrar de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f33e-104">Specifies the display name for a device.</span></span> <span data-ttu-id="0f33e-105">El *nombre para mostrar* es una cadena legible que se puede mostrar en una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0f33e-105">The *display name* is a human-readable string, suitable for display in a user interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="0f33e-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0f33e-106">Data type</span></span>

<span data-ttu-id="0f33e-107">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="0f33e-107">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="0f33e-108">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="0f33e-108">Get/set</span></span>

<span data-ttu-id="0f33e-109">Para obtener este atributo, llame a [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="0f33e-109">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="0f33e-110">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="0f33e-110">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f33e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f33e-111">Remarks</span></span>

<span data-ttu-id="0f33e-112">Este atributo se establece en los objetos de activación devueltos por las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="0f33e-112">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="0f33e-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="0f33e-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="0f33e-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="0f33e-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="0f33e-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0f33e-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f33e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f33e-116">Requirements</span></span>



| <span data-ttu-id="0f33e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f33e-117">Requirement</span></span> | <span data-ttu-id="0f33e-118">Value</span><span class="sxs-lookup"><span data-stu-id="0f33e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f33e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f33e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f33e-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f33e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0f33e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f33e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f33e-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f33e-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0f33e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f33e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f33e-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f33e-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f33e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f33e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f33e-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f33e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0f33e-127">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="0f33e-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="0f33e-128">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0f33e-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




