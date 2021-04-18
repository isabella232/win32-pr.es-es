---
description: La \_ clase ManagedElement de CIM es una clase abstracta que proporciona una superclase común (o parte superior del árbol de herencia) para las clases que no son de asociación en el esquema CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686510"
---
# <a name="cim_managedelement-class"></a>CIM \_ ManagedElement (clase)

La **clase \_ ManagedElement de CIM** es una clase abstracta que proporciona una superclase común (o parte superior del árbol de herencia) para las clases que no son de asociación en el esquema CIM.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ManagedElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ManagedElement** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual del objeto.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una descripción textual del objeto.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un nombre descriptivo para el objeto. Esta propiedad permite a cada instancia definir un nombre descriptivo además de las propiedades clave, los datos de identidad y la información de descripción.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica de forma única y opaca una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.

> [!IMPORTANT]
>
> Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*
>
> *OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define el **InstanceID**, o bien un identificador registrado asignado por una entidad global reconocida. Este patrón es similar a la estructura de los nombres de clase de esquema. Además, para garantizar la exclusividad, el primer signo de dos puntos en **InstanceID** debe estar entre el *OrgID* y el *LocalID*. Por lo tanto, el *OrgID* no debe contener un signo de dos puntos (': ').
>
> La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.
>
> Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.
>
> En el caso de las instancias definidas por el grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con el valor de *OrgID* establecido en CIM.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

