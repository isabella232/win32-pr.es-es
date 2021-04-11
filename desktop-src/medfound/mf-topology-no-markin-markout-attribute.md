---
description: Especifica si la canalización recorta los ejemplos.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: MF_TOPOLOGY_NO_MARKIN_MARKOUT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275944"
---
# <a name="mf_topology_no_markin_markout-attribute"></a>\_No se pudo \_ marcar el \_ \_ atributo MARKOUT en la topología MF

Especifica si la canalización recorta los ejemplos.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

De forma predeterminada, la canalización recorta los ejemplos para que coincidan con los tiempos de presentación correctos. El recorte se realiza en los nodos de topología que tienen los atributos [**MF \_ TOPONODE \_ avelinot \_ aquí**](mf-toponode-markin-here-attribute.md) y [**MF \_ TOPONODE \_ MARKOUT \_ aquí**](mf-toponode-markout-here-attribute.md) . Si el atributo MF de la **\_ topología \_ no \_ \_ MARKOUT** está establecido en **true** en la topología, la canalización no recorta los ejemplos y se omiten los atributos **MF \_ TOPONODE \_ Avelino \_ here** y **MF \_ TOPONODE \_ MARKOUT \_ aquí** . Si el atributo no está establecido o tiene el valor **false**, la canalización recorta los ejemplos.

Una aplicación puede establecer el atributo de la **\_ topología MF \_ sin \_ Marken \_ MARKOUT** en **true** si la aplicación recibe muestras comprimidas de la canalización y necesita obtener todos los fotogramas clave, que de lo contrario se pueden recortar.

El valor predeterminado de este atributo es **false**.

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

[**\_TOPONODE MF \_ \_ aquí**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKOUT \_ aquí**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




