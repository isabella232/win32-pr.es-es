---
description: Especifica si el lector de origen cierra el origen del medio.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361942"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a><span data-ttu-id="7c83f-103">El \_ \_ lector de origen MF \_ desconecta \_ MEDIASOURCE en el \_ \_ atributo Shutdown</span><span class="sxs-lookup"><span data-stu-id="7c83f-103">MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute</span></span>

<span data-ttu-id="7c83f-104">Especifica si el [lector de origen](source-reader.md) cierra el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="7c83f-104">Specifies whether the [Source Reader](source-reader.md) shuts down the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c83f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7c83f-105">Data type</span></span>

<span data-ttu-id="7c83f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7c83f-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7c83f-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="7c83f-107">Get/set</span></span>

<span data-ttu-id="7c83f-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7c83f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7c83f-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7c83f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c83f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c83f-110">Remarks</span></span>

<span data-ttu-id="7c83f-111">Este atributo solo se aplica cuando la aplicación crea el lector de origen a partir de un objeto de origen multimedia existente, ya sea llamando a [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) o llamando a [**IMFReadWriteClassFactory:: CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span><span class="sxs-lookup"><span data-stu-id="7c83f-111">This attribute applies only when the application creates the source reader from an existing media source object, either by calling [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) or by calling [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span></span>

<span data-ttu-id="7c83f-112">De forma predeterminada, cuando la aplicación libera el lector de origen, el lector de origen cierra el origen del medio llamando a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="7c83f-112">By default, when the application releases the source reader, the source reader shuts down the media source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span> <span data-ttu-id="7c83f-113">En ese momento, la aplicación ya no puede usar el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="7c83f-113">At that point, the application can no longer use the media source.</span></span>

<span data-ttu-id="7c83f-114">Sin embargo, si el \_ \_ atributo del lector de origen MF \_ desconectar \_ MEDIASOURCE \_ al cerrar el \_ atributo es **true**, el lector de origen no apaga el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="7c83f-114">However, if the MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is **TRUE**, the source reader does not shut down the media source.</span></span> <span data-ttu-id="7c83f-115">Esto significa que la aplicación todavía puede usar el origen de medios una vez que la aplicación libera el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="7c83f-115">That means the application can still use the media source after the application releases the source reader.</span></span> <span data-ttu-id="7c83f-116">También significa que la aplicación es responsable de llamar a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="7c83f-116">It also means the application is responsible for calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>

<span data-ttu-id="7c83f-117">Si la aplicación crea el lector de origen a partir de una dirección URL o de una secuencia de bytes, el lector de origen siempre cierra el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="7c83f-117">If the application creates the source reader from a URL or from a byte stream, the source reader always shuts down the media source.</span></span> <span data-ttu-id="7c83f-118">\_ \_ \_ En este caso, se omite el atributo del lector de código de MF desconectar \_ MEDIASOURCE \_ al \_ cerrar.</span><span class="sxs-lookup"><span data-stu-id="7c83f-118">The MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is ignored in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c83f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c83f-119">Requirements</span></span>



| <span data-ttu-id="7c83f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c83f-120">Requirement</span></span> | <span data-ttu-id="7c83f-121">Value</span><span class="sxs-lookup"><span data-stu-id="7c83f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c83f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c83f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c83f-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c83f-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7c83f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c83f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c83f-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c83f-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7c83f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c83f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c83f-127"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c83f-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c83f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c83f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c83f-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c83f-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c83f-130">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="7c83f-130">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="7c83f-131">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="7c83f-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




