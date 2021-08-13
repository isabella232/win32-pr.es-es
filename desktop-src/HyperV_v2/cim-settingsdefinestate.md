---
description: Asocia los datos de configuración a un elemento administrado.
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: CIM_SettingsDefineState clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4278043511348f3df5f72886f0c96bf18a34158a61b31a4590f880c7a1c0f150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647274"
---
# <a name="cim_settingsdefinestate-class"></a>Cim \_ SettingsDefineState (clase)

Asocia los datos de configuración a un elemento administrado.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ SettingsDefineState** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ SettingsDefineState** tiene estas propiedades.

<dl> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elemento administrado de la asociación.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Los datos de configuración de la asociación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

