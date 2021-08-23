---
description: Define los perfiles registrados a los que se ajusta el sistema independiente al que se hace referencia.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Msvm_StandaloneV2ElementConformsToProfile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5506119f0e8938a29b94b298460a1f164dab97359d13d956bfa5ca74e97a081b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950244"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>Clase Msvm \_ StandaloneV2ElementConformsToProfile

Define los perfiles registrados a los que se ajusta el sistema independiente al que se hace referencia.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ StandaloneV2ElementConformsToProfile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ StandaloneV2ElementConformsToProfile** tiene estas propiedades.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ RegisteredProfile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Perfil registrado al que se ajusta el sistema independiente.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ TargetNamespace** ("root \\ \\ virtualization \\ \\ v2")
</dt> </dl>

Sistema independiente que se ajusta al perfil registrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Interoperabilidad \\ raíz<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento \_ MsvmConformsToProfile**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

