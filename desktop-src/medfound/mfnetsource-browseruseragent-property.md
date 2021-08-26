---
description: Valor de la primera parte del campo \# &0034;cs(User-Agent)&0034; que el origen de red usa para el \# registro.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: MFNETSOURCE_BROWSERUSERAGENT propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf46fde925dbe2d94643a0843d105726f0976ba7a84f47773ef35e32ae8dfde7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954865"
---
# <a name="mfnetsource_browseruseragent-property"></a>Propiedad MFNETSOURCE \_ BROWSERUSERAGENT

Valor de la primera parte del campo "cs(User-Agent)" que el origen de red usa para el registro. Las aplicaciones pueden establecer esta propiedad en cualquier valor de cadena.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Cadena de caracteres anchos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ BROWSERUSERAGENT** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Registro de cliente](client-logging.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[**MFNETSOURCE \_ PLAYERUSERAGENT**](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




