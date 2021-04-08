---
description: Informa de un evento de modificación del espacio de nombres, que es un tipo de evento intrínseco que se genera cuando se modifica un espacio de nombres.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: __NamespaceModificationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817614"
---
# <a name="__namespacemodificationevent-class"></a>\_\_Clase NamespaceModificationEvent

La clase del sistema **\_ \_ NamespaceModificationEvent** informa de un evento de modificación del espacio de nombres, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se modifica un espacio de nombres.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ NamespaceModificationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ NamespaceModificationEvent** tiene estas propiedades.

<dl> <dt>

**PreviousNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ espacio de nombres**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de la versión original de una instancia de [**\_ \_ espacio de nombres**](--namespace.md) . La propiedad **nombre** de esta instancia identifica el espacio de nombres que se ha modificado.

</dd> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**descriptor de seguridad \_** 
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor que el proveedor de eventos utiliza para determinar los usuarios que pueden recibir un evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

> [!Note]  
> Una lista de control de acceso (ACL) **nula** en el [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado a todos los usuarios. Para obtener más información, vea [crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ espacio de nombres**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de la instancia de [**\_ \_ espacio de nombres**](--namespace.md) que se modifica. La propiedad **Name** de la instancia de **\_ \_ espacio de nombres** indica el espacio de nombres que se ha modificado. Esta propiedad se hereda de la clase [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se genera un evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información tiene el formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ NamespaceModificationEvent** se deriva de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

Las únicas diferencias entre el espacio de nombres de destino y el espacio de nombres anterior son los calificadores y las propiedades excepto [**Name**](--namespace.md).

Tenga en cuenta que la propiedad [**Name**](--namespace.md) de una instancia de **\_ \_ espacio de nombres** no puede cambiar porque no se puede cambiar el nombre de los espacios de nombres. Para modificar el nombre de un espacio de nombres, se debe eliminar la instancia de **\_ \_ espacio de nombres** y volver a crearla con un nuevo nombre. Por lo tanto, los eventos de modificación del espacio de nombres se generan cuando se produce un cambio en calificadores y propiedades que no sean **Name**. Un evento de modificación del espacio de nombres no se genera cuando se produce algún tipo de cambio en el espacio de nombres. Un evento de modificación del espacio de nombres solo se genera cuando se modifica una instancia de espacio de nombres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

