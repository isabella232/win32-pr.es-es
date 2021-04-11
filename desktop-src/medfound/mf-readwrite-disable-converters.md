---
description: Habilita o deshabilita las conversiones de formato por el lector de origen o el escritor del receptor.
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: MF_READWRITE_DISABLE_CONVERTERS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8532c45ca3aeb272fa6b6ef422e0d82e40bd3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279044"
---
# <a name="mf_readwrite_disable_converters-attribute"></a><span data-ttu-id="3ef25-103">MF \_ ReadWrite \_ Disable \_ Converters (atributo)</span><span class="sxs-lookup"><span data-stu-id="3ef25-103">MF\_READWRITE\_DISABLE\_CONVERTERS attribute</span></span>

<span data-ttu-id="3ef25-104">Habilita o deshabilita las conversiones de formato por el lector de origen o el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="3ef25-104">Enables or disables format conversions by the source reader or sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ef25-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3ef25-105">Data type</span></span>

<span data-ttu-id="3ef25-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3ef25-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3ef25-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="3ef25-107">Get/set</span></span>

<span data-ttu-id="3ef25-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3ef25-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3ef25-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3ef25-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ef25-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ef25-110">Remarks</span></span>

<span data-ttu-id="3ef25-111">De forma predeterminada, el lector de origen y el escritor del receptor pueden realizar algunas conversiones de formato en secuencias de audio y vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="3ef25-111">By default, the source reader and sink writer can perform some format conversions on uncompressed audio and video streams.</span></span> <span data-ttu-id="3ef25-112">Para deshabilitar este comportamiento, establezca este atributo en **true** al crear el lector de origen o el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="3ef25-112">To disable this behavior, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="3ef25-113">Utilice este atributo con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="3ef25-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="3ef25-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="3ef25-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="3ef25-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="3ef25-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="3ef25-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="3ef25-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="3ef25-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="3ef25-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="3ef25-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="3ef25-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="3ef25-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ef25-119">Requirements</span></span>



| <span data-ttu-id="3ef25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ef25-120">Requirement</span></span> | <span data-ttu-id="3ef25-121">Value</span><span class="sxs-lookup"><span data-stu-id="3ef25-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef25-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ef25-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ef25-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="3ef25-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="3ef25-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ef25-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ef25-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3ef25-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3ef25-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ef25-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ef25-127"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef25-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ef25-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ef25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef25-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ef25-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ef25-130">Atributos del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="3ef25-130">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ef25-131">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="3ef25-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




