---
description: Especifica si la canalización aplica la marca de salida en este nodo. Mark-out es el punto en el que finaliza una presentación. Si los componentes de canalización generan datos más allá del punto de marcado, los datos no se representan.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: MF_TOPONODE_MARKOUT_HERE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7196fd9f0ccc342672b609ce32d922d091a3f962ef9dd8e9dcdd4077c34a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691126"
---
# <a name="mf_toponode_markout_here-attribute"></a>Atributo MF \_ TOPONODE \_ MARKOUT \_ HERE

Especifica si la canalización aplica la marca de salida en este nodo. Mark-out es el punto en el que finaliza una presentación. Si los componentes de canalización generan datos más allá del punto de marcado, los datos no se representan.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Este atributo se aplica a todos los tipos de nodo.

Si este atributo es **TRUE**, la canalización Media Foundation recorta los ejemplos de salida de este nodo para que coincidan con la hora de detenerse de la presentación. El cargador de topologías establece este atributo cuando resuelve una topología. La mayoría de las aplicaciones no necesitan establecer ni recuperar este atributo.

Se recomienda que exactamente un nodo de cada rama de la topología tenga este atributo establecido en **TRUE.** Una rama de topología se define como la ruta de acceso de un nodo de origen a un nodo de salida. Dentro de una rama, los atributos MF \_ TOPONODE MARKOUT HERE y \_ \_ MF [ \_ TOPONODE \_ MARKIN \_ HERE](mf-toponode-markin-here-attribute.md) deben establecerse en el mismo nodo de la rama. No se pueden establecer en nodos diferentes dentro de la misma rama.

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

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKIN \_ AQUÍ**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




