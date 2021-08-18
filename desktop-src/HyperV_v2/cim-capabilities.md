---
description: Clase abstracta para subclases que describe las capacidades de un elemento administrado asociado y el potencial de las capacidades.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: CIM_Capabilities clase
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
ms.openlocfilehash: 7fc640950b7e943f0e549f41ec216b2832ec9de3b91938ef1aadea1893ac2faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561915"
---
# <a name="cim_capabilities-class"></a>Cim \_ Capabilities (clase)

Clase abstracta para subclases que describe las capacidades de un elemento administrado asociado y el potencial de las capacidades.

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

La **clase \_ Capacidades** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Capacidades** de CIM tiene estas propiedades.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nombre descriptivo de esta instancia de clase. Además, el nombre descriptivo se puede usar como una propiedad de índice para una consulta. Este valor no tiene que ser único dentro de su espacio de nombres.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica de forma única y opaca una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.

> [!IMPORTANT]
>
> Para garantizar la unidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse con el siguiente patrón: *OrgID*:*LocalID*
>
> *OrgID* debe incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial que define el **InstanceID,** o debe ser un identificador registrado asignado por una autoridad global reconocida. Este patrón es similar a la estructura de los nombres de clase de esquema. Además, para garantizar la unidad, el primer signo de dos puntos de **InstanceID** debe estar entre *orgID* y *LocalID*. Por lo *tanto, orgID* no debe contener dos puntos (':').
>
> La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar los distintos elementos subyacentes del mundo real.
>
> Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **instanceID** resultante no se vuelva a usar en ninguna propiedad **InstanceID** producida por este proveedor u otros proveedores para este espacio de nombres.
>
> En el caso de las instancias definidas por el Grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con *el OrgID* establecido en CIM.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento administrado de CIM \_**](cim-managedelement.md)
</dt> </dl>

 

