---
description: Notifica un evento de creación de espacio de nombres, que es un tipo de evento intrínseco que se genera cuando se agrega un nuevo espacio de nombres al espacio de nombres actual.
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: __NamespaceCreationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 8432bcfb2c96c70b91a7f0d187297217082e2d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678049"
---
# <a name="__namespacecreationevent-class"></a>\_\_Clase NamespaceCreationEvent

La clase del sistema **\_ \_ NamespaceCreationEvent** informa de un evento de creación de espacio de nombres, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se agrega un nuevo espacio de nombres al espacio de nombres actual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ NamespaceCreationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ NamespaceCreationEvent** tiene estas propiedades.

<dl> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ espacio de nombres**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de la instancia de [**\_ \_ espacio de nombres**](--namespace.md) que se creó. La propiedad **Name** de la instancia de **\_ \_ espacio de nombres** indica qué espacio de nombres se ha creado. Esta propiedad se hereda de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información tiene el formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ NamespaceCreationEvent** se deriva de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

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

 

