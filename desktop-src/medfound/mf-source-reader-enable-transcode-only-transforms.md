---
description: Permite al lector de código fuente usar transformaciones de Media Foundation (MFTs) que están optimizadas para la transcodificación.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541347"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a><span data-ttu-id="5c487-103">\_Lector de código fuente MF \_ \_ Habilitar solo el \_ \_ \_ atributo transformaciones</span><span class="sxs-lookup"><span data-stu-id="5c487-103">MF\_SOURCE\_READER\_ENABLE\_TRANSCODE\_ONLY\_TRANSFORMS attribute</span></span>

<span data-ttu-id="5c487-104">Permite al [lector de código fuente](source-reader.md) usar transformaciones de Media Foundation (MFTs) que están optimizadas para la transcodificación.</span><span class="sxs-lookup"><span data-stu-id="5c487-104">Enables the [Source Reader](source-reader.md) to use Media Foundation transforms (MFTs) that are optimized for transcoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c487-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5c487-105">Data type</span></span>

<span data-ttu-id="5c487-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5c487-106">**UINT32**</span></span>

<span data-ttu-id="5c487-107">Tratar como booleanos.</span><span class="sxs-lookup"><span data-stu-id="5c487-107">Treat as Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c487-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c487-108">Remarks</span></span>

<span data-ttu-id="5c487-109">Algunos MFTs, especialmente los descodificadores, están optimizados para la transcodificación en lugar de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="5c487-109">Some MFTs, particularly decoders, are optimized for transcoding rather than playback.</span></span> <span data-ttu-id="5c487-110">De forma predeterminada, el lector de origen no cargará dichas transformaciones.</span><span class="sxs-lookup"><span data-stu-id="5c487-110">By default, the Source Reader will not load such transforms.</span></span> <span data-ttu-id="5c487-111">Establezca este atributo en **true** si desea usar la transcodificación de MFTs con el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="5c487-111">Set this attribute to **TRUE** if you want to use transcoding MFTs with the Source Reader.</span></span>

<span data-ttu-id="5c487-112">Una aplicación podría establecer este atributo si no procesa los datos en tiempo real (para la transcodificación o escenarios similares).</span><span class="sxs-lookup"><span data-stu-id="5c487-112">An application might set this attribute if it does not process the data in real time (for transcoding or similar scenarios).</span></span> <span data-ttu-id="5c487-113">De lo contrario, para la reproducción en tiempo real, utilice el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5c487-113">Otherwise, for real-time playback, use the default behavior.</span></span>

<span data-ttu-id="5c487-114">Internamente, este atributo hace que el lector de origen incluya la marca de **\_ enumeración de MFT \_ \_ \_ solo Transcode** Flag cuando llama a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="5c487-114">Internally, this attribute causes the Source Reader to include the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when it calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c487-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c487-115">Requirements</span></span>



| <span data-ttu-id="5c487-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c487-116">Requirement</span></span> | <span data-ttu-id="5c487-117">Value</span><span class="sxs-lookup"><span data-stu-id="5c487-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c487-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c487-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5c487-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="5c487-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5c487-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c487-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5c487-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="5c487-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5c487-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c487-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c487-123"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c487-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c487-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c487-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c487-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c487-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c487-126">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="5c487-126">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




