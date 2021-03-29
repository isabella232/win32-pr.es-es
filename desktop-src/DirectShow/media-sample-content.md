---
description: Describe el contenido de una secuencia elemental dentro de una secuencia de transporte MPEG-2. Esta enumeración se usa en la interfaz IMPEG2PIDMap, que se implementa en los terminales de salida del demultiplexador MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: Enumeración MEDIA_SAMPLE_CONTENT (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679211"
---
# <a name="media_sample_content-enumeration"></a><span data-ttu-id="da4aa-104">\_Enumeración de contenido de ejemplo multimedia \_</span><span class="sxs-lookup"><span data-stu-id="da4aa-104">MEDIA\_SAMPLE\_CONTENT enumeration</span></span>

<span data-ttu-id="da4aa-105">Describe el contenido de una secuencia elemental dentro de una secuencia de transporte MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="da4aa-105">Describes the contents of an elementary stream within an MPEG-2 transport stream.</span></span> <span data-ttu-id="da4aa-106">Esta enumeración se usa en la interfaz [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , que se implementa en los terminales de salida del [demultiplexador MPEG-2](mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="da4aa-106">This enumeration is used in the [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) interface, which is implemented on the output pins of the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da4aa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da4aa-107">Syntax</span></span>


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a><span data-ttu-id="da4aa-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="da4aa-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da4aa-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_paquete de transporte de medios \_**</span><span class="sxs-lookup"><span data-stu-id="da4aa-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**MEDIA\_TRANSPORT\_PACKET**</span></span>
</dt> <dd>

<span data-ttu-id="da4aa-110">Especifica un paquete de flujo de transporte completo que se pasará sin procesar.</span><span class="sxs-lookup"><span data-stu-id="da4aa-110">Specifies a complete transport stream packet to be passed through without processing.</span></span>

</dd> <dt>

<span data-ttu-id="da4aa-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_secuencia básica de medios \_**</span><span class="sxs-lookup"><span data-stu-id="da4aa-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA\_ELEMENTARY\_STREAM**</span></span>
</dt> <dd>

<span data-ttu-id="da4aa-112">Especifica una carga de PE de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="da4aa-112">Specifies an audio or video PES payload.</span></span>

</dd> <dt>

<span data-ttu-id="da4aa-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ PSI**</span><span class="sxs-lookup"><span data-stu-id="da4aa-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA\_MPEG2\_PSI**</span></span>
</dt> <dd>

<span data-ttu-id="da4aa-114">Especifica un flujo de datos de PAT, PMT, CAT o Private.</span><span class="sxs-lookup"><span data-stu-id="da4aa-114">Specifies a PAT, PMT, CAT, or Private data stream.</span></span> <span data-ttu-id="da4aa-115">Se trata de secciones de PSI completas que no es necesario reensamblar.</span><span class="sxs-lookup"><span data-stu-id="da4aa-115">These are complete PSI sections which do not need to be reassembled.</span></span>

</dd> <dt>

<span data-ttu-id="da4aa-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_carga de transporte multimedia \_**</span><span class="sxs-lookup"><span data-stu-id="da4aa-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**MEDIA\_TRANSPORT\_PAYLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="da4aa-117">Especifica las cargas de paquetes de TS recopiladas, como paquetes de PES.</span><span class="sxs-lookup"><span data-stu-id="da4aa-117">Specifies gathered TS packet payloads, such as PES packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da4aa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da4aa-118">Requirements</span></span>



| <span data-ttu-id="da4aa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="da4aa-119">Requirement</span></span> | <span data-ttu-id="da4aa-120">Value</span><span class="sxs-lookup"><span data-stu-id="da4aa-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da4aa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da4aa-121">Header</span></span><br/> | <dl> <span data-ttu-id="da4aa-122"><dt>Bdatypes. h (incluye Bdaiface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da4aa-122"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4aa-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="da4aa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4aa-124">Tipos enumerados de DirectShow</span><span class="sxs-lookup"><span data-stu-id="da4aa-124">DirectShow Enumerated Types</span></span>](directshow-enumerated-types.md)
</dt> </dl>

 

 




