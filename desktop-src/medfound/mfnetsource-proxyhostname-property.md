---
description: Especifica el nombre de host del servidor proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: MFNETSOURCE_PROXYHOSTNAME propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574872"
---
# <a name="mfnetsource_proxyhostname-property"></a>Propiedad MFNETSOURCE \_ PROXYHOSTNAME

Especifica el nombre de host del servidor proxy.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Cadena de caracteres anchos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PROXYHOSTNAME** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el localizador de proxy predeterminado al crear el objeto de localizador de proxy. Para establecer la propiedad , pase un **puntero IPropertyStore** en el *parámetro pProxyConfig* de la [**función MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) La aplicación debe establecer esta propiedad cuando el localizador de proxy está configurado para funcionar en modo manual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Compatibilidad con proxy para orígenes de red](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




