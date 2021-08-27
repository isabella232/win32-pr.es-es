---
description: La clase ManagedElement de CIM es una clase abstracta que proporciona una superclase común (o la parte superior del árbol de herencia) para las clases que no son de asociación \_ en el esquema CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement clase
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
ms.openlocfilehash: acce9925f057ab63e0697c2bc12cae4336533068afdf43f46322e4d3718b25c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648187"
---
# <a name="cim_managedelement-class"></a>Cim \_ ManagedElement (clase)

La **clase \_ ManagedElement de CIM** es una clase abstracta que proporciona una superclase común (o la parte superior del árbol de herencia) para las clases que no son de asociación en el esquema CIM.

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

La **clase \_ ManagedElement de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ManagedElement de CIM** tiene estas propiedades.

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

Descripción textual del objeto.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre descriptivo del objeto. Esta propiedad permite a cada instancia definir un nombre descriptivo además de sus propiedades clave, datos de identidad e información de descripción.

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
> Para garantizar la unidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse con el siguiente patrón: *OrgID*:*LocalID*
>
> *OrgID* debe incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial que define **instanceID** o ser un identificador registrado asignado por una autoridad global reconocida. Este patrón es similar a la estructura de los nombres de clase de esquema. Además, para garantizar la unidad, el primer signo de dos puntos de **InstanceID** debe estar entre *orgID* y *LocalID.* Por lo *tanto, orgID* no debe contener dos puntos (':').
>
> La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar los distintos elementos subyacentes del mundo real.
>
> Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **instanceID** resultante no se vuelva a usar en ninguna propiedad **InstanceID** producida por este proveedor u otros proveedores para este espacio de nombres.
>
> En el caso de las instancias definidas por el Grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con *el OrgID* establecido en CIM.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

