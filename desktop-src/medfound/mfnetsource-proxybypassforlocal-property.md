---
description: Especifica si el localizador de proxy debe usar un servidor proxy para las direcciones locales.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: MFNETSOURCE_PROXYBYPASSFORLOCAL propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1de60371ac71e570b9c11abcbc255e20efe1793884ebb0746834d32a34353006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954795"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>MFNETSOURCE \_ PROXYBYPASSFORLOCAL, propiedad

Especifica si el localizador de proxy debe usar un servidor proxy para las direcciones locales.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Booleano (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy. Para establecer la propiedad , pase un **puntero IPropertyStore** en el *parámetro pProxyConfig* de la [**función MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) El valor debe establecerse en 0 si el servidor proxy se va a usar para las direcciones locales; De lo contrario, un valor distinto de cero configura el localizador de proxy predeterminado para omitir el servidor proxy para las direcciones locales.

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

[Compatibilidad con proxy para orígenes de red](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




