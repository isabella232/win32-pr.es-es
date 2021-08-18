---
description: Especifica si la canalización aplica el mark-in en este nodo.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: MF_TOPONODE_MARKIN_HERE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c105dae6792e995e281309d2b693b78a0ec01e67c4412dc6d62056df09ebe9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874882"
---
# <a name="mf_toponode_markin_here-attribute"></a>Atributo MF \_ TOPONODE \_ MARKIN \_ HERE

Especifica si la canalización aplica el mark-in en este nodo. Mark-in es el punto en el que se inicia una presentación. Si los componentes de canalización generan datos antes del punto de entrada, los datos no se representan.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

> [!Note]  
> La mayoría de las aplicaciones no necesitan usar este atributo. La [sesión multimedia](media-session.md) establece automáticamente este atributo si es necesario.

 

Este atributo se aplica a todos los tipos de nodo. Si el atributo es **TRUE,** la canalización Media Foundation recorta los ejemplos de salida de este nodo para que coincidan con la hora de inicio de la presentación. El cargador de topologías establece este atributo cuando resuelve una topología.

Se recomienda que exactamente un nodo de cada rama de la topología tenga este atributo establecido en **TRUE.** Una rama de topología se define como la ruta de acceso de un nodo de origen a un nodo de salida. Dentro de una rama, los atributos [MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) y MF TOPONODE MARKIN HERE deben establecerse en el mismo \_ \_ nodo de la \_ rama. No se pueden establecer en nodos diferentes dentro de la misma rama.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKOUT \_ AQUÍ**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




