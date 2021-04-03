---
description: Duración máxima de la transmisión por secuencias acelerada, en milisegundos, en que el origen de red utiliza el transporte UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: Propiedad MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083327"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a>\_Propiedad MAXUDPACCELERATEDSTREAMINGDURATION de MFNETSOURCE

Duración máxima de la transmisión por secuencias acelerada, en milisegundos, en que el origen de red utiliza el transporte UDP.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**DWORD** (almacenado como **Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

En el transporte UDP, esta propiedad invalida la propiedad [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) si el valor de esta propiedad es inferior.

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

El valor predeterminado de esta propiedad es 8.000 milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




