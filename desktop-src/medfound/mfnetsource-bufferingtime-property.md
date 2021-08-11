---
description: Número de segundos de datos que el origen de red almacena en búfer durante el inicio.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: MFNETSOURCE_BUFFERINGTIME propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6de79344913d77a30dc05dcad4e4f8dd3608e0d35009b1d8e5254e08790993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243812"
---
# <a name="mfnetsource_bufferingtime-property"></a>Propiedad MFNETSOURCE \_ BUFFERINGTIME

Número de segundos de datos que el origen de red almacena en búfer durante el inicio.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**DWORD** (almacenado como **LONG)**

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ BUFFERINGTIME** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El valor predeterminado de esta propiedad es 5 segundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




