---
description: El valor del campo &\# 0034; c-playerversion&\# 0034; que usa el origen de red para el registro.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: Propiedad MFNETSOURCE_PLAYERVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817915"
---
# <a name="mfnetsource_playerversion-property"></a>\_Propiedad PLAYERVERSION de MFNETSOURCE

El valor del campo "c-playerversion" que usa el origen de red para el registro. Las aplicaciones pueden establecer esta propiedad en el número de versión de la aplicación.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**LONGLONG**

VT \_ i8

**hVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PLAYERVERSION** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [solucionador de código fuente](source-resolver.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Registro de cliente](client-logging.md)
</dt> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




