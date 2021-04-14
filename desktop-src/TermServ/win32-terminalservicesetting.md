---
title: Win32_TerminalServiceSetting (clase)
description: Representa la configuración de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalServiceSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359821"
---
# <a name="win32_terminalservicesetting-class"></a>\_Clase Win32 TerminalServiceSetting

La clase WMI **\_ TerminalServiceSetting de Win32** representa la configuración de un servidor host de sesión de escritorio remoto (host escritorio remoto de sesión de RD). La configuración incluye capacidades como el modo de servidor host de sesión de escritorio remoto, licencias, Active Desktop, permisos, eliminación de carpetas temporales y directorios temporales para las sesiones.

La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético. Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a>Miembros

La **clase \_ TerminalServiceSetting de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TerminalServiceSetting** tiene estos métodos.



| Método                                                                                                                | Descripción                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDirectConnectLicenseServer**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | Configura un nuevo servidor de licencias en la empresa.<br/>                                                                                                                  |
| [**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | Agrega el servidor de licencias especificado al final de la lista de servidores de licencias especificados.<br/>                                                                                  |
| [**CanAccessLicenseServer**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | Determina si el servidor host de sesión de escritorio remoto tiene permiso para solicitar Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) desde un servidor de licencias de Escritorio remoto.<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | Establece el tipo de licencia del servidor de licencias de Escritorio remoto.<br/>                                                                                                       |
| [**CreateWinstation**](createwinstation-win32-terminalservicesetting.md)                                             | Crea una nueva pila de agentes de escucha basada en la combinación única de nombre del agente de escucha y NIC.<br/>                                                                              |
| [**DeleteDirectConnectLicenseServer**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | Elimina el servidor de licencias especificado de la empresa.<br/>                                                                                                           |
| [**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | Quita todos los servidores de licencias de la lista de servidores de licencias especificados.<br/>                                                                                             |
| [**FindLicenseServers**](findlicenseservers-win32-terminalservicesetting.md)                                         | Enumera todos los servidores de licencias de Escritorio remoto y el método de detección.<br/>                                                                                   |
| [**GetDomain**](getdomain-win32-terminalservicesetting.md)                                                           | Recupera el nombre del dominio del que es miembro el servidor host de sesión de escritorio remoto.<br/>                                                                                    |
| [**GetGracePeriodDays**](getgraceperioddays-win32-terminalservicesetting.md)                                         | Recupera el número de días que quedan en el período de gracia de la licencia de escritorio remoto para un servidor host de sesión de escritorio remoto.<br/>                                                     |
| [**GetRegisteredLicenseServerList**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | Obtiene la lista de servidores de licencias registrados.<br/>                                                                                                                        |
| [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Recupera la lista de servidores de licencias especificados.<br/>                                                                                                                    |
| [**GetTSLanaIds**](gettslanaids-win32-terminalservicesetting.md)                                                     | Obtiene los identificadores y descripciones de Servicios de Escritorio remoto adaptadores de red.<br/>                                                                                          |
| [**GetTStoLSConnectivityStatus**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | Determina el estado de conectividad entre Servicios de Escritorio remoto y un servidor de licencias.<br/>                                                                            |
| [**GetWinstationDriverNames**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | Recupera una lista de los nombres de controlador de la estación de la.<br/>                                                                                                                        |
| [**PingLicenseServer**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Hace ping en el servidor de licencias para determinar si se trata de un servidor de licencias válido.<br/>                                                                                         |
| [**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | Quita el servidor de licencias dado de la lista de servidores de licencias especificados.<br/>                                                                                        |
| [**SetAllowTSConnections**](win32-terminalservicesetting-setallowtsconnections.md)                                   | Establece la propiedad **AllowTSConnections** .<br/>                                                                                                                           |
| [**SetDisableForcibleLogoff**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | Establece la propiedad **DisableForcibleLogoff** .<br/>                                                                                                                        |
| [**SetFallbackPrintDriverType**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | Establece la propiedad **FallbackPrintDriverType** .<br/>                                                                                                                      |
| [**SetHomeDirectory**](win32-terminalservicesetting-sethomedirectory.md)                                             | Establece la propiedad **HomeDirectory** .<br/>                                                                                                                                |
| [**SetPolicyPropertyName**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | Establece una de las propiedades siguientes: **DeleteTempFolders** o **UseTempFolders**.<br/>                                                                                  |
| [**SetPrimaryLicenseServer**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | Establece el servidor de licencias dado como la primera entrada de la lista de servidores de licencias especificados.<br/>                                                                          |
| [**SetProfilePath**](win32-terminalservicesetting-setprofilepath.md)                                                 | Establece la propiedad **ProfilePath** .<br/>                                                                                                                                  |
| [**SetSingleSession**](win32-terminalservicesetting-setsinglesession.md)                                             | Establece la propiedad **SingleSession** .<br/>                                                                                                                                |
| [**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Actualiza la lista de servidores de licencias especificados, reemplazando los servidores de licencias especificados.<br/>                                                                    |
| [**SetTimeZoneRedirection**](win32-terminalservicesetting-settimezoneredirection.md)                                 | Establece la propiedad **TimeZoneRedirection** .<br/>                                                                                                                          |
| [**UpdateDirectConnectLicenseServer**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | Actualiza la lista de servidores de licencias de detección.<br/>                                                                                                                      |



 

### <a name="properties"></a>Propiedades

La **clase \_ TerminalServiceSetting de Win32** tiene estas propiedades.

<dl> <dt>

**ActiveDesktop**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se permite Active Desktop en cada sesión de usuario.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (0)


</dt> <dd>

Active Desktop no se permite en cada sesión de usuario.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (1)


</dt> <dd>

Active Desktop se permite en cada sesión de usuario.

</dd> </dl>

</dd> <dt>

**AllowTSConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se permiten nuevas conexiones Servicios de Escritorio remoto.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

No se permiten nuevas conexiones.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Se permiten nuevas conexiones.

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

Descripción breve (cadena de una línea) del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**DeleteTempFolders**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si los directorios temporales se eliminan al salir.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La eliminación de directorios temporales está deshabilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La eliminación de directorios temporales está habilitada.

</dd> </dl>

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**DirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no está disponible.

**Windows Server 2008:** Enumera la lista de servidores de licencias.

</dd> <dt>

**DisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Determina si un administrador que ha iniciado sesión en la consola de se puede cerrar la sesión forzosamente.

<dt>

0
</dt> <dd>

El administrador puede cerrar la sesión con fuerza.

</dd> <dt>

1
</dt> <dd>

No se puede cerrar la sesión del administrador forzosamente.

</dd> </dl>

</dd> <dt>

**EnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se permite que los clientes de conexión de Escritorio remoto se vuelvan a conectar automáticamente a las sesiones de un servidor host de sesión de escritorio remoto si el vínculo de red se pierde temporalmente.

<dt>

0 (0X0)
</dt> <dd>

La reconexión automática está deshabilitada.

</dd> <dt>

1 (0x1)
</dt> <dd>

La reconexión automática está habilitada.

</dd> </dl>

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**EnableDFSS**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si la programación dinámica de recursos compartidos (DFSS) está habilitada o deshabilitada. Puede ser uno de los valores siguientes.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

<dt>

0
</dt> <dd>

DFSS está deshabilitado.

</dd> <dt>

1
</dt> <dd>

DFSS está habilitado.

</dd> </dl>

</dd> <dt>

**EnableDiskFSS**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si está habilitada la programación de recursos compartidos de disco.

<dt>

0 (0X0)
</dt> <dd>

La programación de la cuota de disco equilibrada está deshabilitada.

</dd> <dt>

1 (0x1)
</dt> <dd>

Está habilitada la programación de recursos compartidos de disco.

</dd> </dl>

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**EnableNetworkFSS**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si está habilitada la programación de recursos compartidos de red.

<dt>

0 (0X0)
</dt> <dd>

La programación de proporcionalidad equilibrada de red está deshabilitada.

</dd> <dt>

1 (0x1)
</dt> <dd>

La programación de proporcionalidad equilibrada de red está habilitada.

</dd> </dl>

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**EnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si la Escritorio remoto MSI está habilitada o deshabilitada.

<dt>

0 (0X0)
</dt> <dd>

Disabled

</dd> <dt>

1 (0x1)
</dt> <dd>

habilitado

</dd> </dl>

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**FallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el controlador de impresora al que se va a retrasar.

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No dirvers de reserva = 0** (0)


</dt> <dd>

No hay controladores de reserva.

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Mejor estimación = 1** (1)


</dt> <dd>

Mejor aproximación.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Mejor estimación, si no se encuentra ninguna coincidencia, reserva a PCL = 2** (2)


</dt> <dd>

Mejor aproximación. Si no se encuentra ninguna coincidencia, retroceder a Hewlett-Packard el lenguaje de control de impresoras (PCL).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Mejor estimación, si no se encuentra ninguna coincidencia, reserva a PS = 3** (3)


</dt> <dd>

Mejor aproximación. Si no se encuentra ninguna coincidencia, retroceder a PostScript (PS).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Mejor suposición, si no se encuentra ninguna coincidencia, mostrar los controladores PCL y PS = 4** (4)


</dt> <dd>

Mejor aproximación. Si no se encuentra ninguna coincidencia, muestre los controladores PS y PCL.

</dd> </dl>

</dd> <dt>

**GetCapabilitiesID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

IDENTIFICADOR de funcionalidad del proveedor.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Directorio raíz del equipo.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Fecha en que se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**LicensingDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del modo de licencia.

</dd> <dt>

**LicensingName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del modo de licencia.

</dd> <dt>

**LicensingType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de licencia para el modo de servidor especificado.

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Terminal Server personal** (0)


</dt> <dd>

Servidor host de sesión de escritorio remoto personal.

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Escritorio remoto para la administración** (1)


</dt> <dd>

Escritorio remoto para la administración.

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Por dispositivo** (2)


</dt> <dd>

Por dispositivo. Válido para los servidores de aplicaciones.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (3)


</dt> <dd>

Por usuario. Válido para los servidores de aplicaciones.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (4)


</dt> <dd>

No configurado.

</dd> </dl>

</dd> <dt>

**LimitedUserSessions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si la característica para limitar el número de sesiones activas e inactivas que se permiten en un servidor host de sesión de escritorio remoto está habilitada. Por ejemplo, puede que desee establecer **LimitedUserSessions** para garantizar el cumplimiento de las licencias para una aplicación concreta que está instalada en el servidor host de sesión de escritorio remoto. O bien, puede que desee limitar el número máximo de sesiones en un servidor host de sesión de escritorio remoto en una granja de servidores con equilibrio de carga, de modo que el servidor no se sobrecargue si se produce un error en otro servidor de la granja.

> [!Note]
>
> La sesión que se usa para conectarse al servidor con fines administrativos no se ve afectada por **LimitedUserSessions**.
>
> En una granja de servidores host de sesión de escritorio remoto, si un usuario supera el límite de sesión, la sesión se dirigirá a otro servidor mediante el equilibrio de carga del agente de conexión a escritorio remoto. Si el servidor es un servidor independiente, el usuario no podrá conectarse.
>
> Debido a la sesión que se usa para conectarse al servidor con fines administrativos, y a la temporización de la aplicación del número de sesiones durante el ciclo de inicio de sesión, se recomienda establecer **LimitedUserSessions** en un valor que sea ligeramente inferior al límite físico para el número de sesiones en un servidor.
>
> La propiedad **LimitedUserSessions** solo es válida si está instalado el servicio de rol host de sesión de escritorio remoto.

 

<dt>

0
</dt> <dd>

Esta función está deshabilitada.

</dd> <dt>

1 o superior
</dt> <dd>

Un valor de uno o más representa el número máximo de sesiones (activas e inactivas) que se permiten en el servidor host de sesión de escritorio remoto.

</dd> </dl>

</dd> <dt>

**Inicios**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se permiten las nuevas sesiones. Esta configuración no afecta a la configuración existente.

<dt>

0
</dt> <dd>

Se permiten nuevas sesiones.

</dd> <dt>

1
</dt> <dd>

No se permiten nuevas sesiones.

</dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**NetworkFSSCatchAllWeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica el peso de la cuota equitativa predeterminada de red para el tráfico de red comodín. Los valores válidos son de 1 a 9.

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**NetworkFSSLocalSystemWeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica el peso de la cuota equitativa predeterminada de red para un proceso del sistema local. Los valores válidos son de 1 a 9.

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**NetworkFSSUserSessionWeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica el peso de la cuota equitativa predeterminada de red para una sesión de usuario. Los valores válidos son de 1 a 9.

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**PolicySourceAllowTSConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **AllowTSConnections** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceConfiguredLicenseServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si los servidores de licencias devueltos por el método [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) están configurados por el servidor o por la Directiva de grupo.

**Windows Server 2008:** Esta propiedad no está disponible.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceDeleteTempFolders**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **DeleteTempFolders** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceDirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no está disponible.

**Windows Server 2008:** Indica si la propiedad **DirectConnectLicenseServers** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceDisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad no es compatible.

**Windows Server 2008:** Determina si la propiedad **DisableForcibleLogoff** está configurada por el servidor o por la Directiva de grupo.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo.

</dd> </dl>

</dd> <dt>

**PolicySourceEnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **EnableAutomaticReconnection** está configurada por el servidor o la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**PolicySourceEnableDFSS**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **EnableDFSS** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**PolicySourceEnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **EnableRemoteDesktopMSI** está configurada por el servidor o la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**PolicySourceFallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **FallbackPrintDriverType** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceHomeDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **HomeDirectory** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceLicensingType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **LicensingType** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceProfilePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **ProfilePath** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceRedirectSmartCards**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **RedirectSmartCards** está configurada por el servidor o la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**PolicySourceSingleSession**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **SingleSession** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceTimeZoneRedirection**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **TimeZoneRedirection** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceUseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **UseRDEasyPrintDriver** está configurada por el servidor o la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**PolicySourceUseTempFolders**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **UseTempFolders** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PossibleLicensingTypes**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**mapa de bits**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("personal Terminal Server", "escritorio remoto para administración", "por dispositivo", "por usuario", "sin configurar")
</dt> </dl>

Máscara de máscara que especifica los tipos de licencia que están disponibles. Puede ser una combinación de uno o varios de los valores siguientes.

<dt>

1 (0x1)
</dt> <dd>

Se admiten licencias de servidor host de sesión de escritorio remoto personal.

</dd> <dt>

2 (0X2)
</dt> <dd>

Se admiten Escritorio remoto licencias.

</dd> <dt>

4 (0x4)
</dt> <dd>

Se admiten licencias por dispositivo.

</dd> <dt>

8 (0x8)
</dt> <dd>

Se admiten licencias por usuario.

</dd> </dl>

</dd> <dt>

**ProfilePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del perfil para el equipo.

</dd> <dt>

**RedirectSmartCards**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se permite la redirección de dispositivos de tarjeta inteligente en una sesión remota.

<dt>

0 (0X0)
</dt> <dd>

No se permite la redirección de dispositivos de tarjeta inteligente.

</dd> <dt>

1 (0x1)
</dt> <dd>

Se permite el redireccionamiento de dispositivos de tarjeta inteligente.

</dd> </dl>

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del servidor host de sesión de escritorio remoto cuyas propiedades son de interés.

</dd> <dt>

**SessionBrokerDrainMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El modo de inicio de sesión de usuario del agente de conexión a escritorio remoto.

<dt>

0
</dt> <dd>

Permitir todas las conexiones.

</dd> <dt>

1
</dt> <dd>

Permitir las reconexiones, pero impedir nuevos inicios de sesión hasta que se reinicie el servidor.

</dd> <dt>

2
</dt> <dd>

Permitir las reconexiones, pero impedir nuevos inicios de sesión.

</dd> </dl>

</dd> <dt>

**SingleSession**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se permiten una o varias sesiones de Servicios de Escritorio remoto por usuario.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

Se permite más de una sesión por usuario.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

Solo se permite una sesión por usuario.

</dd> </dl>

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios Estados operativos y no operativos. Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo). Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio". El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

<dt>



 ("Correcto")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconocido")


</dt> <dd></dd> <dt>



 ("Pred FAIL")


</dt> <dd></dd> <dt>



 ("Iniciando")


</dt> <dd></dd> <dt>



 ("Deteniéndose")


</dt> <dd></dd> <dt>



 ("Servicio")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalServerMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Modo de funcionamiento del servidor host de sesión de escritorio remoto del servicio Servicios de Escritorio remoto. Este modo controla las directivas de licencias que son aplicables y si están habilitadas las características de compatibilidad de aplicaciones.

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)


</dt> <dd>

El servidor funciona como un servidor de aplicaciones.

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)


</dt> <dd>

La sesión se administra de forma remota.

</dd> </dl>

</dd> <dt>

**TimeZoneRedirection**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si el equipo cliente puede redirigir su configuración de zona horaria a la sesión de Servicios de Escritorio remoto.

<dt>

0
</dt> <dd>

La redirección está deshabilitada.

</dd> <dt>

1
</dt> <dd>

La redirección está habilitada.

</dd> </dl>

</dd> <dt>

**UseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si el controlador de impresora Easy Print de Escritorio remoto se utiliza en primer lugar para instalar todas las impresoras de cliente.

<dt>

0
</dt> <dd>

El servidor host de sesión de escritorio remoto intenta encontrar un controlador de impresora adecuado para instalar la impresora de cliente. Si el servidor host de sesión de escritorio remoto no tiene un controlador de impresora que coincida con la impresora de cliente, el servidor intenta usar el controlador de Easy Print de Escritorio remoto para instalar la impresora de cliente.

</dd> <dt>

1
</dt> <dd>

El servidor host de sesión de escritorio remoto primero intenta usar el controlador de impresora Easy Print de Escritorio remoto para instalar todas las impresoras cliente. Si por alguna razón no se puede usar el controlador de impresora Easy Print de Escritorio remoto, se usa un controlador de impresora en el servidor host de sesión de escritorio remoto que coincida con la impresora cliente.

</dd> </dl>

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**UserPermission**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si cada sesión de usuario tiene una seguridad estricta o relajada.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La seguridad es estrecha.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La seguridad es relajada.

</dd> </dl>

</dd> <dt>

**UseTempFolders**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si los directorios temporales se crean y se eliminan por sesión.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Los directorios temporales no se crean y eliminan para cada sesión. Se crea uno para la primera sesión y nunca se elimina.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Los directorios temporales se crean y se eliminan para cada sesión.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Win32 \_ TerminalServiceSetting** está asociado a [**Win32 \_ TerminalService**](win32-terminalservice.md) como la propiedad **Setting** de la [**Asociación \_ TerminalServiceToSetting de Win32**](win32-terminalservicetosetting.md) .

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) está asociado al [**\_ terminal de Win32**](win32-terminal.md) como la propiedad de **configuración** de la Asociación [**\_ TerminalTerminalSetting de Win32**](win32-terminalterminalsetting.md) .

Para conectarse al espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes. En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C. En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de seis.

En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[**\_Terminal Win32**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dt>

[**Configuración de CIM \_**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

