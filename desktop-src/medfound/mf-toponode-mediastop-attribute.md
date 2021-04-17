---
description: Especifica la hora de detención de la presentación.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: MF_TOPONODE_MEDIASTOP atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5b763d1d5adabc520900dde6839d1599ddcb3d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717383"
---
# <a name="mf_toponode_mediastop-attribute"></a>\_ \_ Atributo MEDIASTOP de MF TOPONODE

Especifica la hora de detención de la presentación.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Trata como un valor de **LONGLONG** .

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Observaciones

Este atributo especifica la posición en el origen donde se detiene la reproducción, en unidades de 100-nanosegundos, con respecto al inicio del origen. Si no se establece el atributo, la reproducción se detiene al final del origen. Por ejemplo, para detener la reproducción en la marca de 5 segundos, establezca este atributo en 50 millones. Establezca el atributo en los nodos de origen de la topología (nodos con el tipo igual a la **\_ topología MF \_ SOURCESTREAM \_ nodo**). Establezca el atributo antes de llamar a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Si inserta manualmente un descodificador en la topología, también debe establecer los atributos [MF \_ TOPONODE \_ avelinot \_ aquí](mf-toponode-markin-here-attribute.md) y [MF \_ TOPONODE \_ MARKOUT \_ aquí](mf-toponode-markout-here-attribute.md) en el nodo descodificador.

 

Una vez establecida la topología, el establecimiento de este atributo no tiene ningún efecto.

Este atributo es un valor con signo, aunque se almacena como **UINT64**. Sin embargo, los valores negativos no son significativos.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tiempos de presentación de secuencia](sequence-presentation-times.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




