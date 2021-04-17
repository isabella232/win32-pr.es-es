---
description: Especifica si el escritor del receptor limita la velocidad de los datos entrantes.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: MF_SINK_WRITER_DISABLE_THROTTLING atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716952"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a><span data-ttu-id="f6f44-103">\_Atributo de \_ \_ limitación de deshabilitación del escritor de receptor MF \_</span><span class="sxs-lookup"><span data-stu-id="f6f44-103">MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute</span></span>

<span data-ttu-id="f6f44-104">Especifica si el escritor del receptor limita la velocidad de los datos entrantes.</span><span class="sxs-lookup"><span data-stu-id="f6f44-104">Specifies whether the sink writer limits the rate of incoming data.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6f44-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f6f44-105">Data type</span></span>

<span data-ttu-id="f6f44-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6f44-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f6f44-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="f6f44-107">Get/set</span></span>

<span data-ttu-id="f6f44-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f6f44-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f6f44-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f6f44-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6f44-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6f44-110">Remarks</span></span>

<span data-ttu-id="f6f44-111">De forma predeterminada, el método [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) del escritor receptor limita la velocidad de los datos bloqueando el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="f6f44-111">By default, the sink writer's [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method limits the data rate by blocking the calling thread.</span></span> <span data-ttu-id="f6f44-112">Esto evita que la aplicación entregue los ejemplos demasiado rápido.</span><span class="sxs-lookup"><span data-stu-id="f6f44-112">This prevents the application from delivering samples too quickly.</span></span> <span data-ttu-id="f6f44-113">Para deshabilitar este comportamiento, establezca el \_ atributo de limitación del escritor del receptor MF \_ \_ \_ en **true** cuando cree el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="f6f44-113">To disable this behavior, set the MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute to **TRUE** when you create the sink writer.</span></span>

<span data-ttu-id="f6f44-114">Utilice este atributo con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="f6f44-114">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="f6f44-115">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="f6f44-115">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="f6f44-116">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="f6f44-116">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="f6f44-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6f44-117">Requirements</span></span>



| <span data-ttu-id="f6f44-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6f44-118">Requirement</span></span> | <span data-ttu-id="f6f44-119">Value</span><span class="sxs-lookup"><span data-stu-id="f6f44-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f44-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6f44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f44-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="f6f44-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f6f44-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6f44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f44-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f6f44-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f6f44-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6f44-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f44-125"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f44-125"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f44-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6f44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f44-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6f44-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6f44-128">Atributos del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="f6f44-128">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




