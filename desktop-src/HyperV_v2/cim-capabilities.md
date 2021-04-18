---
description: Clase abstracta para las subclases que describe las capacidades de un elemento administrado asociado y el potencial de las capacidades.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: CIM_Capabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687786"
---
# <a name="cim_capabilities-class"></a>CIM \_ Capabilities (clase)

Clase abstracta para las subclases que describe las capacidades de un elemento administrado asociado y el potencial de las capacidades.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Miembros

La clase de **\_ capacidades CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ capacidades CIM** tiene estas propiedades.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nombre descriptivo de esta instancia de clase. Además, el nombre descriptivo del usuario se puede usar como una propiedad de índice para una consulta. Este valor no tiene que ser único dentro de su espacio de nombres.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ManagedElement de CIM \_**](cim-managedelement.md)
</dt> </dl>

 

