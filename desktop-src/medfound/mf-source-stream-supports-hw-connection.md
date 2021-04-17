---
description: Indica si un origen multimedia admite el flujo de datos de hardware.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716670"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a><span data-ttu-id="0d5f5-103">El \_ flujo de origen MF \_ admite el atributo de \_ \_ conexión de HW \_</span><span class="sxs-lookup"><span data-stu-id="0d5f5-103">MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="0d5f5-104">Indica si un origen multimedia admite el flujo de datos de hardware.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-104">Indicates whether a media source supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d5f5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0d5f5-105">Data type</span></span>

<span data-ttu-id="0d5f5-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="0d5f5-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0d5f5-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d5f5-107">Remarks</span></span>

<span data-ttu-id="0d5f5-108">Este atributo se usa cuando un origen de medios sirve como proxy para un dispositivo de hardware y puede transferir datos de nivel inferior a través de un bus de hardware, sin enviar datos a la CPU.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-108">This attribute is used when a media source proxies a hardware device and is able to transfer data downstream over a hardware bus, without sending data up to the CPU.</span></span> <span data-ttu-id="0d5f5-109">Por ejemplo, una cámara web puede proporcionar vídeo codificado en H. 264 directamente a un descodificador de hardware integrado.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-109">For example, a webcam might deliver H.264-encoded video directly to an integrated hardware decoder.</span></span>

<span data-ttu-id="0d5f5-110">En este escenario, el origen y el descodificador todavía se representan en el Microsoft Media Foundation por un objeto de [origen de medios](media-sources.md) y una [transformación de Media Foundation](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="0d5f5-110">In this scenario, the source and decoder are still represented in the Microsoft Media Foundation by a [media source](media-sources.md) object and a [Media Foundation transform](media-foundation-transforms.md) (MFT).</span></span> <span data-ttu-id="0d5f5-111">Sin embargo, los datos no fluyen entre estos dos objetos en la capa de canalización, solo en el nivel de hardware, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![diagrama que muestra un origen de proxy de hardware.](images/proxy-mft3.png)

<span data-ttu-id="0d5f5-113">La conexión entre el origen del medio y el MFT se negocia como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-113">The connection between the media source and the MFT is negotiated as follows.</span></span>

1.  <span data-ttu-id="0d5f5-114">La canalización consulta el origen de los medios para la interfaz [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="0d5f5-114">The pipeline queries the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span> <span data-ttu-id="0d5f5-115">(Esta interfaz es opcional para admitir los orígenes multimedia).</span><span class="sxs-lookup"><span data-stu-id="0d5f5-115">(This interface is optional for media sources to support.)</span></span>
2.  <span data-ttu-id="0d5f5-116">La canalización llama a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="0d5f5-116">The pipeline calls [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
3.  <span data-ttu-id="0d5f5-117">Las consultas de canalización para el \_ flujo de origen MF \_ \_ admiten el atributo de \_ \_ conexión HW.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-117">The pipeline queries for the MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="0d5f5-118">Si el atributo está presente y es igual a **true**, el origen de medios admite conexiones de hardware.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-118">If the attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="0d5f5-119">La canalización comprueba si la MFT es también un proxy de hardware, comprobando el atributo de [ \_ \_ \_ \_ atributo de dirección URL de hardware de enumeración MFT](mft-enum-hardware-url-attribute.md) en la MFT.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-119">The pipeline checks if the MFT is also a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="0d5f5-120">Para obtener más información, consulte [hardware MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="0d5f5-120">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
5.  <span data-ttu-id="0d5f5-121">La canalización establece el atributo de [ \_ \_ \_ atributo Stream conectado de MFT](mft-connected-stream-attribute.md) en MFT.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-121">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="0d5f5-122">El valor de este atributo es el puntero [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) obtenido del origen multimedia en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-122">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer obtained from the media source in step 2.</span></span>
6.  <span data-ttu-id="0d5f5-123">La canalización establece el atributo [MFT \_ conectado \_ a \_ HW \_ Stream](mft-connected-to-hw-stream.md) en **true** tanto en el origen multimedia como en el MFT.</span><span class="sxs-lookup"><span data-stu-id="0d5f5-123">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the media source and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5f5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d5f5-124">Requirements</span></span>



| <span data-ttu-id="0d5f5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d5f5-125">Requirement</span></span> | <span data-ttu-id="0d5f5-126">Value</span><span class="sxs-lookup"><span data-stu-id="0d5f5-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5f5-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d5f5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0d5f5-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="0d5f5-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0d5f5-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d5f5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0d5f5-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0d5f5-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0d5f5-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d5f5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d5f5-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f5-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d5f5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d5f5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5f5-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d5f5-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d5f5-135">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="0d5f5-135">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> </dl>

 

 




