---
description: Contiene el cuadro de Descripción del ejemplo para un archivo MP4 o 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: MF_MT_MPEG4_SAMPLE_DESCRIPTION atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912162"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a><span data-ttu-id="b9ffb-103">\_Atributo de \_ \_ Descripción de muestra MPEG4 \_ de MF MT</span><span class="sxs-lookup"><span data-stu-id="b9ffb-103">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute</span></span>

<span data-ttu-id="b9ffb-104">Contiene el cuadro de Descripción del ejemplo para un archivo MP4 o 3GP.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-104">Contains the sample description box for an MP4 or 3GP file.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9ffb-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b9ffb-105">Data type</span></span>

<span data-ttu-id="b9ffb-106">**BYTES\[\]**</span><span class="sxs-lookup"><span data-stu-id="b9ffb-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="b9ffb-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b9ffb-107">Get/set</span></span>

<span data-ttu-id="b9ffb-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="b9ffb-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="b9ffb-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="b9ffb-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b9ffb-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="b9ffb-110">Applies to</span></span>

[<span data-ttu-id="b9ffb-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b9ffb-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b9ffb-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9ffb-112">Remarks</span></span>

<span data-ttu-id="b9ffb-113">El cuadro Descripción del ejemplo describe la codificación utilizada para una secuencia en el archivo.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-113">The sample description box describes the encoding used for a stream in the file.</span></span>

<span data-ttu-id="b9ffb-114">El origen de archivo MPEG-4 establece este atributo en el tipo de medio para cada flujo.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-114">The MPEG-4 file source sets this attribute on the media type for each stream.</span></span> <span data-ttu-id="b9ffb-115">El valor del atributo son los datos sin procesar en el cuadro Descripción del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-115">The value of the attribute is the raw data in the sample description box.</span></span> <span data-ttu-id="b9ffb-116">Si el origen de archivo MPEG-4 puede analizar la descripción del ejemplo, también agrega los detalles del formato al tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-116">If the MPEG-4 file source can parse the sample description, it also adds the format details to the media type.</span></span> <span data-ttu-id="b9ffb-117">De lo contrario, la aplicación o el descodificador deben analizar la descripción del ejemplo del atributo de Descripción del ejemplo de MF \_ MT \_ MPEG4 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9ffb-117">Otherwise, the application or the decoder must parse the sample description from the MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute.</span></span>

<span data-ttu-id="b9ffb-118">Al establecer este atributo en el receptor MPEG-4 a través del método [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , los datos del atributo MF \_ MT \_ MPEG4 \_ Sample \_ Description no deben cambiar después de que se hayan enviado una o varias muestras al receptor en la interfaz [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) de la secuencia correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-118">When setting this attribute on MPEG-4 sink through [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) method, the data for the attribute MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION should not change after one or more samples have been sent to the sink on the corresponding stream's [**IMFStreamSink::ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) interface.</span></span>

<span data-ttu-id="b9ffb-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ffb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9ffb-120">Requirements</span></span>



| <span data-ttu-id="b9ffb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ffb-121">Requirement</span></span> | <span data-ttu-id="b9ffb-122">Value</span><span class="sxs-lookup"><span data-stu-id="b9ffb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ffb-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9ffb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ffb-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="b9ffb-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b9ffb-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9ffb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ffb-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b9ffb-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b9ffb-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9ffb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9ffb-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ffb-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ffb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9ffb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ffb-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9ffb-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9ffb-131">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="b9ffb-131">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




