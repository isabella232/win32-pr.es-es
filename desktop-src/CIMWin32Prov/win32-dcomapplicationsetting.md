---
description: Win32 \_ DCOMApplicationSetting&\# 8194; La clase WMI representa la configuración de una aplicación DCOM.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659747"
---
# <a name="win32_dcomapplicationsetting-class"></a>\_Clase Win32 DCOMApplicationSetting

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DCOMApplicationSetting de Win32** representa la configuración de una aplicación DCOM. Contiene las opciones de configuración de DCOM asociadas a la clave **AppID** en el registro. Estas opciones son válidas en los componentes agrupados lógicamente en la clase de aplicación especificada.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a>Miembros

La **clase \_ DCOMApplicationSetting de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ DCOMApplicationSetting** tiene estos métodos.



| Método                                                                                                                        | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAccessSecurityDescriptor**](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Obtiene el descriptor de seguridad que controla quién tiene permiso para obtener acceso a una aplicación DCOM.<br/>                                                                                                                              |
| [**GetConfigurationSecurityDescriptor**](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Obtiene el descriptor de seguridad que controla quién tiene permiso para configurar una aplicación DCOM.<br/>                                                                                                                           |
| [**GetLaunchSecurityDescriptor**](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | Obtiene el descriptor de seguridad que controla quién tiene permiso para iniciar una aplicación DCOM.<br/>                                                                                                                              |
| [**SetAccessSecurityDescriptor**](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Actualiza el descriptor de seguridad de acceso de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de la clase de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/>        |
| [**SetConfigurationSecurityDescriptor**](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Actualiza el descriptor de seguridad de configuración de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de la clase de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/> |
| [**SetLaunchSecurityDescriptor**](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Actualiza el descriptor de seguridad de inicio de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de la clase de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/>        |



 

### <a name="properties"></a>Propiedades

La **clase \_ DCOMApplicationSetting de Win32** tiene estas propiedades.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ default \] ")
</dt> </dl>

Identificador único global (GUID) para esta aplicación DCOM.

</dd> <dt>

**AuthenticationLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")
</dt> </dl>

Nivel mínimo de autenticación del cliente requerido por este servidor COM. Si **es null**, se usan los valores predeterminados.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (1)


</dt> <dd>

Ninguno (no se realiza ninguna autenticación)

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Conectar** (2)


</dt> <dd>

Connect (solo se realiza la autenticación cuando el cliente establece una relación con la aplicación)

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>**Llamar a** (3)


</dt> <dd>

Call (la autenticación se realiza solo al principio de cada llamada cuando la aplicación recibe la solicitud)

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Paquete** (4)


</dt> <dd>

Paquete (la autenticación se realiza en todos los datos recibidos del cliente)

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)


</dt> <dd>

PacketIntegrity (todos los datos transferidos entre el cliente y la aplicación se autentican y comprueban)

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)


</dt> <dd>

PacketPrivacy (se usan las propiedades de los otros niveles de autenticación y se cifran todos los datos)

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**CustomSurrogate**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")
</dt> </dl>

Nombre del suplente personalizado en el que se activa la aplicación DCOM en proceso. Si este valor es **null** y la clave **UseSurrogate** es **true**, el sistema proporciona un proceso suplente.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**EnableAtStorageActivation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] ")
</dt> </dl>

La aplicación DCOM recupera el estado guardado de la aplicación o comienza en el estado en el que la aplicación se inicializa por primera vez.

</dd> <dt>

**LocalService (Servicio local)**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")
</dt> </dl>

Nombre de los servicios proporcionados por la aplicación DCOM.

</dd> <dt>

**RemoteServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] ")
</dt> </dl>

Nombre del servidor remoto en el que se activa la aplicación.

</dd> <dt>

**Como_usuario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ runas \] ")
</dt> </dl>

Cuenta de usuario específica en la que se ejecutará la aplicación durante la activación.

</dd> <dt>

**ServiceParameters**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] ")
</dt> </dl>

Parámetros de línea de comandos pasados a la aplicación DCOM. Esto solo es válido si la aplicación se escribe como un servicio basado en Windows.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**UseSurrogate**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")
</dt> </dl>

La aplicación DCOM se puede activar como un servidor fuera de proceso mediante el uso de un archivo ejecutable suplente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **Win32 \_ DCOMApplicationSetting** se deriva de [**\_ comsetting de Win32**](win32-comsetting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Establecimiento de Win32 \_**](win32-comsetting.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Constantes de privilegio**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

