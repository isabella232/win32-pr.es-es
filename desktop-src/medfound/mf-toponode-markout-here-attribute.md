---
description: Especifica si la canalización aplica el marcado en este nodo. El marcado es el punto en el que finaliza una presentación. Si los componentes de canalización generan datos más allá del punto de la marca de salida, los datos no se representan.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: MF_TOPONODE_MARKOUT_HERE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715381"
---
# <a name="mf_toponode_markout_here-attribute"></a>MF \_ TOPONODE \_ MARKOUT \_ aquí atributo

Especifica si la canalización aplica el marcado en este nodo. El marcado es el punto en el que finaliza una presentación. Si los componentes de canalización generan datos más allá del punto de la marca de salida, los datos no se representan.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se aplica a todos los tipos de nodo.

Si este atributo es **true**, la canalización Media Foundation recorta los ejemplos de salida de este nodo para que coincidan con la hora de detención de la presentación. El cargador de topología establece este atributo cuando resuelve una topología. La mayoría de las aplicaciones no necesitan establecer ni recuperar este atributo.

Se recomienda que un nodo de cada rama de la topología tenga este atributo establecido en **true**. Una rama de topología se define como la ruta de acceso desde un nodo de origen a un nodo de salida. Dentro de una bifurcación, \_ \_ \_ se deben establecer en el mismo nodo de la bifurcación los atributos MF TOPONODE MARKOUT aquí y [MF \_ TOPONODE \_ Marka \_ aquí](mf-toponode-markin-here-attribute.md) . No se pueden establecer en nodos diferentes dentro de la misma rama.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**\_TOPONODE MF \_ \_ aquí**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




