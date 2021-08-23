---
description: Describe el contenido de una secuencia elemental dentro de una secuencia de transporte MPEG-2. Esta enumeración se usa en la interfaz IMPEG2PIDMap, que se implementa en los pines de salida del demultiplexor MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: MEDIA_SAMPLE_CONTENT enumeración (Bdatypes.h)
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
ms.openlocfilehash: 1dead22b2c8ea3cf7da665e01a4b36554b8282922a1d2b2a12d59f429f2acac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684995"
---
# <a name="media_sample_content-enumeration"></a>Enumeración \_ MEDIA SAMPLE \_ CONTENT

Describe el contenido de una secuencia elemental dentro de una secuencia de transporte MPEG-2. Esta enumeración se usa en la [**interfaz IMPEG2PIDMap,**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) que se implementa en los pines de salida del [demultiplexor MPEG-2](mpeg-2-demultiplexer.md).

## <a name="syntax"></a>Syntax


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

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**PAQUETE DE \_ TRANSPORTE \_ DE MEDIOS**
</dt> <dd>

Especifica un paquete de flujo de transporte completo que se pasará sin procesar.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA \_ ELEMENTARY \_ STREAM**
</dt> <dd>

Especifica una carga de PES de audio o vídeo.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ PSI**
</dt> <dd>

Especifica un flujo de datos PAT, PMT, CAT o Private. Se trata de secciones PSI completas que no es necesario volver a ensamblar.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**CARGA DE \_ TRANSPORTE \_ DE MEDIOS**
</dt> <dd>

Especifica las cargas de paquetes TS recopilados, como los paquetes PES.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Bdatypes.h (incluir Bdaiface.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Tipos enumerados](directshow-enumerated-types.md)
</dt> </dl>

 

 




