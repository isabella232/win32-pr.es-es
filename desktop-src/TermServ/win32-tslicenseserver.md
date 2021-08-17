---
title: Win32_TSLicenseServer clase
description: Proporciona métodos y propiedades para ver y configurar Escritorio remoto licencias (licencias de Escritorio remoto) en un servidor Escritorio remoto licencias.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer clase Servicios de Escritorio remoto
- Win32_TSLicenseServer clase Servicios de Escritorio remoto , descrita
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
ms.openlocfilehash: 0f7c73c1d1a48bbc76b4988afca8a07fd9ce505d0633c74f67306901259d9f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126515"
---
# <a name="win32_tslicenseserver-class"></a>Clase \_ TSLicenseServer de Win32

Proporciona métodos y propiedades para ver y configurar Escritorio remoto licencias (licencias de Escritorio remoto) en un servidor Escritorio remoto licencias.

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

La **clase \_ TSLicenseServer de Win32** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | Activa el Escritorio remoto de licencias mediante un Escritorio remoto de servidor de licencias que se obtiene por teléfono o Internet.<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Activa el Escritorio remoto de licencias automáticamente a través de Internet. Las **propiedades FirstName**, **LastName**, **Company** y **CountryRegion** no deben estar vacías cuando se llama a este método o se producirá un error en el método.<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Agrega el Escritorio remoto de licencias al grupo Escritorio remoto de licencias en un controlador de dominio en el mismo dominio que el servidor de licencias.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Cambia el ámbito de detección del Escritorio remoto de licencias.<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | No se admite este método.<br/> **Windows Server 2008 R2 y Windows Server 2008:** Crea el grupo local Equipos de Terminal Server en Escritorio remoto servidor de licencias.<br/>                                               |
| [**DeactivateServer**](deactivateserver-win32-tslicenseserver.md)                       | Desactiva el Escritorio remoto de licencias mediante un código de confirmación que se recibe por teléfono.<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | Desactiva el servidor Escritorio remoto licencias a través de Internet. Las **propiedades FirstName** y **LastName** no deben estar vacías cuando se llama a este método o se producirá un error en el método.<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | Recupera el estado de activación actual.<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | Recupera un identificador Escritorio remoto servidor de licencias si el servidor está activado actualmente.<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Recupera si el Escritorio remoto de licencias es miembro del grupo Escritorio remoto servidores de licencias de un controlador de dominio en un dominio determinado.<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | Recupera si la licencia de Escritorio remoto está instalada en un controlador de dominio.<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Recupera si la configuración de directiva de grupo "impedir la actualización de licencias" está habilitada en Escritorio remoto servidor de licencias.<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | Recupera si el Escritorio remoto de licencias se publica en Active Directory Domain Services (AD DS).<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Recupera si el servidor Escritorio remoto licencia está registrado como punto de conexión de servicio en Active Directory Domain Services.<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Recupera si la configuración de directiva de grupo "grupo de seguridad del servidor de licencias" está habilitada en Escritorio remoto servidor de licencias.<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Recupera si un servidor host de sesión de Escritorio remoto puede solicitar Servicios de Escritorio remoto de acceso de cliente (CAL de RDS) desde el servidor de Escritorio remoto de licencias.<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | No se admite este método.<br/> **Windows Server 2008 R2 y Windows Server 2008:** Recupera si el grupo local Equipos de Terminal Server existe en el Escritorio remoto de licencias.<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | Recupera si un servidor host de sesión de Escritorio remoto es miembro del grupo local Equipos de Terminal Server en Escritorio remoto servidor de licencias.<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | Publica el servidor Escritorio remoto licencias en AD DS.<br/>                                                                                                                                                                              |
| [**ReactivateServer**](reactivateserver-win32-tslicenseserver.md)                       | Vuelve a activar el Escritorio remoto de licencias mediante un nuevo Escritorio remoto de servidor de licencias que se obtiene a través del teléfono o Internet.<br/>                                                                                     |
| [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | Vuelve a activar el Escritorio remoto de licencias a través de Internet. Las **propiedades FirstName** y **LastName** no deben estar vacías cuando se llama a este método o se producirá un error en el método.<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | Registra el servidor Escritorio remoto licencia como punto de conexión de servicio en Active Directory Domain Services.<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Quita el servidor Escritorio remoto licencias del grupo Escritorio remoto de licencias de un controlador de dominio en el mismo dominio que el servidor de licencias.<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | No se admite este método.<br/> **Windows Server 2008 R2 y Windows Server 2008:** Quita el grupo local Equipos de Terminal Server del Escritorio remoto de licencias.<br/>                                             |
| [**UnpublishLS**](unpublishls-win32-tslicenseserver.md)                                 | Despublica un Escritorio remoto de licencias de AD DS.<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Quita el servidor Escritorio remoto licencias como punto de conexión de servicio en Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseServer de Win32** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Dirección postal del contacto para licencias de Escritorio remoto. Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) (Esta propiedad es opcional cuando se usa **el método ActivateServerAutomatic).**

</dd> <dt>

**Ciudad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Ciudad del contacto para licencias de Escritorio remoto. Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) (Esta propiedad es opcional cuando se usa **el método ActivateServerAutomatic).**

</dd> <dt>

**Company**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Empresa del contacto para licencias de Escritorio remoto. Esta propiedad se usa (y es necesaria) cuando se llama al [**método ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md)

</dd> <dt>

**CountryRegion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

País o región del contacto para licencias de Escritorio remoto. Esta propiedad se usa (y es necesaria) cuando se llama al [**método ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md)

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de la base de datos de licencias de RDS.

</dd> <dt>

**Correo electrónico**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Dirección de correo electrónico del contacto para licencias de Escritorio remoto. Esta propiedad se usa cuando se llama a los métodos [**ActivateServerAutomatic,**](activateserverautomatic-win32-tslicenseserver.md) [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic.**](deactivateserverautomatic-win32-tslicenseserver.md) (Esta propiedad es opcional para estas llamadas de método).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Nombre del contacto para licencias de Escritorio remoto. Esta propiedad se usa (y es necesaria) cuando se llama a los métodos [**ActivateServerAutomatic,**](activateserverautomatic-win32-tslicenseserver.md) [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic.**](deactivateserverautomatic-win32-tslicenseserver.md)

</dd> <dt>

**Apellidos**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Apellidos del contacto para licencias de Escritorio remoto. Esta propiedad se usa (y es necesaria) cuando se llama a los métodos [**ActivateServerAutomatic,**](activateserverautomatic-win32-tslicenseserver.md) [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic.**](deactivateserverautomatic-win32-tslicenseserver.md)

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Unidad organizativa del contacto para licencias de Escritorio remoto. Esta propiedad se usa cuando se llama [**a ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) (Esta propiedad es opcional cuando se usa **el método ActivateServerAutomatic).**

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Código postal del contacto para licencias de Escritorio remoto. Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) (Esta propiedad es opcional cuando se usa **el método ActivateServerAutomatic).**

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Id. de producto del Escritorio remoto de licencias.

</dd> <dt>

**ServerRole**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe el ámbito de licencia para el Escritorio remoto de licencias dentro de la organización.

<dt>

0
</dt> <dd>

Los servidores host de sesión de Escritorio remoto del mismo grupo de trabajo pueden detectar el servidor de licencias.

</dd> <dt>

1
</dt> <dd>

Los servidores host de sesión de Escritorio remoto del mismo dominio pueden detectar el servidor de licencias.

</dd> <dt>

2
</dt> <dd>

Los servidores host de sesión de Escritorio remoto de varios dominios del mismo bosque pueden detectar el servidor de licencias.

</dd> </dl>

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Estado del contacto para licencias de Escritorio remoto. Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) (Esta propiedad es opcional cuando se usa **el método ActivateServerAutomatic).**

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión del servidor Escritorio remoto licencia.

</dd> <dt>

**VersionNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de versión del Escritorio remoto de licencias.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta clase es una [clase singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) y solo puede tener una instancia. Todos los métodos incluidos en esta clase son estáticos.

Debe ser miembro del grupo Administradores para usar esta clase. Si el autor de la llamada no es miembro del grupo Administradores, las propiedades devueltas estarán vacías.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
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

 

