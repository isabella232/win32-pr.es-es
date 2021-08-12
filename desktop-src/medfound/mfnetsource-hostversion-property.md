---
description: Valor del campo &\# 0034;c-hostexever&0034; que el origen de red usa para \# el registro.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: MFNETSOURCE_HOSTVERSION propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5f78a277de4fc5b0609be31f21f684357806dbb8609657a930cdc4816b1e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243465"
---
# <a name="mfnetsource_hostversion-property"></a>Propiedad MFNETSOURCE \_ HOSTVERSION

Valor del campo "c-hostexever" que usa el origen de red para el registro. Las aplicaciones pueden establecer esta propiedad en el número de versión de la aplicación host. La aplicación host es el .exe identificado por el campo c-hostexe.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**LONGLONG**

VT \_ I8

**hVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ HOSTVERSION** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador Source. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Registro de cliente](client-logging.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




