---
description: Describe las funcionalidades de Msvm \_ VirtualEthernetSwitchManagementService asociada.
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Msvm_VirtualEthernetSwitchManagementCapabilities clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec672403171407d0e6d8d29ff8a5605c2d460ea855aef2230d0f9ed0285cecc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148108"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a>Clase Msvm \_ VirtualEthernetSwitchManagementCapabilities

Describe las funcionalidades de [**Msvm \_ VirtualEthernetSwitchManagementService asociada.**](msvm-virtualethernetswitchmanagementservice.md)

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a>Miembros

La **clase \_ VirtualEthernetSwitchManagementCapabilities de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VirtualEthernetSwitchManagementCapabilities de Msvm** tiene estas propiedades.

<dl> <dt>

**AsynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")
</dt> </dl>

Matriz de identificadores de método, cada uno de los que identifica un método de la clase [**\_ VirtualEthernetSwitchManagementService de Msvm**](msvm-virtualethernetswitchmanagementservice.md) que la implementación admite de forma asincrónica. Esta propiedad se hereda de **CIM \_ VirtualSystemManagementCapabilities.**

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

**DefineSystem** (2)


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

**DestroySystem** (3)


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

**DestroySystemConfiguration** (4)


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

**ModifyResourceSettings** (5)


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

**ModifySystemSettings** (6)


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

**RemoveResources** (7)


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

**SelectSystemConfiguration** (8)


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

**SnapshotSystem** (9)


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

**AddResources** (10)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

**AddFeatureSettingsSupported** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

**ModifyFeatureSettingsSupported** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

**RemoveFeatureSettingsSupported** (32781)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

**AddFeatureSettingsSupported** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

**ModifyFeatureSettingsSupported** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

**RemoveFeatureSettingsSupported** (32781)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Funcionalidades del servicio de administración de conmutador Ethernet virtual de Hyper-V".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Define las funcionalidades del servicio de administración de conmutador Ethernet virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Funcionalidades del servicio de administración de conmutador Ethernet virtual de Hyper-V".

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede modificar la propiedad **ElementName.** Esta propiedad se hereda de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica las restricciones en **ElementName**, expresadas como una expresión regular. Esta propiedad se hereda de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**Indicaciones Admitidas**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de identificadores de indicación, cada uno de los que identifica una indicación que es compatible con la implementación. Esta propiedad se hereda de **CIM \_ VirtualSystemManagementCapabilities.**



| Value                                                                                                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt> </dl> | Indica si la implementación admite la notificación sobre los cambios de estado de las instancias [**\_ logicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) de CIM que representan recursos de sistemas virtuales.<br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt> </dl>                 | Indica si la implementación admite la notificación sobre los cambios de estado de [**las instancias de \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) de CIM.<br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt> </dl>         | Indica si la implementación admite la notificación sobre los cambios de estado de las instancias [**\_ de CIM ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representan sistemas virtuales.<br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>.</dt> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Vendor Reserved**</dt> <dt>32767..65535</dt> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**IOVSupport**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor booleano que indica si la plataforma admite la virtualización de E/S (IOV). Si el valor es **True**, la plataforma admite IOV y **IOVSupportReasons** estará vacío. De lo **contrario, la propiedad IOVSupportReasons** tendrá los motivos por los que no se admite IOV.

</dd> <dt>

**IOVSupportReasons**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que indica las posibles razones por las que no se admite IOV. Si el valor de **IOVSupport es** **True,** esta matriz estará vacía.

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo de datos: **unit16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxValue** (256)
</dt> </dl>

Especifica la longitud máxima admitida de la **propiedad ElementName.** Esta propiedad se hereda de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz unit16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los posibles estados que se pueden solicitar al usar el **método RequestStateChange** en el elemento lógico habilitado. Esta propiedad se hereda de **CIM \_ EnabledLogicalElementCapabilities** y siempre es **Null.**

</dd> <dt>

**SynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de identificadores de método, cada uno de los que identifica un método de la clase [**\_ VirtualEthernetSwitchManagementService de Msvm**](msvm-virtualethernetswitchmanagementservice.md) que la implementación admite de forma sincrónica. Esta propiedad se hereda de **CIM \_ VirtualSystemManagementCapabilities.**

<dl> <dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)
</dt> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)
</dt> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)
</dt> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)
</dt> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)
</dt> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)
</dt> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)
</dt> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)
</dt> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)
</dt> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)
</dt> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)
</dt> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 )
</dt> </dl>

</dd> <dt>

**VirtualSystemTypesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas, cada una de las que designa un tipo de sistema virtual compatible con la implementación. El valor de cada elemento de matriz distinto de **NULL** debe ajustarse al formato definido para la propiedad **VirtualSystemType** de la clase [**Msvm \_ VirtualSystemSettingData.**](msvm-virtualsystemsettingdata.md) Esta propiedad se hereda de **CIM \_ VirtualSystemManagementCapabilities.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

