---
title: Win32_TSLicenseReportPerDeviceEntry clase
description: Proporciona detalles sobre el error Servicios de Escritorio remoto licencia de acceso de cliente por dispositivo (RDS \ 160; Cal por dispositivo).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry clase Servicios de Escritorio remoto
- Win32_TSLicenseReportPerDeviceEntry clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbcdad271a346820b318c94bed7ce6b9b9527d3fdd7df9cc3f1dc9d9a97aae3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008425"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a>Clase \_ TSLicenseReportPerDeviceEntry de Win32

Proporciona detalles sobre el error Servicios de Escritorio remoto licencia de acceso de cliente por dispositivo (CAL de RDS por dispositivo).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSLicenseReportPerDeviceEntry de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseReportPerDeviceEntry de Win32** tiene estas propiedades.

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

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DATETIME**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha de expiración de la licencia.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión de Servicios de Escritorio remoto para la que se emitió la CAL de RDS por usuario. Este será uno de los siguientes valores.

<dt>

"Windows Server 2012"
</dt> <dd>

Con esta licencia solo se admiten los servidores Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.

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

**sHardwareId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador de hardware del equipo.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo para el que se intentó emitir la licencia.

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

[**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

