---
title: Win32_TSLicenseReportFailedPerUserEntry clase
description: Proporciona detalles sobre el error Servicios de Escritorio remoto licencia de acceso de cliente por usuario (RDS \ 160; Cal por usuario).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry clase Servicios de Escritorio remoto
- Win32_TSLicenseReportFailedPerUserEntry clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02d56c1a7e2c715f068d808d45ac6ae3295b16bb7382179ec0e32c93beee096
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420845"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a>Clase \_ TSLicenseReportFailedPerUserEntry de Win32

Proporciona detalles sobre el error Servicios de Escritorio remoto licencia de acceso de cliente por usuario (CAL de RDS por usuario).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSLicenseReportFailedPerUserEntry de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseReportFailedPerUserEntry de Win32** tiene estas propiedades.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de CAL emitido. Este será uno de los siguientes valores.

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

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión de Servicios de Escritorio remoto para la que se emitió la CAL por usuario de RDS. Este será uno de los siguientes valores.

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

Solo los servidores que Windows Server 2008 se admiten con esta licencia.

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

**TriedIssuanceOn**
</dt> <dd> <dl> <dt>

Tipo de datos: **DATETIME**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha en la que se intentó emitir la licencia.

</dd> <dt>

**User**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del usuario al que se intentó emitir la licencia.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

