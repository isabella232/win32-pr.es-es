---
description: Especifica el identificador del punto de conexión de un dispositivo de captura de audio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699411"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a><span data-ttu-id="d9aa1-103">\_Tipo de origen de atributo MF DEVSOURCE \_ \_ \_ Type \_ AUDCAP \_ Endpoint \_ ID</span><span class="sxs-lookup"><span data-stu-id="d9aa1-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="d9aa1-104">Especifica el identificador del punto de conexión de un dispositivo de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="d9aa1-104">Specifies the endpoint ID for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9aa1-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d9aa1-105">Data type</span></span>

<span data-ttu-id="d9aa1-106">**WCHAR\***</span><span class="sxs-lookup"><span data-stu-id="d9aa1-106">**WCHAR\***</span></span>

## <a name="getset"></a><span data-ttu-id="d9aa1-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="d9aa1-107">Get/set</span></span>

<span data-ttu-id="d9aa1-108">Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="d9aa1-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="d9aa1-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="d9aa1-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9aa1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9aa1-110">Remarks</span></span>

<span data-ttu-id="d9aa1-111">El valor del atributo es un identificador de extremo.</span><span class="sxs-lookup"><span data-stu-id="d9aa1-111">The value of the attribute is an endpoint ID.</span></span> <span data-ttu-id="d9aa1-112">Este atributo se utiliza con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="d9aa1-112">This attribute is used with the following functions:</span></span>

-   <span data-ttu-id="d9aa1-113">Se puede usar como entrada para las funciones [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) y [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="d9aa1-113">It can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="d9aa1-114">En este contexto, el atributo especifica el dispositivo de captura de audio para la función.</span><span class="sxs-lookup"><span data-stu-id="d9aa1-114">In this context, the attribute specifies the audio capture device for the function.</span></span> <span data-ttu-id="d9aa1-115">Puede obtener el identificador de punto de conexión para un dispositivo determinado llamando al método [**IMMDevice:: getId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) .</span><span class="sxs-lookup"><span data-stu-id="d9aa1-115">You can get the endpoint ID for a given device by calling the [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method.</span></span> <span data-ttu-id="d9aa1-116">Consulte la documentación de la API de audio básica para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d9aa1-116">See the Core Audio API documentation for more information.</span></span>
-   <span data-ttu-id="d9aa1-117">Cuando la función [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) enumera los dispositivos de audio, los objetos de activación devueltos contienen este atributo.</span><span class="sxs-lookup"><span data-stu-id="d9aa1-117">When the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function enumerates audio devices, the returned activation objects contain this attribute.</span></span> <span data-ttu-id="d9aa1-118">El objeto de activación usa el atributo internamente cuando crea el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d9aa1-118">The attribute is used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="d9aa1-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d9aa1-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9aa1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9aa1-120">Requirements</span></span>



| <span data-ttu-id="d9aa1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9aa1-121">Requirement</span></span> | <span data-ttu-id="d9aa1-122">Value</span><span class="sxs-lookup"><span data-stu-id="d9aa1-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9aa1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9aa1-123">Header</span></span><br/> | <dl> <span data-ttu-id="d9aa1-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9aa1-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9aa1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9aa1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9aa1-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9aa1-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9aa1-127">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="d9aa1-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="d9aa1-128">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9aa1-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
