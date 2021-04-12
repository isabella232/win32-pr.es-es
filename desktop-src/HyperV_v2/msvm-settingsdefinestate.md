---
description: Asocia una máquina virtual y sus dispositivos con instancias del \_ objeto SettingData de CIM que representan la configuración actual que se aplica a estos objetos.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277570"
---
# <a name="msvm_settingsdefinestate-class"></a>MSVM \_ SettingsDefineState (clase)

Asocia una máquina virtual y sus dispositivos con instancias del [**objeto \_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) que representan la configuración actual que se aplica a estos objetos. Más específicamente, asocia [**MSVM \_ ComputerSystem**](msvm-computersystem.md) con instancias de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)y asocia **MSVM \_ \** _ derivados de _ el [*\_ LogicalDevice* * de CIM](/windows/desktop/CIMWin32Prov/cim-logicaldevice) con **MSVM \_ \** _ derivados de [_ *CIM \_ ResourceAllocationSettingData*. *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SettingsDefineState** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SettingsDefineState** tiene estas propiedades.

<dl> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la máquina virtual.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la configuración actual de la máquina virtual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ SettingsDefineState** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETTINGSDEFINESTATE CIM**](cim-settingsdefinestate.md)
</dt> <dt>

[**\_SETTINGSDEFINESTATE CIM**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Clases de administración de sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

