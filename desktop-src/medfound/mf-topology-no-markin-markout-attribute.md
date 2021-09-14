---
description: Especifica si la canalización recorta muestras.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: MF_TOPOLOGY_NO_MARKIN_MARKOUT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361153"
---
# <a name="mf_topology_no_markin_markout-attribute"></a>ATRIBUTO \_ MF TOPOLOGY \_ NO \_ \_ MARKIN MARKOUT

Especifica si la canalización recorta muestras.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Observaciones

De forma predeterminada, la canalización recorta ejemplos para que coincidan con los tiempos de presentación correctos. El recorte se realiza en los nodos de topología que tienen los atributos [**MF \_ TOPONODE \_ MARKIN \_ HERE**](mf-toponode-markin-here-attribute.md) y [**MF \_ TOPONODE \_ MARKOUT \_ HERE.**](mf-toponode-markout-here-attribute.md) Si el atributo **MF \_ TOPOLOGY \_ NO \_ MARKIN \_ MARKOUT** se establece en **TRUE** en la topología, la canalización no recorta ejemplos y los atributos **MF \_ TOPONODE \_ MARKIN \_ HERE** y **MF \_ TOPONODE \_ MARKOUT \_ HERE** se omiten. Si el atributo no está establecido o tiene el valor **FALSE,** la canalización recorta ejemplos.

Una aplicación podría establecer el atributo **MF \_ TOPOLOGY \_ NO \_ MARKIN \_ MARKOUT** en **TRUE** si la aplicación recibe muestras comprimidas de la canalización y necesita obtener todos los fotogramas clave, que de lo contrario podrían recortarse.

El valor predeterminado de este atributo es **FALSE.**

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKIN \_ AQUÍ**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKOUT \_ AQUÍ**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




