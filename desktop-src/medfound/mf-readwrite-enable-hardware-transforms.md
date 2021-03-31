---
description: Permite al lector de código fuente o al escritor de receptores usar transformaciones de Media Foundation basadas en hardware (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361100"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a><span data-ttu-id="c941c-103">MF \_ ReadWrite \_ habilitar \_ el \_ atributo de transformaciones de hardware</span><span class="sxs-lookup"><span data-stu-id="c941c-103">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="c941c-104">Permite al lector de código fuente o al escritor de receptores usar transformaciones de Media Foundation basadas en hardware (MFTs).</span><span class="sxs-lookup"><span data-stu-id="c941c-104">Enables the source reader or sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>

## <a name="data-type"></a><span data-ttu-id="c941c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c941c-105">Data type</span></span>

<span data-ttu-id="c941c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c941c-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c941c-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="c941c-107">Get/set</span></span>

<span data-ttu-id="c941c-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c941c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c941c-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c941c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="c941c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c941c-110">Remarks</span></span>

<span data-ttu-id="c941c-111">De forma predeterminada, el lector de origen y el escritor del receptor no usan descodificadores ni codificadores de hardware.</span><span class="sxs-lookup"><span data-stu-id="c941c-111">By default, the source reader and sink writer do not use hardware decoders or encoders.</span></span> <span data-ttu-id="c941c-112">Para habilitar el uso de MFTs de hardware, establezca este atributo en **true** al crear el lector de origen o el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="c941c-112">To enable the use of hardware MFTs, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="c941c-113">Utilice este atributo con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="c941c-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="c941c-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="c941c-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="c941c-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="c941c-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="c941c-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="c941c-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="c941c-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="c941c-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="c941c-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="c941c-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="c941c-119">Existe una excepción al comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c941c-119">There is one exception to the default behavior.</span></span> <span data-ttu-id="c941c-120">El lector de origen y el escritor de receptores usan automáticamente MFTs que se registran localmente en el proceso del llamador.</span><span class="sxs-lookup"><span data-stu-id="c941c-120">The source reader and sink writer automatically use MFTs that are registered locally in the caller's process.</span></span> <span data-ttu-id="c941c-121">Para registrar una MFT localmente, llame a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span><span class="sxs-lookup"><span data-stu-id="c941c-121">To register an MFT locally, call [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span></span> <span data-ttu-id="c941c-122">Los MFTs de hardware que se registran localmente se usan aunque no se haya establecido el atributo **MF \_ ReadWrite \_ habilitar \_ \_ transformaciones de hardware** .</span><span class="sxs-lookup"><span data-stu-id="c941c-122">Hardware MFTs that are registered locally are used even if the **MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS** attribute is not set.</span></span>

<span data-ttu-id="c941c-123">Este atributo no afecta a la descodificación de vídeo acelerado por hardware que usa la aceleración de vídeo de DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="c941c-123">This attribute does not affect hardware-accelerated video decoding that uses DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="c941c-124">Para habilitar la descodificación de DXVA en el lector de origen, establezca el atributo de [Administrador de D3D del \_ lector de origen \_ \_ \_ MF](mf-source-reader-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="c941c-124">To enable DXVA decoding in the source reader, set the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="c941c-125">Si este atributo es **true**, no establezca el atributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) .</span><span class="sxs-lookup"><span data-stu-id="c941c-125">If this attribute is **TRUE**, do not set the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="c941c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c941c-126">Requirements</span></span>



| <span data-ttu-id="c941c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c941c-127">Requirement</span></span> | <span data-ttu-id="c941c-128">Value</span><span class="sxs-lookup"><span data-stu-id="c941c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c941c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c941c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c941c-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="c941c-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c941c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c941c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c941c-132">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c941c-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c941c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c941c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c941c-134"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="c941c-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c941c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c941c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c941c-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c941c-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c941c-137">Atributos del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="c941c-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c941c-138">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="c941c-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




