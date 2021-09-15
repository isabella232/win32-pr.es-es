---
description: Especifica la hora de detenerse de la presentación.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: MF_TOPONODE_MEDIASTOP atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5b763d1d5adabc520900dde6839d1599ddcb3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574885"
---
# <a name="mf_toponode_mediastop-attribute"></a>Atributo \_ MF TOPONODE \_ MEDIASTOP

Especifica la hora de detenerse de la presentación.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como un **valor LONGLONG.**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Observaciones

Este atributo especifica la posición en el origen donde se detiene la reproducción, en unidades de 100 nanosegundos, con respecto al inicio del origen. Si el atributo no está establecido, la reproducción se detiene al final del origen. Por ejemplo, para detener la reproducción en la marca de 5 segundos, establezca este atributo en 50000000. Establezca el atributo en los nodos de origen de la topología (nodos con el tipo igual a **MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Establezca el atributo antes de llamar [**a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Si inserta manualmente un descodificador en la topología, también debe establecer los atributos [MF \_ TOPONODE \_ MARKIN \_ HERE](mf-toponode-markin-here-attribute.md) y [MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) en el nodo descodificador.

 

Una vez establecida la topología, establecer este atributo no tiene ningún efecto.

Este atributo es un valor con firma, aunque se almacena como **UINT64.** Sin embargo, los valores negativos no son significativos.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tiempos de presentación de secuencia](sequence-presentation-times.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




