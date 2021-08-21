---
description: Especifica el valor de configuración para el localizador de proxy predeterminado.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: MFNETSOURCE_PROXYSETTINGS propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6af82b593899eb504818ff041c6c6839c4cca1b18ea29218f7259c41b4df9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738680"
---
# <a name="mfnetsource_proxysettings-property"></a>Propiedad MFNETSOURCE \_ PROXYSETTINGS

Especifica el valor de configuración para el localizador de proxy predeterminado. El valor de esta propiedad es un miembro de la [**enumeración MFNET \_ PROXYSETTINGS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings)



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PROXYSETTINGS** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy predeterminado. Para establecer la propiedad , pase un **puntero IPropertyStore** en el *parámetro pProxyConfig* de la [**función MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)

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

 

 




