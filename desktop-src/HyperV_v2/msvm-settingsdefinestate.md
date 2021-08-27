---
description: Asocia una máquina virtual y sus dispositivos a instancias de CIM SettingData que representan la \_ configuración actual que se aplica a estos objetos.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState clase
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
ms.openlocfilehash: eea8a6cce263ddb3ad00ecd6951c1d5b47c6d98d58e99763b3f28780cb3438b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950473"
---
# <a name="msvm_settingsdefinestate-class"></a>Clase Msvm \_ SettingsDefineState

Asocia una máquina virtual y sus dispositivos a instancias de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que representan la configuración actual que se aplica a estos objetos. Más concretamente, asocia [**Msvm \_ ComputerSystem**](msvm-computersystem.md) con instancias de [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)y asocia **\_ \* Msvm* _ derivados de [_ CIM *\_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) con **Msvm \_ \** _ derivados de _ CIM [*\_ ResourceAllocationSettingData* *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase \_ SettingsDefineState de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ SettingsDefineState** tiene estas propiedades.

<dl> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la máquina virtual.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la configuración activa actualmente para la máquina virtual.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a la **clase Msvm \_ SettingsDefineState** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración \_ de CIMDefineState**](cim-settingsdefinestate.md)
</dt> <dt>

[**Configuración \_ de CIMDefineState**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Clases de administración de sistemas virtuales](virtual-system-management-classes.md)
</dt> </dl>

 

