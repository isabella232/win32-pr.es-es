---
description: Contiene un puntero a la interfaz de devolución de llamada de aplicaciones para el escritor del receptor.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: MF_SINK_WRITER_ASYNC_CALLBACK atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817782"
---
# <a name="mf_sink_writer_async_callback-attribute"></a><span data-ttu-id="66c9b-103">\_Atributo de \_ devolución de \_ llamada asincrónica de escritor de receptor MF \_</span><span class="sxs-lookup"><span data-stu-id="66c9b-103">MF\_SINK\_WRITER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="66c9b-104">Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="66c9b-104">Contains a pointer to the application's callback interface for the sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="66c9b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="66c9b-105">Data type</span></span>

<span data-ttu-id="66c9b-106">**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ almacenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="66c9b-106">**[**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="66c9b-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="66c9b-107">Get/set</span></span>

<span data-ttu-id="66c9b-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="66c9b-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="66c9b-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="66c9b-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="66c9b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66c9b-110">Remarks</span></span>

<span data-ttu-id="66c9b-111">El valor de este atributo es un puntero a la interfaz [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66c9b-111">The value of this attribute is a pointer to the application's [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) interface.</span></span>

<span data-ttu-id="66c9b-112">Utilice este atributo con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="66c9b-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="66c9b-113">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="66c9b-113">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="66c9b-114">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="66c9b-114">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="66c9b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66c9b-115">Requirements</span></span>



| <span data-ttu-id="66c9b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c9b-116">Requirement</span></span> | <span data-ttu-id="66c9b-117">Value</span><span class="sxs-lookup"><span data-stu-id="66c9b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c9b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66c9b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="66c9b-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="66c9b-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="66c9b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66c9b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="66c9b-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="66c9b-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="66c9b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66c9b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="66c9b-123"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="66c9b-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66c9b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="66c9b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c9b-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66c9b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66c9b-126">Atributos del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="66c9b-126">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




