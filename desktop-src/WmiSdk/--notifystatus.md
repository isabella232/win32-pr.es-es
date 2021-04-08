---
description: Actúa como clase primaria para las clases de error definidas por el proveedor.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: __NotifyStatus (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817611"
---
# <a name="__notifystatus-class"></a>\_\_Clase NotifyStatus

La clase de sistema abstracta **\_ \_ NotifyStatus** actúa como clase primaria para las clases de error definidas por el proveedor.

La siguiente sintaxis se simplifica desde el código Managed Object Format (MF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ NotifyStatus** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ NotifyStatus** tiene estas propiedades.

<dl> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contiene un código de error o de información para una operación. Puede ser cualquier código definido por el usuario, pero el valor 0 (cero) normalmente se reserva para indicar que la operación se ha realizado correctamente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Aunque la clase **\_ \_ NotifyStatus** puede ser la clase primaria para las clases de error definidas por el proveedor, se recomienda que los proveedores deriven clases de error de [**\_ \_ ExtendedStatus**](--extendedstatus.md) en su lugar. El uso de **\_ \_ ExtendedStatus** permite una mayor estandarización de las clases de error.

Los proveedores nunca deben crear instancias de **\_ \_ NotifyStatus** directamente, ya que estas instancias no transmiten más información que un código de retorno simple.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




