---
title: Win32_TSLicenseReportSummaryEntry clase
description: Proporciona un resumen de las licencias de acceso de cliente Servicios de Escritorio remoto por usuario (RDS \ 160; CAL por usuario).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry clase Servicios de Escritorio remoto
- Win32_TSLicenseReportSummaryEntry clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58efc2c70019037219d8eca986fa8afd81e4dc2d06cd638ee24fc59947e3bf3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137808"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>Clase \_ TSLicenseReportSummaryEntry de Win32

Proporciona un resumen de las licencias de acceso de cliente Servicios de Escritorio remoto por usuario (CAL de rds por usuario).

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSLicenseReportSummaryEntry de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseReportSummaryEntry de Win32** tiene estas propiedades.

<dl> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de CAL de RDS por usuario que están instaladas.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de CAL de RDS por usuario que se emiten.

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

**TSCALAvailability**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Disponibilidad de las CAL de RDS por usuario. Este será uno de los siguientes valores.

<dt>

"Disponible"
</dt> <dd>

Las CAL de RDS por usuario están disponibles.

</dd> <dt>

"Limitado"
</dt> <dd>

La disponibilidad de las CAL de RDS por usuario es limitada.

</dd> <dt>

"None"
</dt> <dd>

Las CAL de RDS por usuario no están disponibles.

</dd> <dt>

"Not Tracking"
</dt> <dd>

No se realiza el seguimiento de la disponibilidad de las CAL de RDS por usuario.

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de CAL de RDS por usuario. Este será uno de los siguientes valores.

<dt>

"Por dispositivo"
</dt> <dd>

Las CAL de RDS por usuario se emiten por dispositivo.

</dd> <dt>

"Por usuario"
</dt> <dd>

Las CAL de RDS por usuario se emiten por usuario.

</dd> <dt>

"Desconocido"
</dt> <dd>

Se desconoce el tipo de CAL de RDS por usuario.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





