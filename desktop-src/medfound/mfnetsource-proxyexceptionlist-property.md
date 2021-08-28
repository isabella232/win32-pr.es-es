---
description: Especifica una lista delimitada por punto y coma de servidores multimedia que pueden aceptar conexiones de aplicaciones cliente sin usar un servidor proxy.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: MFNETSOURCE_PROXYEXCEPTIONLIST propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e87c07068d31cdd5e9762dab14e2a61edbe9c8f90f8750acc1b23c851ad47c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113495"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a>Propiedad MFNETSOURCE \_ PROXYEXCEPTIONLIST

Especifica una lista delimitada por punto y coma de servidores multimedia que pueden aceptar conexiones de aplicaciones cliente sin usar un servidor proxy.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Cadena de caracteres anchos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy. Para establecer la propiedad , pase un **puntero IPropertyStore** en el *parámetro pProxyConfig* de la [**función MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) El localizador de proxy no realiza la detección de proxy para estas direcciones.

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

 

 




