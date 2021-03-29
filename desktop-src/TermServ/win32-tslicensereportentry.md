---
title: Win32_TSLicenseReportEntry (clase)
description: Proporciona detalles de la licencia de acceso de cliente por usuario Servicios de Escritorio remoto emitida (RDS \ 160; CAL por usuario).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReportEntry de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421960"
---
# <a name="win32_tslicensereportentry-class"></a>\_Clase Win32 TSLicenseReportEntry

Proporciona detalles de la licencia de acceso de cliente por usuario de Servicios de Escritorio remoto emitida (CAL por usuario de RDS).

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSLicenseReportEntry de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseReportEntry de Win32** tiene estas propiedades.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de CAL emitida. Será uno de los valores siguientes.

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no se admite.

"CAL por dispositivo de TS integrada"

"CAL por dispositivo de TS"

"CAL de conector de Internet de TS"

"CAL por usuario de TS"

"CAL por dispositivo de TS o RDS"

"CAL por usuario de TS o RDS"

"Licencia de suscripción por dispositivo de VDI Standard Suite"

"Licencia de suscripción por dispositivo de VDI Premium Suite"

"CAL por dispositivo de RDS"

"CAL por usuario de RDS"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha de expiración de la licencia que se emitió para el usuario.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión de Servicios de Escritorio remoto para la que se emitió la CAL por usuario de RDS.

<dt>

"Windows Server 2012"
</dt> <dd>

En esta licencia solo se admiten servidores que ejecuten Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008 R2 o Windows Server 2008.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de la versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.

<dt>

4
</dt> <dd>

Windows Server 2012

</dd> <dt>

3
</dt> <dd>

Windows Server 2008 R2

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> <dt>

1
</dt> <dd>

No se admite.

</dd> <dt>

0
</dt> <dd>

No se admite.

</dd> </dl>

</dd> <dt>

**User**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del usuario al que se emitió la licencia.

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

[**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

