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
# <a name="media_sample_content-enumeration"></a>\_Enumeración de contenido de ejemplo multimedia \_

Describe el contenido de una secuencia elemental dentro de una secuencia de transporte MPEG-2. Esta enumeración se usa en la interfaz [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , que se implementa en los terminales de salida del [demultiplexador MPEG-2](mpeg-2-demultiplexer.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_paquete de transporte de medios \_**
</dt> <dd>

Especifica un paquete de flujo de transporte completo que se pasará sin procesar.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_secuencia básica de medios \_**
</dt> <dd>

Especifica una carga de PE de audio o vídeo.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ PSI**
</dt> <dd>

Especifica un flujo de datos de PAT, PMT, CAT o Private. Se trata de secciones de PSI completas que no es necesario reensamblar.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_carga de transporte multimedia \_**
</dt> <dd>

Especifica las cargas de paquetes de TS recopiladas, como paquetes de PES.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Bdatypes. h (incluye Bdaiface. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos enumerados de DirectShow](directshow-enumerated-types.md)
</dt> </dl>

 

 




