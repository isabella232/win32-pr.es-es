---
description: Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica que los paquetes de transporte contienen un código de tiempo de 4 bytes.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: MF_MT_MPEG2_TIMECODE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277689"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a><span data-ttu-id="671b5-103">\_Atributo de \_ código de tiempo MF MT MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="671b5-103">MF\_MT\_MPEG2\_TIMECODE attribute</span></span>

<span data-ttu-id="671b5-104">Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica que los paquetes de transporte contienen un código de tiempo de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="671b5-104">For a media type that describes an MPEG-2 transport stream (TS), specifies the transport packets contain a 4-byte time code.</span></span>

## <a name="data-type"></a><span data-ttu-id="671b5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="671b5-105">Data type</span></span>

<span data-ttu-id="671b5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="671b5-106">**UINT32**</span></span>



| <span data-ttu-id="671b5-107">Value</span><span class="sxs-lookup"><span data-stu-id="671b5-107">Value</span></span>                                                                                                | <span data-ttu-id="671b5-108">Significado</span><span class="sxs-lookup"><span data-stu-id="671b5-108">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="671b5-109"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="671b5-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="671b5-110">No se agrega código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="671b5-110">No time code is added.</span></span><br/>                                                                                                              |
| <span id="1"></span><dl> <span data-ttu-id="671b5-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="671b5-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="671b5-112">Se agrega un código de tiempo de 4 bytes al principio de cada paquete de transporte.</span><span class="sxs-lookup"><span data-stu-id="671b5-112">A 4-byte time code is added at the start of each transport packet.</span></span> <span data-ttu-id="671b5-113">Este código de tiempo es necesario para algunos estándares de televisión digital.</span><span class="sxs-lookup"><span data-stu-id="671b5-113">This time code is required by some digital television standards.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="671b5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671b5-114">Requirements</span></span>



| <span data-ttu-id="671b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="671b5-115">Requirement</span></span> | <span data-ttu-id="671b5-116">Value</span><span class="sxs-lookup"><span data-stu-id="671b5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="671b5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="671b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="671b5-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="671b5-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="671b5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="671b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="671b5-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="671b5-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="671b5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="671b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="671b5-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="671b5-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671b5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="671b5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671b5-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="671b5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




