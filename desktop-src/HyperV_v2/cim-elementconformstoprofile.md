---
description: Representa una asociación en la que un elemento administrado se ajusta al estándar de un perfil registrado.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: CIM_ElementConformsToProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666692"
---
# <a name="cim_elementconformstoprofile-class"></a>\_Clase ElementConformsToProfile de CIM

Representa una asociación en la que un elemento administrado se ajusta al estándar de un perfil registrado. Esta asociación se aplica normalmente a una instancia de nivel superior, como un sistema, un espacio de nombres o un servicio. Cuando se aplica a una instancia de nivel superior, todas las partes constituyentes deben comportarse de forma adecuada para admitir la conformidad del ManagedElement con el RegisteredProfile con nombre.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ElementConformsToProfile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ElementConformsToProfile** tiene estas propiedades.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ RegisteredProfile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Perfil registrado al que se ajusta el elemento administrado.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elemento administrado que se ajusta al perfil registrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

