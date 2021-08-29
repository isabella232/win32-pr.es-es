---
description: Representa la configuración de un conmutador Canal de fibra virtual.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Msvm_VirtualFcSwitchSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 75991b0efe412d53fab421d8518cc8fa35d2fb37cd1bda21a6d38186d9874cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426325"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a>Clase Msvm \_ VirtualFcSwitchSettingData

Representa la configuración de un conmutador Canal de fibra virtual.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ VirtualFcSwitchSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualFcSwitchSettingData** tiene estas propiedades.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para la máquina virtual cuando se produce un error en el software ejecutado por la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para la máquina virtual cuando se apaga el host. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para la máquina virtual cuando se inicia el host. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tiempo de retraso antes de que la máquina virtual se inicie automáticamente. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número que indica la secuencia relativa de activación de la máquina virtual cuando se inicia el sistema host. Un número inferior indica una activación anterior. Si una o varias configuraciones muestran el mismo valor, la secuencia depende de la implementación. Un valor de 0 indica que la secuencia depende de la implementación. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena información sobre la configuración de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso relativa y nombre de archivo de un archivo donde se almacena información sobre la configuración de la máquina virtual. Esta ruta de acceso es relativa a la **propiedad ConfigurationDataRoot.** Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único de la configuración. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena la información de registro de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**Notas**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Notas proporcionadas por el usuario relacionadas con la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso completa de un archivo donde se almacena la información relacionada con la recuperación de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena información sobre las instantáneas de máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacena información sobre la máquina virtual relacionada con la suspensión. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de un directorio donde se almacenan los archivos de intercambio de la máquina virtual. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))pero no se usa.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del objeto [**\_ ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) al que pertenecen los datos de esta configuración. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de máquina virtual que representan los datos de configuración. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

