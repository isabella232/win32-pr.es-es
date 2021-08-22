---
description: Representa el estado del componente de interfaz de servicio invitado, que proporciona un mecanismo para interactuar con la máquina virtual desde las interfaces de administración del sistema host.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Msvm_GuestServiceInterfaceComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c7e404a1195332b508de22fc0a26dfebb96eba29f487f08505987edcc72b6cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523025"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>Clase \_ GuestServiceInterfaceComponent de Msvm

Representa el estado del componente de interfaz de servicio invitado, que proporciona un mecanismo para interactuar con la máquina virtual desde las interfaces de administración del sistema host. Esta clase se deriva de la [**clase \_ LogicalDevice de CIM.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Miembros

La **clase \_ GuestServiceInterfaceComponent de Msvm** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase Msvm \_ GuestServiceInterfaceComponent** tiene estos métodos.



| Método                                                                               | Descripción                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | Solicita que el estado del componente de la interfaz de servicio invitado se cambie al valor especificado.<br/>                           |
| [**Restablecer**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | Solicita un restablecimiento del dispositivo lógico. Wmi no implementa .<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | Define el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo en ese estado. Wmi no implementa .<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ GuestServiceInterfaceComponent de Msvm** tiene estas propiedades.

<dl> <dt>

**Disponibilidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Disponibilidad y estado del dispositivo.



| Value                                                                                                                                                                                                                                                                                                              | Significado                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Otros**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>2 (0x2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <dt>**Running/Full Power**</dt> <dt>3 (0x3)</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**Advertencia**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**En la**</dt> <dt>prueba 5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**No aplicable**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**Apagar**</dt> <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Off Line**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**Fuera del servicio**</dt> <dt>9 (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degradado**</dt> <dt>10 (0xA)</dt> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**No instalado**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**Error de**</dt> <dt>instalación 12 (0xC)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <dt>**Ahorro de energía: desconocido**</dt> <dt>13 (0xD)</dt> </dl>                             | Se sabe que el dispositivo está en modo de ahorro de energía, pero se desconoce su estado exacto.<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <dt>**Ahorro de energía: modo de bajo consumo**</dt> <dt>14 (0xE)</dt> </dl> | El dispositivo está en un estado de ahorro de energía pero sigue funcionando y puede presentar un rendimiento degradado.<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <dt>**Ahorro de energía: espera**</dt> <dt>15 (0xF)</dt> </dl>                             | El dispositivo no funciona, pero se podría llevar a toda la energía rápidamente.<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**Ciclo de**</dt> <dt>energía 16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <dt>**Ahorro de energía: advertencia**</dt> <dt>17 (0x11)</dt> </dl>                            | El dispositivo está en estado de advertencia, aunque también en modo de ahorro de energía.<br/>                              |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción textual del objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Código de error Administrador de configuración Win32.



| Value                                                                                | Significado                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | El dispositivo funciona correctamente.<br/>                                                                                                   |
| <dl> <dt>1 (0x1)</dt> </dl>   | El dispositivo no está configurado correctamente.<br/>                                                                                           |
| <dl> <dt>2 (0x2)</dt> </dl>   | Windows puede cargar el controlador para este dispositivo.<br/>                                                                               |
| <dl> <dt>3 (0x3)</dt> </dl>   | Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.<br/>                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | El dispositivo no funciona correctamente. Uno de sus controladores o el registro podrían estar dañados.<br/>                                        |
| <dl> <dt>5 (0x5)</dt> </dl>   | El controlador del dispositivo requiere un recurso que Windows puede administrar.<br/>                                                         |
| <dl> <dt>6 (0x6)</dt> </dl>   | La configuración de arranque del dispositivo entra en conflicto con otros dispositivos.<br/>                                                               |
| <dl> <dt>7 (0x7)</dt> </dl>   | No se puede filtrar.<br/>                                                                                                                |
| <dl> <dt>8 (0x8)</dt> </dl>   | Falta el cargador de controladores para el dispositivo.<br/>                                                                                      |
| <dl> <dt>9 (0x9)</dt> </dl>   | El dispositivo no funciona correctamente; el firmware de control informa incorrectamente de los recursos del dispositivo.<br/>               |
| <dl> <dt>10 (0xA)</dt> </dl>  | El dispositivo no se puede iniciar.<br/>                                                                                                          |
| <dl> <dt>11 (0xB)</dt> </dl>  | Error en el dispositivo.<br/>                                                                                                                |
| <dl> <dt>12 (0xC)</dt> </dl>  | El dispositivo no puede encontrar suficientes recursos gratuitos para usarlos.<br/>                                                                              |
| <dl> <dt>13 (0xD)</dt> </dl>  | Windows puede comprobar los recursos del dispositivo.<br/>                                                                                 |
| <dl> <dt>14 (0xE)</dt> </dl>  | El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.<br/>                                                                  |
| <dl> <dt>15 (0xF)</dt> </dl>  | El dispositivo no funciona correctamente debido a un posible problema de nueva enumeración.<br/>                                                      |
| <dl> <dt>16 (0x10)</dt> </dl> | Windows puede identificar todos los recursos que usa el dispositivo.<br/>                                                            |
| <dl> <dt>17 (0x11)</dt> </dl> | El dispositivo solicita un tipo de recurso desconocido.<br/>                                                                                |
| <dl> <dt>18 (0x12)</dt> </dl> | Los controladores de dispositivos deben volver a instalarse.<br/>                                                                                           |
| <dl> <dt>19 (0x13)</dt> </dl> | Error al usar el cargador VxD.<br/>                                                                                                 |
| <dl> <dt>20 (0x14)</dt> </dl> | El Registro puede estar dañado.<br/>                                                                                                  |
| <dl> <dt>21 (0x15)</dt> </dl> | Error del sistema. Si cambiar el controlador de dispositivo no es eficaz, consulte la documentación de hardware. Windows está quitando el dispositivo.<br/> |
| <dl> <dt>22 (0x16)</dt> </dl> | El dispositivo está deshabilitado.<br/>                                                                                                           |
| <dl> <dt>23 (0x17)</dt> </dl> | Error del sistema. Si cambiar el controlador de dispositivo no es eficaz, consulte la documentación de hardware.<br/>                                 |
| <dl> <dt>24 (0x18)</dt> </dl> | El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.<br/>                                   |
| <dl> <dt>25 (0x19)</dt> </dl> | Windows está configurando el dispositivo.<br/>                                                                                       |
| <dl> <dt>26 (0x1A)</dt> </dl> | Windows está configurando el dispositivo.<br/>                                                                                       |
| <dl> <dt>27 (0x1B)</dt> </dl> | El dispositivo no tiene una configuración de registro válida.<br/>                                                                                 |
| <dl> <dt>28 (0x1C)</dt> </dl> | Los controladores de dispositivo no están instalados.<br/>                                                                                             |
| <dl> <dt>29 (0x1D)</dt> </dl> | El dispositivo está deshabilitado; el firmware del dispositivo no proporciona los recursos necesarios.<br/>                                               |
| <dl> <dt>30 (0x1E)</dt> </dl> | El dispositivo usa un recurso IRQ que está usando otro dispositivo.<br/>                                                                 |
| <dl> <dt>31 (0x1F)</dt> </dl> | El dispositivo no funciona correctamente; Windows cargar los controladores de dispositivo necesarios.<br/>                                              |



 

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el dispositivo usa una configuración definida por el usuario.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase o subclase usada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de la clase y sus subclases.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección u otra información de identificación para dar un nombre único al dispositivo lógico.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** ahora se borra el error notificado en la propiedad **LastErrorCode.**

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que proporciona información sobre el error registrado en la **propiedad LastErrorCode** y las acciones correctivas que se deben realizar.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último código de error notificado por el dispositivo lógico.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.

Ejemplo: \* "PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de las funcionalidades específicas relacionadas con la energía de un dispositivo lógico. Esta propiedad se hereda de **CIM \_ LogicalDevice.**



| Value                                                                                                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**No se admite**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deshabilitado**</dt> <dt>2 (0x2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Habilitado**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <dt>**Modos de ahorro de energía especificados automáticamente**</dt> <dt>4 (0x4)</dt> </dl> | El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**Power State Settable**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | Se [**admite el método SetPowerState.**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) Este método se encuentra en la clase **\_ logicalDevice** de CIM primaria y se puede implementar. Para obtener más información, vea [Designing Managed Object Format (MOF) Classes .](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**Power Cycling Supported**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | El [**método SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) se puede invocar con el *parámetro PowerState* establecido en 5 ("Ciclo de energía").<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <dt>**Encendido con tiempo de encendido compatible**</dt> <dt>7 (0x7)</dt> </dl>                                                                 | El [**método SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) se puede invocar con el parámetro  *PowerState* establecido en 5 ("Ciclo de energía") y el tiempo establecido en una fecha y hora específicas, o un intervalo, para el encendido.<br/>                                                                                       |



 

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el dispositivo se puede administrar con energía, es decir, poner en un estado de ahorro de energía. Si **es FALSE,** el valor entero 1 ("No compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities.**

Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o, si están habilitadas, qué características se admiten. Para más información, consulte la matriz **PowerManagementCapabilities.**

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

Los valores son los siguientes:

<dl><span id="OK"></span><span id="ok"></span><dt>

**"Ok" (Correcto)**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**"Error"**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**"Degradado"**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**"Desconocido"**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Error previo"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**"Starting"**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**"Deteniendo"**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**"Servicio"**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**"Estresado"**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"NonRecover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Sin contacto"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Comm perdido"**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado del dispositivo lógico. Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("No aplicable"). Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1 (0x1))
</dt> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2 (0x2))
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3 (0x3))
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (4 (0x4))
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (5 (0x5))
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ámbito del nombre de la clase de creación del sistema.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del sistema de ámbito.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Dispositivo lógico CIM**](cim-logicaldevice.md)
</dt> <dt>

[**\_Dispositivo lógico CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

