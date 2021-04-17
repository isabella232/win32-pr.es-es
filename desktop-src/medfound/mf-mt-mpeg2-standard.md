---
description: Para un tipo de medio que describe una secuencia de programa MPEG-2 (PS) o una secuencia de transporte (TS), especifica el estándar que se usa para multiplexar la secuencia.
ms.assetid: 3D4C1A81-A9BA-427F-93DB-F522A0616EAB
title: MF_MT_MPEG2_STANDARD atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0650a68975f449ea938b41872005e11d79922393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648320"
---
# <a name="mf_mt_mpeg2_standard-attribute"></a><span data-ttu-id="1385e-103">\_Atributo estándar de MF MT \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="1385e-103">MF\_MT\_MPEG2\_STANDARD attribute</span></span>

<span data-ttu-id="1385e-104">Para un tipo de medio que describe una secuencia de programa MPEG-2 (PS) o una secuencia de transporte (TS), especifica el estándar que se usa para multiplexar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1385e-104">For a media type that describes an MPEG-2 program stream (PS) or transport stream (TS), specifies the standard that is used to multiplex the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="1385e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1385e-105">Data type</span></span>

<span data-ttu-id="1385e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1385e-106">**UINT32**</span></span>



| <span data-ttu-id="1385e-107">Value</span><span class="sxs-lookup"><span data-stu-id="1385e-107">Value</span></span>                                                                                                | <span data-ttu-id="1385e-108">Significado</span><span class="sxs-lookup"><span data-stu-id="1385e-108">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="1385e-109"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="1385e-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="1385e-110">Estándar MPEG-2 PS o TS.</span><span class="sxs-lookup"><span data-stu-id="1385e-110">Standard MPEG-2 PS or TS.</span></span><br/>                                       |
| <span id="1"></span><dl> <span data-ttu-id="1385e-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1385e-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1385e-112">Estándar del Comité de sistemas de televisión avanzada (ATSC).</span><span class="sxs-lookup"><span data-stu-id="1385e-112">Advanced Television Systems Committee (ATSC) standard.</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="1385e-113"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1385e-113"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1385e-114">Estándar de difusión de vídeo digital (DVB).</span><span class="sxs-lookup"><span data-stu-id="1385e-114">Digital Video Broadcasting (DVB) standard.</span></span><br/>                      |
| <span id="3"></span><dl> <span data-ttu-id="1385e-115"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="1385e-115"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="1385e-116">Asociación del estándar de industrias y empresas de radio (ARIB).</span><span class="sxs-lookup"><span data-stu-id="1385e-116">Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1385e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1385e-117">Requirements</span></span>



| <span data-ttu-id="1385e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1385e-118">Requirement</span></span> | <span data-ttu-id="1385e-119">Value</span><span class="sxs-lookup"><span data-stu-id="1385e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1385e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1385e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1385e-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="1385e-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1385e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1385e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1385e-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1385e-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1385e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1385e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1385e-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1385e-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1385e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1385e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1385e-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1385e-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




