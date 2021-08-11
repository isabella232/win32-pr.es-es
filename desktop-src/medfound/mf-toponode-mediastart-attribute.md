---
description: Especifica la hora de inicio de la presentación.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: MF_TOPONODE_MEDIASTART atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7efeed2bd34745ffda4e756c8b43894bd51fc287ded5cba0ecf0ffb323713754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244426"
---
# <a name="mf_toponode_mediastart-attribute"></a>Atributo \_ MF TOPONODE \_ MEDIASTART

Especifica la hora de inicio de la presentación.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como un **valor LONGLONG.**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Comentarios

Este atributo especifica la posición en el origen donde se inicia la reproducción, en unidades de 100 nanosegundos, en relación con el inicio del origen. Si el atributo no está establecido, la reproducción se inicia en cero (el inicio del archivo). Por ejemplo, para iniciar la reproducción en la marca de 5 segundos, establezca este atributo en 50000000. Establezca el atributo en los nodos de origen de la topología (nodos con el tipo igual a **MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Establezca el atributo antes de llamar [**a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Si inserta manualmente un descodificador en la topología, también debe establecer los atributos [MF \_ TOPONODE \_ MARKIN \_ HERE](mf-toponode-markin-here-attribute.md) y [MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) en el nodo descodificador.

 

Este atributo es un valor con firma, aunque se almacena como **UINT64.** Sin embargo, los valores negativos no son significativos.

La constante GUID de este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tiempos de presentación de secuencia](sequence-presentation-times.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




