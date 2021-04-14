---
title: Clase Win32_TSLicenseKeyPack
description: Proporciona métodos y propiedades para ver e instalar los paquetes de claves de licencia de Servicios de Escritorio remoto.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseKeyPack de clase, se describe
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
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533789"
---
# <a name="win32_tslicensekeypack-class"></a>\_Clase Win32 TSLicenseKeyPack

Proporciona métodos y propiedades para ver e instalar los paquetes de claves de licencia de Servicios de Escritorio remoto.

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

La clase **Win32 \_ TSLicenseKeyPack** tiene estos métodos.



| Método                                                                                                        | Descripción                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertLicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | Convierte las licencias en el paquete de claves actual.<br/>                                                                                                                                                                                 |
| [**ImportAgreementLicenseKeyPack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.<br/> |
| [**ImportLicenseKeyPackOffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia de Servicios de Escritorio remoto que utiliza un identificador de licencia recibido a través de Internet o del teléfono.<br/>                                               |
| [**ImportOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Open Servicios de Escritorio remoto.<br/>                                                                                                                 |
| [**ImportRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal minorista.<br/>                                                                                   |
| [**InstallAgreementLicenseKeyPack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de una licencia de contrato.<br/>                                                                                                                           |
| [**InstallLicenseKeyPack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | Instala un paquete de claves de licencia Servicios de Escritorio remoto que utiliza un identificador de paquete de claves de licencia recibido a través de Internet o del teléfono.<br/>                                                                                          |
| [**InstallOpenLicenseKeyPack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia abierto.<br/>                                                                                                                      |
| [**InstallRetailPurchaseLicenseKeyPack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de una tienda de venta directa.<br/>                                                                                                                                 |
| [**ReinstallAgreementLicenseKeyPack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.<br/>                                           |
| [**ReinstallLicenseKeyPackOffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto que usa el identificador de licencia que se recibió a través de Internet o el teléfono.<br/>                                                                                       |
| [**ReinstallOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | Vuelve a instalar una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.<br/>                                                                                                                                                           |
| [**ReinstallRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal de venta directa.<br/>                                                                                                                             |
| [**RemoveLicensesWithIdCount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | Quita el número especificado de licencias de Servicios de Escritorio remoto del paquete de claves especificado.<br/>                                                                                                                                  |
| [**UninstallLicenseKeyPack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | Desinstala un paquete de claves de licencia de Servicios de Escritorio remoto.<br/>                                                                                                                                                                         |
| [**UninstallLicenseKeyPackWithId**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | Desinstala el paquete de claves de licencia de Servicios de Escritorio remoto con el identificador de paquete de claves especificado.<br/>                                                                                                                                |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseKeyPack de Win32** tiene estas propiedades.

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**mapa de bits**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("sesión de RD", "sesión de VDI", "Calista", "asociados de VDI")
</dt> </dl>

Calificador para derechos de acceso de paquete de claves de licencias TS

</dd> <dt>

**AvailableLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de licencias disponibles en el paquete de claves de licencia de Servicios de Escritorio remoto.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del paquete de claves de licencia de Servicios de Escritorio remoto.

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha de expiración de la Servicios de Escritorio remoto paquete de claves de licencia.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de licencias emitidas en el paquete de claves de licencia de Servicios de Escritorio remoto.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador del paquete de claves de licencia de Servicios de Escritorio remoto.

</dd> <dt>

**KeyPackType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de paquete de claves para el servidor de licencias de Escritorio remoto.

| Value | Descripción |
|-------|-------------|
| 0 | No se conoce el tipo de paquete de claves de licencia Servicios de Escritorio remoto. |
| 1 | El tipo de paquete de claves de licencia Servicios de Escritorio remoto es una compra comercial. |
| 2 | El tipo de paquete de claves de licencia Servicios de Escritorio remoto es una compra por volumen. |
| 3 | El tipo de paquete de claves de licencia Servicios de Escritorio remoto es una licencia simultánea. |
| 4 | El tipo de paquete de claves de licencia Servicios de Escritorio remoto es temporal. |
| 5 | El tipo de paquete de claves de licencia Servicios de Escritorio remoto es una licencia abierta. |
| 6 | No se admite. |

**ProductType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de producto del paquete de claves de licencia de Servicios de Escritorio remoto.

| Value | Descripción |
|-------|-------------|
| 0 | El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo. Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia. |
| 1 | El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario. Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia. |
| 2 | Este tipo de producto no es válido. |

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.

| Value | Descripción |
|-------|-------------|
| "Windows Server 2012" | En esta licencia solo se admiten servidores que ejecuten Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008. |
| "Windows Server 7" | Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008 R2 o Windows Server 2008. |
| "Windows Server 2008" | Este paquete de claves solo admite servidores que ejecuten Windows Server 2008. |

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de la versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.

| Value | Descripción |
|-------|-------------|
| 0 | No compatible |
| 1 | No compatible |
| 2 | Windows Server 2008 |
| 3 | Windows Server 2008 R2 |
| 4 | Windows Server 2012 o Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

**TotalLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de licencias en el paquete de claves de licencia de Servicios de Escritorio remoto.

</dd> <dt>

**TypeAndModel**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificador para el modelo y el tipo de paquete de claves de licencias de TS. Ejemplos: licencias por suscripción de VDI por dispositivo, CAL por usuario de TS

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar esta clase, debe ser miembro del grupo administradores.

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

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

