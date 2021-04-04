---
description: Contiene un puntero a la interfaz de devolución de llamada de aplicaciones para el lector de origen.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: MF_SOURCE_READER_ASYNC_CALLBACK atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277682"
---
# <a name="mf_source_reader_async_callback-attribute"></a><span data-ttu-id="26b53-103">\_Atributo de \_ devolución de \_ llamada Async del lector de origen MF \_</span><span class="sxs-lookup"><span data-stu-id="26b53-103">MF\_SOURCE\_READER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="26b53-104">Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el [lector de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="26b53-104">Contains a pointer to the application's callback interface for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="26b53-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="26b53-105">Data type</span></span>

<span data-ttu-id="26b53-106">**IMFSourceReaderCallback \** _ almacenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="26b53-106">**IMFSourceReaderCallback\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="26b53-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="26b53-107">Get/set</span></span>

<span data-ttu-id="26b53-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="26b53-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="26b53-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="26b53-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="26b53-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26b53-110">Remarks</span></span>

<span data-ttu-id="26b53-111">El valor de este atributo es un puntero a la interfaz [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="26b53-111">The value of this attribute is a pointer to the application's [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) interface.</span></span>

<span data-ttu-id="26b53-112">Utilice este atributo con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="26b53-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="26b53-113">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="26b53-113">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="26b53-114">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="26b53-114">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="26b53-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="26b53-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a><span data-ttu-id="26b53-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26b53-116">Requirements</span></span>



| <span data-ttu-id="26b53-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b53-117">Requirement</span></span> | <span data-ttu-id="26b53-118">Value</span><span class="sxs-lookup"><span data-stu-id="26b53-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="26b53-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26b53-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26b53-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="26b53-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="26b53-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26b53-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26b53-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="26b53-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="26b53-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26b53-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="26b53-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b53-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b53-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="26b53-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b53-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26b53-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26b53-127">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="26b53-127">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="26b53-128">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="26b53-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




