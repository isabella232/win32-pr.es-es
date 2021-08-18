---
description: Notifica un evento de modificación del espacio de nombres, que es un tipo de evento intrínseco que se genera cuando se modifica un espacio de nombres.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: __NamespaceModificationEvent clase
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
ms.openlocfilehash: 3243afe0a8cae34e83ad85e2d89a3becab8d07775ba3ec0c3283fd4ea8ed8bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557818"
---
# <a name="__namespacemodificationevent-class"></a>\_\_Clase NamespaceModificationEvent

La clase del sistema **\_ \_ NamespaceModificationEvent** notifica un evento [](determining-the-type-of-event-to-receive.md) de modificación del espacio de nombres, que es un tipo de evento intrínseco que se genera cuando se modifica un espacio de nombres.

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

La **\_ \_ clase NamespaceModificationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase NamespaceModificationEvent** tiene estas propiedades.

<dl> <dt>

**PreviousNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: Espacio **\_ \_ de nombres**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de la versión original de una instancia [**\_ \_ de Namespace.**](--namespace.md) La **propiedad Name** de esta instancia identifica el espacio de nombres que se modifica.

</dd> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**DESCRIPTOR \_ DE SEGURIDAD** 
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor que usa el proveedor de eventos para determinar los usuarios que pueden recibir un evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

> [!Note]  
> Una **lista de** control de acceso (ACL) NULL en el DESCRIPTOR DE [**\_ SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado a todos los usuarios todo el tiempo. Para obtener más información, [vea Crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**Targetnamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: Espacio **\_ \_ de nombres**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de la instancia [**\_ \_ del espacio**](--namespace.md) de nombres que se modifica. La **propiedad Name** de la instancia de **\_ \_ Namespace** indica el espacio de nombres que se modifica. Esta propiedad se hereda de la clase [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se genera un evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase NamespaceModificationEvent** se deriva de [**\_ \_ NamespaceOperationEvent.**](--namespaceoperationevent.md)

Las únicas diferencias entre el espacio de nombres de destino y el espacio de nombres anterior son los calificadores y las propiedades, excepto [**Name**](--namespace.md).

Tenga en cuenta que [**la propiedad Name**](--namespace.md) de una instancia de **\_ \_ Namespace** no puede cambiar porque no se puede cambiar el nombre de los espacios de nombres. Para modificar el nombre de un espacio de nombres, la instancia **\_ \_ de Namespace** debe eliminarse y volver a crearse con un nuevo nombre. Por lo tanto, los eventos de modificación del espacio de nombres se generan cuando se produce un cambio en calificadores y propiedades distintos de **Name**. No se genera un evento de modificación del espacio de nombres cuando se produce cualquier tipo de cambio dentro del espacio de nombres. Solo se genera un evento de modificación del espacio de nombres cuando se modifica una instancia de espacio de nombres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

