---
title: Clase Win32_TSLicenseKeyPack
description: Proporciona métodos y propiedades para ver e instalar Servicios de Escritorio remoto de claves de licencia.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7927270f262d0a66722660bf4b2c8f15cf75f49bb807abcff604af9edf58d99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137818"
---
# <a name="win32_tslicensekeypack-class"></a>Clase \_ TSLicenseKeyPack de Win32

Proporciona métodos y propiedades para ver e instalar Servicios de Escritorio remoto de claves de licencia.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSLicenseKeyPack de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSLicenseKeyPack de Win32** tiene estos métodos.



| Método                                                                                                        | Descripción                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertLicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | Convierte las licencias del paquete de claves actual.<br/>                                                                                                                                                                                 |
| [**ImportAgreementLicenseKeyPack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia de Servicios de Escritorio remoto que se compró a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.<br/> |
| [**ImportLicenseKeyPackOffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | Importa, desde otro servidor Escritorio remoto licencias, un Servicios de Escritorio remoto de claves de licencia que usa un identificador de licencia que se recibió a través de Internet o el teléfono.<br/>                                               |
| [**ImportOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | Importa, desde otro servidor Escritorio remoto licencias, un paquete de claves de licencia Servicios de Escritorio remoto licencia abierta.<br/>                                                                                                                 |
| [**ImportRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | Importa, desde otro servidor Escritorio remoto licencias, un Servicios de Escritorio remoto de claves de licencia que se compró a través de un canal comercial.<br/>                                                                                   |
| [**InstallAgreementLicenseKeyPack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | Instala un paquete Servicios de Escritorio remoto de claves de licencia que se compró a través de una licencia de contrato.<br/>                                                                                                                           |
| [**InstallLicenseKeyPack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | Instala un Servicios de Escritorio remoto de claves de licencia que usa un identificador de paquete de claves de licencia que se recibió a través de Internet o el teléfono.<br/>                                                                                          |
| [**InstallOpenLicenseKeyPack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | Instala un paquete Servicios de Escritorio remoto de claves de licencia que se compró a través de un contrato de licencia abierto.<br/>                                                                                                                      |
| [**InstallRetailPurchaseLicenseKeyPack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | Instala un paquete Servicios de Escritorio remoto de claves de licencia que se compró a través de una tienda minorista.<br/>                                                                                                                                 |
| [**ReinstallAgreementLicenseKeyPack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | Vuelve a instalar un Servicios de Escritorio remoto de claves de licencia que se compró a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.<br/>                                           |
| [**ReinstallLicenseKeyPackOffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | Vuelve a instalar un Servicios de Escritorio remoto de claves de licencia que usa el identificador de licencia que se recibió a través de Internet o el teléfono.<br/>                                                                                       |
| [**ReinstallOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | Vuelve a instalar un paquete de claves Servicios de Escritorio remoto licencia abierta.<br/>                                                                                                                                                           |
| [**ReinstallRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | Vuelve a instalar un Servicios de Escritorio remoto de claves de licencia que se compró a través de un canal comercial.<br/>                                                                                                                             |
| [**RemoveLicensesWithIdCount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | Quita el número especificado de licencias Servicios de Escritorio remoto del paquete de claves especificado.<br/>                                                                                                                                  |
| [**UninstallLicenseKeyPack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | Desinstala un paquete Servicios de Escritorio remoto de claves de licencia.<br/>                                                                                                                                                                         |
| [**UninstallLicenseKeyPackWithId**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | Desinstala el Servicios de Escritorio remoto de claves de licencia con el identificador del paquete de claves especificado.<br/>                                                                                                                                |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseKeyPack de Win32** tiene estas propiedades.

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sesión de Escritorio remoto", "Sesión de VDI", "Calista", "Asociados de VDI")
</dt> </dl>

Calificador de los derechos de acceso del paquete de claves de licencias de TS

</dd> <dt>

**AvailableLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de licencias disponibles en el paquete Servicios de Escritorio remoto de claves de licencia.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del paquete Servicios de Escritorio remoto de claves de licencia.

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha de expiración del paquete Servicios de Escritorio remoto de claves de licencia.

</dd> <dt>

**Licencias emitidas**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de licencias emitidas en el paquete Servicios de Escritorio remoto de claves de licencia.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador del paquete Servicios de Escritorio remoto de claves de licencia.

</dd> <dt>

**KeyPackType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de paquete de claves para el Escritorio remoto de licencias.

| Value | Descripción |
|-------|-------------|
| 0 | Se desconoce Servicios de Escritorio remoto tipo de paquete de claves de licencia. |
| 1 | El Servicios de Escritorio remoto de paquete de claves de licencia es una compra comercial. |
| 2 | El Servicios de Escritorio remoto de paquete de claves de licencia es una compra por volumen. |
| 3 | El Servicios de Escritorio remoto de paquete de claves de licencia es una licencia simultánea. |
| 4 | El Servicios de Escritorio remoto del paquete de claves de licencia es temporal. |
| 5 | El Servicios de Escritorio remoto de paquete de claves de licencia es una licencia abierta. |
| 6 | No compatible. |

**ProductType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de producto del paquete Servicios de Escritorio remoto de claves de licencia.

| Value | Descripción |
|-------|-------------|
| 0 | El Servicios de Escritorio remoto de producto del paquete de claves de licencia es por dispositivo. Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de Escritorio remoto debe tener una licencia. |
| 1 | El Servicios de Escritorio remoto de producto del paquete de claves de licencia es por usuario. Por lo tanto, cada usuario que se conecta al servidor host de sesión de Escritorio remoto debe tener una licencia. |
| 2 | Este tipo de producto no es válido. |

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión del producto para el paquete Servicios de Escritorio remoto de claves de licencia.

| Value | Descripción |
|-------|-------------|
| "Windows Server 2012" | Solo los servidores que Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 son compatibles con esta licencia. |
| "Windows Server 7" | Solo los servidores que Windows Server 2008 R2 o Windows Server 2008 son compatibles con esta licencia. |
| "Windows Server 2008" | Solo los servidores que Windows Server 2008 son compatibles con este paquete de claves. |

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de versión del producto para el Servicios de Escritorio remoto de claves de licencia.

| Value | Descripción |
|-------|-------------|
| 0 | No compatible |
| 1 | No compatible |
| 2 | Windows Server 2008 |
| 3 | Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

**TotalLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de licencias del paquete de claves Servicios de Escritorio remoto licencia.

</dd> <dt>

**TypeAndModel**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificador para el modelo y el tipo del paquete de claves de licencias de TS. Ejemplos: licencia de suscripción de VDI por dispositivo, CAL de TS por usuario

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para usar esta clase.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**TSLicenseReport de Win32 \_**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**TSLicenseServer de Win32 \_**](win32-tslicenseserver.md)
</dt> </dl>

 

