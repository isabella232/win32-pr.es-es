---
description: Especifica si el receptor de archivos MPEG-4 filtra el conjunto de parámetros de secuencia (SPS) y el conjunto de parámetros de imagen (PPS) NALUs.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811857"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a><span data-ttu-id="144b8-103">MF \_ MPEG4SINK \_ SPSPPS \_ PASSTHROUGH (atributo)</span><span class="sxs-lookup"><span data-stu-id="144b8-103">MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute</span></span>

<span data-ttu-id="144b8-104">Especifica si el [**receptor de archivos MPEG-4**](mpeg-4-file-sink.md) filtra el conjunto de parámetros de secuencia (SPS) y el conjunto de parámetros de imagen (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="144b8-104">Specifies whether the [**MPEG-4 File Sink**](mpeg-4-file-sink.md) filters out sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

## <a name="data-type"></a><span data-ttu-id="144b8-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="144b8-105">Data type</span></span>

<span data-ttu-id="144b8-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="144b8-106">**BOOL** stored as **UINT32**</span></span>

## <a name="applies-to"></a><span data-ttu-id="144b8-107">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="144b8-107">Applies to</span></span>

[<span data-ttu-id="144b8-108">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="144b8-108">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a><span data-ttu-id="144b8-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="144b8-109">Remarks</span></span>

<span data-ttu-id="144b8-110">El [**receptor de archivos MPEG-4**](mpeg-4-file-sink.md) escribe los parámetros de SPS y PPS en el cuadro Descripción de ejemplo del archivo MP4.</span><span class="sxs-lookup"><span data-stu-id="144b8-110">The [**MPEG-4 File Sink**](mpeg-4-file-sink.md) writes the SPS and PPS parameters into the sample description box of the MP4 file.</span></span> <span data-ttu-id="144b8-111">De forma predeterminada, filtra los SPS y el NALUs de PPS del flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="144b8-111">By default, it filters out the SPS and PPS NALUs from the video stream.</span></span> <span data-ttu-id="144b8-112">Para invalidar este comportamiento, establezca el \_ atributo de paso MF MPEG4SINK \_ SPSPPS \_ en **true**.</span><span class="sxs-lookup"><span data-stu-id="144b8-112">To override this behavior, set the MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="144b8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="144b8-113">Requirements</span></span>



| <span data-ttu-id="144b8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="144b8-114">Requirement</span></span> | <span data-ttu-id="144b8-115">Value</span><span class="sxs-lookup"><span data-stu-id="144b8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="144b8-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="144b8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="144b8-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="144b8-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="144b8-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="144b8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="144b8-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="144b8-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="144b8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="144b8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="144b8-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="144b8-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="144b8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="144b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144b8-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="144b8-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




