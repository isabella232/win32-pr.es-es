---
description: Habilita el procesamiento de baja latencia en la canalización de Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815510"
---
# <a name="mf_low_latency-attribute"></a><span data-ttu-id="9a00f-103">\_Atributo de baja \_ latencia MF</span><span class="sxs-lookup"><span data-stu-id="9a00f-103">MF\_LOW\_LATENCY attribute</span></span>

<span data-ttu-id="9a00f-104">Habilita el procesamiento de baja latencia en la canalización de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9a00f-104">Enables low-latency processing in the Microsoft Media Foundation pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="9a00f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9a00f-105">Data type</span></span>

<span data-ttu-id="9a00f-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="9a00f-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9a00f-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="9a00f-107">Get/set</span></span>

<span data-ttu-id="9a00f-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9a00f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9a00f-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9a00f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a00f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a00f-110">Remarks</span></span>

<span data-ttu-id="9a00f-111">La baja latencia se define como el menor retraso posible desde el momento en que se generan (o reciben) los datos multimedia cuando se representan.</span><span class="sxs-lookup"><span data-stu-id="9a00f-111">Low latency is defined as the smallest possible delay from when the media data is generated (or received) to when it is rendered.</span></span> <span data-ttu-id="9a00f-112">La latencia baja es conveniente para escenarios de comunicación en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="9a00f-112">Low latency is desirable for real-time communication scenarios.</span></span> <span data-ttu-id="9a00f-113">En otros escenarios, como la reproducción local o la transcodificación, normalmente no debe habilitar el modo de baja latencia, ya que puede afectar a la calidad.</span><span class="sxs-lookup"><span data-stu-id="9a00f-113">For other scenarios, such as local playback or transcoding, you typically should not enable low-latency mode, because it can affect quality.</span></span>

> [!Note]  
> <span data-ttu-id="9a00f-114">El valor GUID de este atributo es idéntico a la [propiedad \_ AVLowLatencyMode de CODECAPI](codecapi-avlowlatencymode.md) definida para la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="9a00f-114">The GUID value of this attribute is identical to the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) property defined for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>

 

<span data-ttu-id="9a00f-115">Establezca este atributo en los componentes de canalización de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9a00f-115">Set this attribute on pipeline components as follows:</span></span>

-   <span data-ttu-id="9a00f-116">Origen de medios: Use el método [**IMFMediaSourceEx:: GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="9a00f-116">Media source: Use the [**IMFMediaSourceEx::GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) method.</span></span>
-   <span data-ttu-id="9a00f-117">Media Foundation Transform (MFT): Use el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="9a00f-117">Media Foundation transform (MFT): Use the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="9a00f-118">En el caso de los codificadores, el codificador podría admitir latencia baja a través de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="9a00f-118">For encoders, the encoder might support low latency through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
-   <span data-ttu-id="9a00f-119">Receptor de medios: Consulte el receptor de medios para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="9a00f-119">Media sink: Query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="9a00f-120">Normalmente, las aplicaciones no establecen este atributo directamente en los componentes de canalización, sino que establecen el atributo en uno de los siguientes objetos:</span><span class="sxs-lookup"><span data-stu-id="9a00f-120">Applications typically do not set this attribute directly on the pipeline components, but instead set the attribute on one of the following objects:</span></span>

-   <span data-ttu-id="9a00f-121">[Sesión de medios](media-session.md): Use el parámetro *pConfiguation* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , o bien establezca el atributo en la topología.</span><span class="sxs-lookup"><span data-stu-id="9a00f-121">[Media Session](media-session.md): Use the *pConfiguation* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function, or else set the attribute on the topology.</span></span>
-   <span data-ttu-id="9a00f-122">[Lector de origen](source-reader.md): establezca el atributo con las propiedades de configuración al crear el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="9a00f-122">[Source Reader](source-reader.md): Set the attribute with the configuration properties when you create the Source Reader.</span></span> <span data-ttu-id="9a00f-123">Para obtener más información, vea [atributos del lector de código fuente](source-reader-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9a00f-123">For more information, see [Source Reader Attributes](source-reader-attributes.md).</span></span>
-   <span data-ttu-id="9a00f-124">[Escritor de receptor](sink-writer.md): establezca el atributo con las propiedades de configuración al crear el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="9a00f-124">[Sink Writer](sink-writer.md): Set the attribute with the configuration properties when you create the Sink Writer.</span></span> <span data-ttu-id="9a00f-125">Para obtener más información, vea [atributos del escritor de receptor](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9a00f-125">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a00f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a00f-126">Requirements</span></span>



| <span data-ttu-id="9a00f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a00f-127">Requirement</span></span> | <span data-ttu-id="9a00f-128">Value</span><span class="sxs-lookup"><span data-stu-id="9a00f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a00f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a00f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9a00f-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="9a00f-130">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9a00f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a00f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9a00f-132">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="9a00f-132">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9a00f-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a00f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a00f-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a00f-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a00f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a00f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a00f-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9a00f-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a00f-137">Atributos del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="9a00f-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a00f-138">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="9a00f-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a00f-139">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="9a00f-139">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
