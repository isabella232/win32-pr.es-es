---
description: Valor del campo \# &0034;c-playerversion&0034; que el origen de red usa para \# el registro.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: MFNETSOURCE_PLAYERVERSION propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468667"
---
# <a name="mfnetsource_playerversion-property"></a>Propiedad MFNETSOURCE \_ PLAYERVERSION

Valor del campo "c-playerversion" que usa el origen de red para el registro. Las aplicaciones pueden establecer esta propiedad en el número de versión de la aplicación.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**LONGLONG**

VT \_ I8

**hVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PLAYERVERSION** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Solucionador de origen.](source-resolver.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Registro de cliente](client-logging.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




