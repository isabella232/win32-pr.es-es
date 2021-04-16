---
description: Contiene la marca de tiempo de descodificación (DTS) para el ejemplo.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: MFSampleExtension_DecodeTimestamp atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696684"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a><span data-ttu-id="a5800-103">\_Atributo DecodeTimestamp de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="a5800-103">MFSampleExtension\_DecodeTimestamp attribute</span></span>

<span data-ttu-id="a5800-104">Contiene la marca de tiempo de descodificación (DTS) para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a5800-104">Contains the decode time stamp (DTS) for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5800-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a5800-105">Data type</span></span>

<span data-ttu-id="a5800-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a5800-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5800-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5800-107">Remarks</span></span>

<span data-ttu-id="a5800-108">El valor del atributo es el DTS en unidades 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="a5800-108">The value of the attribute is the DTS in 100-nanosecond units.</span></span> <span data-ttu-id="a5800-109">El DTS se define en algunos estándares de codificación, incluido MPEG.</span><span class="sxs-lookup"><span data-stu-id="a5800-109">The DTS is defined in some encoding standards, including MPEG.</span></span> <span data-ttu-id="a5800-110">El DTS especifica cuándo se debe descodificar la imagen codificada.</span><span class="sxs-lookup"><span data-stu-id="a5800-110">The DTS specifies when the encoded picture should be decoded.</span></span> <span data-ttu-id="a5800-111">Si el vídeo codificado contiene fotogramas B, el DTS puede diferir del tiempo de presentación, ya que las imágenes B aparecen fuera del orden temporal en el fragmentada.</span><span class="sxs-lookup"><span data-stu-id="a5800-111">If the encoded video contains B frames, the DTS can differ from the presentation time, because B pictures appear out of temporal order in the bitstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5800-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5800-112">Requirements</span></span>



| <span data-ttu-id="a5800-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5800-113">Requirement</span></span> | <span data-ttu-id="a5800-114">Value</span><span class="sxs-lookup"><span data-stu-id="a5800-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5800-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5800-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a5800-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="a5800-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a5800-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5800-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a5800-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="a5800-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a5800-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5800-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5800-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5800-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5800-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5800-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5800-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5800-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5800-123">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5800-123">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




