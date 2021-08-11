---
description: Especifica si el transporte del Protocolo de datagramas de usuario (UDP) está habilitado en el origen de red.
ms.assetid: d46a59e6-8abc-484b-aecc-edf57ffff512
title: MFNETSOURCE_ENABLE_UDP propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e86078fc836e2a75dd3e5aed238fd09a1f5a00f6442a761c38111a3c87762c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243578"
---
# <a name="mfnetsource_enable_udp-property"></a>Propiedad ENABLE UDP de MFNETSOURCE \_ \_

Especifica si el transporte del Protocolo de datagramas de usuario (UDP) está habilitado en el origen de red.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Booleano (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ ENABLE \_ UDP** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

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

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos admitidos](supported-protocols.md)
</dt> </dl>

 

 




