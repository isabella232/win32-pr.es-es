---
description: Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica si los paquetes de transporte contienen encabezados de paquetes de contenido.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: MF_MT_MPEG2_CONTENT_PACKET atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911190"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a><span data-ttu-id="ab4ac-103">\_Atributo de \_ \_ paquete de contenido MF MT MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="ab4ac-103">MF\_MT\_MPEG2\_CONTENT\_PACKET attribute</span></span>

<span data-ttu-id="ab4ac-104">Para un tipo de medio que describe una secuencia de transporte MPEG-2 (TS), especifica si los paquetes de transporte contienen encabezados de paquetes de contenido.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-104">For a media type that describes an MPEG-2 transport stream (TS), specifies whether the transport packets contain Content Packet headers.</span></span>

## <a name="data-type"></a><span data-ttu-id="ab4ac-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ab4ac-105">Data type</span></span>

<span data-ttu-id="ab4ac-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ab4ac-106">**UINT32**</span></span>



| <span data-ttu-id="ab4ac-107">Value</span><span class="sxs-lookup"><span data-stu-id="ab4ac-107">Value</span></span>                                                                                                | <span data-ttu-id="ab4ac-108">Significado</span><span class="sxs-lookup"><span data-stu-id="ab4ac-108">Meaning</span></span>                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="ab4ac-109"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="ab4ac-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="ab4ac-110">No se agregan encabezados de paquetes de contenido.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-110">No Content Packet headers are added.</span></span><br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <span data-ttu-id="ab4ac-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ab4ac-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ab4ac-112">A intervalos de 200 a 1.000 milisegundos, se agrega un encabezado de paquete de contenido de 14 bytes al principio del paquete de transporte, tal como se define en la Asociación del estándar de industrias y empresas de radio (ARIB).</span><span class="sxs-lookup"><span data-stu-id="ab4ac-112">At 200–1000 millisecond intervals, a 14-byte Content Packet header is added to the beginning of the transport packet, as defined by the Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ab4ac-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab4ac-113">Requirements</span></span>



| <span data-ttu-id="ab4ac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab4ac-114">Requirement</span></span> | <span data-ttu-id="ab4ac-115">Value</span><span class="sxs-lookup"><span data-stu-id="ab4ac-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab4ac-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab4ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab4ac-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="ab4ac-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ab4ac-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab4ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab4ac-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="ab4ac-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ab4ac-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab4ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab4ac-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab4ac-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab4ac-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab4ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab4ac-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab4ac-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




