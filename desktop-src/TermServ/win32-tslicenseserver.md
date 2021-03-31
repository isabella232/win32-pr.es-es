---
title: Win32_TSLicenseServer (clase)
description: Proporciona métodos y propiedades para ver y configurar licencias de Escritorio remoto (licencias de escritorio remoto) en un servidor de licencias de Escritorio remoto.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996670"
---
# <a name="win32_tslicenseserver-class"></a>\_Clase Win32 TSLicenseServer

Proporciona métodos y propiedades para ver y configurar licencias de Escritorio remoto (licencias de escritorio remoto) en un servidor de licencias de Escritorio remoto.

## <a name="syntax"></a>Sintaxis

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSLicenseServer de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TSLicenseServer** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | Activa el servidor de licencias de Escritorio remoto mediante un identificador de servidor de licencias Escritorio remoto que se obtiene a través del teléfono o Internet.<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Activa el servidor de licencias de Escritorio remoto automáticamente a través de Internet. Las propiedades **FirstName**, **LastName**, **Company** y **CountryRegion** no deben estar vacías cuando se llama a este método o se producirá un error en el método.<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Agrega el servidor de licencias de Escritorio remoto al grupo servidores de licencias de Escritorio remoto en un controlador de dominio del mismo dominio que el servidor de licencias.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Cambia el ámbito de detección del servidor de licencias de Escritorio remoto.<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | No se admite este método.<br/> **Windows server 2008 R2 y Windows server 2008:** Crea el grupo local de Terminal Server equipos en el servidor de licencias de Escritorio remoto.<br/>                                               |
| [**DeactivateServer**](deactivateserver-win32-tslicenseserver.md)                       | Desactiva el servidor de licencias de Escritorio remoto mediante un código de confirmación que se recibe a través del teléfono.<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | Desactiva el servidor de licencias de Escritorio remoto a través de Internet. Las propiedades **FirstName** y **LastName** no deben estar vacías cuando se llama a este método o se producirá un error en el método.<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | Recupera el estado de activación actual.<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | Recupera un identificador de servidor de licencias Escritorio remoto si el servidor está activado actualmente.<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Recupera si el servidor de licencias Escritorio remoto es miembro del grupo servidores de licencias Escritorio remoto en un controlador de dominio de un dominio determinado.<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | Recupera si la concesión de licencias de escritorio remoto está instalada en un controlador de dominio.<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Recupera si está habilitada la configuración de directiva de grupo "impedir actualización de licencia" en el servidor de licencias de Escritorio remoto.<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | Recupera si el servidor de licencias de Escritorio remoto se publica en Active Directory Domain Services (AD DS).<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Recupera si el servidor de licencias de Escritorio remoto está registrado como punto de conexión de servicio en Active Directory Domain Services.<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Recupera si el valor de directiva de grupo "grupo de seguridad del servidor de licencias" está habilitado en el servidor de licencias de Escritorio remoto.<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Recupera si un servidor host de sesión de escritorio remoto tiene permiso para solicitar Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) del servidor de licencias de Escritorio remoto.<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | No se admite este método.<br/> **Windows server 2008 R2 y Windows server 2008:** Recupera si el grupo local de equipos Terminal Server existe en el servidor de licencias de Escritorio remoto.<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | Recupera si un servidor host de sesión de escritorio remoto es miembro del grupo local de Terminal Server equipos en el servidor de licencias de Escritorio remoto.<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | Publica el servidor de licencias de Escritorio remoto en AD DS.<br/>                                                                                                                                                                              |
| [**ReactivateServer**](reactivateserver-win32-tslicenseserver.md)                       | Reactiva el servidor de licencias de Escritorio remoto mediante un nuevo identificador de servidor de licencias Escritorio remoto que se obtiene a través del teléfono o Internet.<br/>                                                                                     |
| [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | Reactiva el servidor de licencias de Escritorio remoto a través de Internet. Las propiedades **FirstName** y **LastName** no deben estar vacías cuando se llama a este método o se producirá un error en el método.<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | Registra el servidor de licencias de Escritorio remoto como punto de conexión de servicio en Active Directory Domain Services.<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Quita el servidor de licencias de Escritorio remoto del grupo servidores de licencias de Escritorio remoto en un controlador de dominio del mismo dominio que el servidor de licencias.<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | No se admite este método.<br/> **Windows server 2008 R2 y Windows server 2008:** Quita el grupo local de Terminal Server equipos del servidor de licencias de Escritorio remoto.<br/>                                             |
| [**UnpublishLS**](unpublishls-win32-tslicenseserver.md)                                 | Anula la publicación de un servidor de licencias de Escritorio remoto de AD DS.<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Quita el servidor de licencias de Escritorio remoto como punto de conexión de servicio en Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseServer de Win32** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Dirección postal del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . (Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).

</dd> <dt>

**Ciudad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Ciudad del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . (Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).

</dd> <dt>

**Company**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Empresa del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa (y se requiere) cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .

</dd> <dt>

**CountryRegion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

País o región del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa (y se requiere) cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de la base de datos de licencias RDS.

</dd> <dt>

**Correo electrónico**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Dirección de correo electrónico del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa cuando se llama a los métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) . (Esta propiedad es opcional para estas llamadas a métodos).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa (y se requiere) cuando se llama a los métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .

</dd> <dt>

**Apellidos**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Apellido del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa (y se requiere) cuando se llama a los métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Unidad organizativa del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa cuando se llama a [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . (Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Código postal del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . (Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

IDENTIFICADOR del producto del servidor de licencias de Escritorio remoto.

</dd> <dt>

**ServerRole**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe el ámbito de licencias para el servidor de licencias de Escritorio remoto dentro de la organización.

<dt>

0
</dt> <dd>

Los servidores host de sesión de escritorio remoto del mismo grupo de trabajo pueden detectar el servidor de licencias.

</dd> <dt>

1
</dt> <dd>

Los servidores host de sesión de escritorio remoto del mismo dominio pueden detectar el servidor de licencias.

</dd> <dt>

2
</dt> <dd>

Los servidores host de sesión de escritorio remoto de varios dominios del mismo bosque pueden detectar el servidor de licencias.

</dd> </dl>

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Estado del contacto para la concesión de licencias de escritorio remoto. Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . (Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión del servidor de licencias de Escritorio remoto.

</dd> <dt>

**NúmeroDeVersión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de versión del servidor de licencias de Escritorio remoto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta clase es una clase [Singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) y solo puede tener una instancia. Todos los métodos contenidos en esta clase son estáticos.

Para usar esta clase, debe ser miembro del grupo administradores. Si el autor de la llamada no es miembro del grupo administradores, las propiedades devueltas estarán vacías.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

