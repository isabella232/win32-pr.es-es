---
description: Abstracción o emulación de una entidad de hardware que puede o no estar basada en hardware físico.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: CIM_LogicalDevice (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0831bff996721a170da105c800e670cf10cb4b422869062014ab4df9e2441416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812120"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a>CIM_LogicalDevice (administración de Hyper-V)

Abstracción o emulación de una entidad de hardware que puede o no estar basada en hardware físico.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a>Miembros

La **clase \_ LogicalDevice de CIM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ LogicalDevice de CIM** tiene estos métodos.



| Método                                                           | Descripción                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableDevice**](cim-logicaldevice-enabledevice.md)           | Este método es desusado. En su lugar, use **el método RequestStateChange.**<br/> **Descripción en desuso:** Habilita o deshabilita el dispositivo lógico.<br/>                                                                     |
| [**OnlineDevice**](cim-logicaldevice-onlinedevice.md)           | Este método es desusado. En su lugar, use **el método RequestStateChange.**<br/> **Descripción en desuso:** Pone el dispositivo lógico en línea para que pueda aceptar solicitudes o sin conexión para que ya no pueda aceptar solicitudes.<br/> |
| [**QuiesceDevice**](cim-logicaldevice-quiescedevice.md)         | Este método es desusado. En su lugar, use **el método RequestStateChange.**<br/> **Descripción en desuso:** Suspende temporalmente la actividad en el dispositivo lógico o vuelva a habilitarla.<br/>                            |
| [**Restablecer**](cim-logicaldevice-reset.md)                         | Restablece el dispositivo lógico.<br/>                                                                                                                                                                                                    |
| [**RestoreProperties**](cim-logicaldevice-restoreproperties.md) | Restaura una configuración y un estado anteriores del dispositivo lógico.<br/>                                                                                                                                                            |
| [**SaveProperties**](cim-logicaldevice-saveproperties.md)       | Guarda la configuración y el estado del dispositivo lógico.<br/>                                                                                                                                                                      |
| [**SetPowerState**](cim-logicaldevice-setpowerstate.md)         | Este método es desusado. En su lugar, use **la propiedad SetPowerState** de la **clase CIM \_ PowerManagementService.**<br/> **Descripción en desuso:** Establece el estado de energía del dispositivo lógico.<br/>                       |



 

### <a name="properties"></a>Propiedades

La **clase \_ LogicalDevice** de CIM tiene estas propiedades.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Disponibilidad**")
</dt> </dl>

Matriz que contiene información de disponibilidad sobre el dispositivo lógico, además de la de la **propiedad Availability.**

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Running/Full Power** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Advertencia** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**En prueba** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Apagado** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

**Fuera de servicio** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**No instalado** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Error de instalación** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

**Ahorro de energía: desconocido** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Ahorro de energía: modo de bajo consumo** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Ahorro de energía: en espera** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Ciclo de** energía (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

**Ahorro de energía: advertencia** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**En pausa** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**No listo** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**No configurado** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

**En modo de quiesced** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**Disponibilidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 006.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus", "MIF. DMTF \| Host Device \| 001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**AdditionalAvailability**")
</dt> </dl>

Contiene la disponibilidad del dispositivo lógico.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Running/Full Power** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Advertencia** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**En prueba** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Apagado** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

**Fuera de servicio** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**No instalado** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Error de instalación** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

**Ahorro de energía: desconocido** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Ahorro de energía: modo de bajo consumo** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Ahorro de energía: en espera** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Ciclo de** energía (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

**Ahorro de energía: advertencia** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**En pausa** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**No listo** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**No configurado** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

**En modo de quiesced** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de clase usado para crear una instancia del dispositivo lógico. **CreationClassName** se combina con otras propiedades clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Identificador único del dispositivo lógico, como la dirección.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Esta propiedad está desusada. En su lugar, use **la propiedad OperationalStatus** de la **clase \_ ManagedSystemElement de** CIM.

**Descripción en desuso:** Indica si se borra un error notificado por **la propiedad LastErrorCode.**

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData.ErrorDescription")
</dt> </dl>

Esta propiedad está desusada. En su lugar, use **la propiedad ErrorDescription** de la **clase \_ DeviceErrorData de CIM.**

**Descripción en desuso:** Información adicional sobre el error notificado por la **propiedad LastErrorCode.**

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**OtherIdentifyingInfo**")
</dt> </dl>

Matriz de cadenas que describen los **elementos de la matriz OtherIdentifyingInfo** del mismo índice.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData.LastErrorCode")
</dt> </dl>

Esta propiedad está desusada. En su lugar, usamos **la propiedad LastErrorCode** de la **clase \_ DeviceErrorData de CIM.**

**Descripción en desuso:** Último código de error notificado por el dispositivo lógico.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sin valor"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Milisegundos")
</dt> </dl>

Esta propiedad está en desuso y no debe utilizarse.

**Descripción en desuso:** El tiempo máximo en milisegundos, que un dispositivo puede permanecer en un estado deshabilitado temporalmente (las propiedades **Availability** y **AdditionalAvailability** establecidas en "21" están en modo de espera). Un valor de "0" indica que el dispositivo lógico puede permanecer en un estado deshabilitado temporalmente indefinidamente.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**IdentifyingDescriptions**")
</dt> </dl>

Información que identifica el dispositivo lógico, distinto de **DeviceID.**

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities.PowerCapabilities")
</dt> </dl>

Esta propiedad está desusada. En su lugar, use **la \_ clase CIM PowerManagementCapabilities.**

**Descripción en desuso:** Matriz que contiene las funcionalidades de administración de energía del dispositivo.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**No compatible** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Modos de ahorro de energía especificados automáticamente** (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Power State Settable** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Power Cycling compatible** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Encendido con tiempo de encendido admitido** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities")
</dt> </dl>

Esta propiedad está desusada. En su lugar, use **la clase PowerManagementCapabilities.**

**Descripción en desuso: true** si el dispositivo lógico se puede administrar con energía; de lo contrario, **false**.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("horas"), **contador**
</dt> </dl>

Número de horas consecutivas en las que se ha encendido el dispositivo lógico, desde su último ciclo de energía.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 006.4")
</dt> </dl>

Esta propiedad está desusada. En su lugar, use **la \_ clase CIM PowerManagementCapabilities.**

**Descripción en desuso:** Indica si el dispositivo lógico está habilitado o en un estado relacionado.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**")
</dt> </dl>

Nombre de clase utilizado para crear una instancia del sistema que contiene el dispositivo lógico. **SystemCreationClassName se** combina con otras propiedades clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**")
</dt> </dl>

Nombre del sistema que contiene el dispositivo lógico.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("horas"), **contador**
</dt> </dl>

Número total de horas que se ha encendido el dispositivo lógico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)
</dt> </dl>

 

