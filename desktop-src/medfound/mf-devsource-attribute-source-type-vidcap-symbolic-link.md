---
description: Contiene el vínculo simbólico de un controlador de captura de vídeo.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155568"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a><span data-ttu-id="eb306-103">\_Tipo de origen de atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ vínculo simbólico de VIDCAP \_</span><span class="sxs-lookup"><span data-stu-id="eb306-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute</span></span>

<span data-ttu-id="eb306-104">Contiene el vínculo simbólico de un controlador de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eb306-104">Contains the symbolic link for a video capture driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="eb306-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="eb306-105">Data type</span></span>

<span data-ttu-id="eb306-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="eb306-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="eb306-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="eb306-107">Get/set</span></span>

<span data-ttu-id="eb306-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="eb306-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="eb306-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="eb306-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb306-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb306-110">Remarks</span></span>

<span data-ttu-id="eb306-111">Use este atributo como entrada para la función [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="eb306-111">Use this attribute as input to the [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="eb306-112">Además, este atributo se establece en los objetos de activación devueltos por las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="eb306-112">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="eb306-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="eb306-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="eb306-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="eb306-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="eb306-115">El vínculo simbólico debe considerarse una cadena opaca.</span><span class="sxs-lookup"><span data-stu-id="eb306-115">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="eb306-116">El nombre para mostrar legible de un dispositivo se encuentra en el atributo [de \_ \_ \_ \_ nombre descriptivo de atributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) .</span><span class="sxs-lookup"><span data-stu-id="eb306-116">The human-readable display name for a device is contained in the [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute.</span></span>

<span data-ttu-id="eb306-117">El atributo \_ de \_ tipo de origen del atributo MF DEVSOURCE \_ \_ \_ \_ \_ se puede pasar como el valor del argumento DevicePath de la función [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .</span><span class="sxs-lookup"><span data-stu-id="eb306-117">The MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute can be passed in as the value of the DevicePath argument of the [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) function.</span></span>

<span data-ttu-id="eb306-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="eb306-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb306-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb306-119">Requirements</span></span>



| <span data-ttu-id="eb306-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb306-120">Requirement</span></span> | <span data-ttu-id="eb306-121">Value</span><span class="sxs-lookup"><span data-stu-id="eb306-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb306-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb306-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eb306-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb306-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="eb306-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb306-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eb306-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb306-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="eb306-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb306-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb306-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb306-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb306-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb306-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb306-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb306-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eb306-130">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="eb306-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="eb306-131">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="eb306-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
