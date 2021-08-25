---
description: Especifica si el transporte TCP está habilitado para el origen de red.
ms.assetid: ba655505-dcac-4cea-8ad5-ccd1b55ee9d4
title: MFNETSOURCE_ENABLE_TCP propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcd5fe37ab423bd48af8aad45bdbb5c2b09b2d9b4b59fd40d85429d1fa1913ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954811"
---
# <a name="mfnetsource_enable_tcp-property"></a>Propiedad MFNETSOURCE \_ ENABLE \_ TCP

Especifica si el transporte TCP está habilitado para el origen de red.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Booleano (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos admitidos](supported-protocols.md)
</dt> </dl>

 

 




