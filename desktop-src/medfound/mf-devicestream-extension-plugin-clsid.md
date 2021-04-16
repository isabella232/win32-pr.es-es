---
description: Especifica el CLSID de un complemento de procesamiento posterior para un dispositivo de captura de vídeo.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696602"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a><span data-ttu-id="8f54e-103">\_ \_ \_ Atributo CLSID del complemento de extensión MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="8f54e-103">MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute</span></span>

<span data-ttu-id="8f54e-104">Especifica el CLSID de un complemento de procesamiento posterior para un dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8f54e-104">Specifies the CLSID of a post-processing plug-in for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="8f54e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8f54e-105">Data type</span></span>

<span data-ttu-id="8f54e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8f54e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="8f54e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f54e-107">Remarks</span></span>

<span data-ttu-id="8f54e-108">Un complemento de procesamiento posterior es un MFT que procesa la imagen de vídeo una vez capturada.</span><span class="sxs-lookup"><span data-stu-id="8f54e-108">A post-processing plug-in is an MFT that processes the video image after it is captured.</span></span> <span data-ttu-id="8f54e-109">El fabricante del hardware puede incluir un complemento de procesamiento posterior como parte del paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="8f54e-109">The hardware vendor can include a post-processing plug-in as part of the installation package.</span></span> <span data-ttu-id="8f54e-110">Si es así, el origen de captura de vídeo establece el \_ \_ \_ atributo CLSID del complemento de extensión MF DEVICESTREAM \_ en el CLSID del complemento.</span><span class="sxs-lookup"><span data-stu-id="8f54e-110">If so, the video capture source sets the MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute to the CLSID of the plug-in.</span></span>

<span data-ttu-id="8f54e-111">Para obtener este atributo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8f54e-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="8f54e-112">Consulte el origen de los medios para la interfaz [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="8f54e-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="8f54e-113">Llame a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8f54e-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="8f54e-114">Llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) para obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="8f54e-114">Call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) to get the attribute.</span></span>

<span data-ttu-id="8f54e-115">Para crear el complemento, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="8f54e-115">To create the plug-in, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f54e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f54e-116">Requirements</span></span>



| <span data-ttu-id="8f54e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f54e-117">Requirement</span></span> | <span data-ttu-id="8f54e-118">Value</span><span class="sxs-lookup"><span data-stu-id="8f54e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f54e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f54e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8f54e-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f54e-120">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8f54e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f54e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8f54e-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f54e-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8f54e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f54e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f54e-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f54e-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f54e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f54e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f54e-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f54e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
