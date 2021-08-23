---
description: Define los perfiles registrados a los que se ajusta el sistema al que se hace referencia.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a80dfcb5ab260b4d60b6370bb34698efb201401f0c6d4924b143e8b9041258a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525055"
---
# <a name="msvm_elementconformstoprofile-class"></a>Clase \_ ElementConformsToProfile de Msvm

Define los perfiles registrados a los que se ajusta el sistema al que se hace referencia. Esta asociación puede aplicarse a cualquier elemento administrado. El uso típico lo aplicará a una instancia de nivel superior, como un sistema, un espacio de nombres o un servicio. Cuando se aplica a una instancia de nivel superior, todas las partes constituyentes deben comportarse correctamente en apoyo de la conformidad del elemento administrado con el perfil registrado con nombre.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Miembros

La **clase \_ ElementConformsToProfile de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ElementConformsToProfile de Msvm** tiene estas propiedades.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de la clase [**\_ RegisteredProfile de Msvm**](msvm-registeredprofile.md) que representa el perfil registrado al que se ajusta el sistema.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa el sistema que se ajusta al perfil registrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

