---
description: Indica si un receptor de medios admite el flujo de datos de hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: MF_STREAM_SINK_SUPPORTS_HW_CONNECTION atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497657"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a><span data-ttu-id="34d93-103">El \_ receptor de Stream MF \_ admite el atributo de \_ \_ conexión de HW \_</span><span class="sxs-lookup"><span data-stu-id="34d93-103">MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="34d93-104">Indica si un receptor de medios admite el flujo de datos de hardware.</span><span class="sxs-lookup"><span data-stu-id="34d93-104">Indicates whether a media sink supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="34d93-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="34d93-105">Data type</span></span>

<span data-ttu-id="34d93-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="34d93-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="34d93-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34d93-107">Remarks</span></span>

<span data-ttu-id="34d93-108">Este atributo se usa cuando un receptor de medios envía un proxy a un dispositivo de hardware y puede recibir datos a través de un bus de hardware.</span><span class="sxs-lookup"><span data-stu-id="34d93-108">This attribute is used when a media sink proxies a hardware device and is able to receive data over a hardware bus.</span></span> <span data-ttu-id="34d93-109">Por ejemplo, un descodificador de audio de hardware podría enviar datos de audio directamente al hardware de representación de audio.</span><span class="sxs-lookup"><span data-stu-id="34d93-109">For example, a hardware audio decoder might send audio data directly to the audio rendering hardware.</span></span>

<span data-ttu-id="34d93-110">En este escenario, el descodificador y el receptor todavía se representan en el Microsoft Media Foundation mediante una [transformación de Media Foundation](media-foundation-transforms.md) (MFT) y un receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="34d93-110">In this scenario, the decoder and the sink are still represented in the Microsoft Media Foundation by a [Media Foundation transform](media-foundation-transforms.md) (MFT) and a media sink.</span></span> <span data-ttu-id="34d93-111">Sin embargo, los datos no fluyen entre estos dos objetos en la capa de canalización, solo en el nivel de hardware, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="34d93-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![diagrama que muestra un origen de proxy de hardware.](images/proxy-mft4.png)

<span data-ttu-id="34d93-113">La conexión entre la MFT y el receptor multimedia se negocia como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="34d93-113">The connection between the MFT and the media sink is negotiated as follows.</span></span>

1.  <span data-ttu-id="34d93-114">La canalización comprueba si MFT es un proxy de hardware, comprobando el atributo de [ \_ \_ \_ \_ atributo de dirección URL de hardware de enumeración MFT](mft-enum-hardware-url-attribute.md) en la MFT.</span><span class="sxs-lookup"><span data-stu-id="34d93-114">The pipeline checks if the MFT is a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="34d93-115">Para obtener más información, consulte [hardware MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="34d93-115">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="34d93-116">La canalización obtiene un puntero a la interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del receptor de la secuencia en el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="34d93-116">The pipeline gets a pointer to the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface of the stream sink on the media sink.</span></span>
3.  <span data-ttu-id="34d93-117">La canalización usa el puntero [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) para consultar el receptor de la \_ secuencia MF \_ \_ compatible con el atributo de conexión de \_ HW \_ .</span><span class="sxs-lookup"><span data-stu-id="34d93-117">The pipeline uses the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer to query for the MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="34d93-118">Si este atributo está presente y es igual a **true**, el origen de medios admite conexiones de hardware.</span><span class="sxs-lookup"><span data-stu-id="34d93-118">If this attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="34d93-119">La canalización establece el atributo de [ \_ \_ \_ atributo Stream conectado de MFT](mft-connected-stream-attribute.md) en el receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="34d93-119">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the stream sink.</span></span> <span data-ttu-id="34d93-120">El valor de este atributo es el puntero [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) desde la MFT.</span><span class="sxs-lookup"><span data-stu-id="34d93-120">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer from the MFT.</span></span>
5.  <span data-ttu-id="34d93-121">La canalización establece el atributo [MFT \_ conectado \_ a \_ HW \_ Stream](mft-connected-to-hw-stream.md) en **true** en el receptor de la secuencia y en la MFT.</span><span class="sxs-lookup"><span data-stu-id="34d93-121">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the stream sink and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="34d93-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34d93-122">Requirements</span></span>



| <span data-ttu-id="34d93-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="34d93-123">Requirement</span></span> | <span data-ttu-id="34d93-124">Value</span><span class="sxs-lookup"><span data-stu-id="34d93-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34d93-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34d93-125">Minimum supported client</span></span><br/> | <span data-ttu-id="34d93-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="34d93-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="34d93-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34d93-127">Minimum supported server</span></span><br/> | <span data-ttu-id="34d93-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="34d93-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="34d93-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34d93-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="34d93-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="34d93-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34d93-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="34d93-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d93-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34d93-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




