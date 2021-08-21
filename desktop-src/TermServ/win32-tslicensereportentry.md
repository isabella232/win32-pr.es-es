---
title: Win32_TSLicenseReportEntry clase
description: Proporciona detalles de la licencia de acceso de cliente Servicios de Escritorio remoto por usuario (RDS \ 160; Cal por usuario).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry clase Servicios de Escritorio remoto
- Win32_TSLicenseReportEntry clase Servicios de Escritorio remoto , descrita
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
ms.openlocfilehash: e08041ac0878f3466712001a0a5e2cc90eb74ea1e360da9785b5d84805574389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126525"
---
# <a name="win32_tslicensereportentry-class"></a>Clase \_ TSLicenseReportEntry de Win32

Proporciona detalles de la licencia de acceso de cliente Servicios de Escritorio remoto por usuario (CAL por usuario de RDS).

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

Especifica el tipo de CAL emitido. Este será uno de los siguientes valores.

**Windows Server 2008 R2 y Windows Server 2008:** Esta propiedad no se admite.

"CAL de TS por dispositivo integrada"

"TS per Device CAL"

"TS Internet Connector CAL"

"TS per User CAL"

"CAL de TS o RDS por dispositivo"

"CAL de TS o RDS por usuario"

"Licencia de suscripción de VDI Standard Suite per Device"

"Licencia de suscripción de VDI Premium Suite por dispositivo"

"CAL de RDS por dispositivo"

"CAL de RDS por usuario"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DATETIME**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha de expiración de la licencia que se emitió al usuario.

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

Solo los servidores que Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 son compatibles con esta licencia.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Solo los servidores que Windows Server 2008 R2 o Windows Server 2008 son compatibles con esta licencia.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Solo los servidores que Windows Server 2008 son compatibles con esta licencia.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de versión del producto para el Servicios de Escritorio remoto de claves de licencia.

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

No compatible.

</dd> <dt>

0
</dt> <dd>

No compatible.

</dd> </dl>

</dd> <dt>

**User**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del usuario al que se emitió la licencia.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para usar esta clase.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
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

 

