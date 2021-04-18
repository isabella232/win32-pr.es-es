---
title: Win32_TSLicenseReportSummaryEntry (clase)
description: Proporciona un resumen de las licencias de acceso de cliente de los Servicios de Escritorio remoto instalados y emitidos por usuario (RDS \ 160; Cal por usuario).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReportSummaryEntry de clase, se describe
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
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676579"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>\_Clase Win32 TSLicenseReportSummaryEntry

Proporciona un resumen de las licencias de acceso de cliente de los Servicios de Escritorio remoto instalados y emitidos por usuario (cal por usuario de RDS).

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

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de cal por usuario de RDS instaladas.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de cal por usuario de RDS que se emiten.

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

**TSCALAvailability**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La disponibilidad de las cal por usuario de RDS. Será uno de los valores siguientes.

<dt>

Disponible
</dt> <dd>

Las cal por usuario de RDS están disponibles.

</dd> <dt>

Separados
</dt> <dd>

La disponibilidad de las cal por usuario de RDS es limitada.

</dd> <dt>

"None"
</dt> <dd>

Las cal por usuario de RDS no están disponibles.

</dd> <dt>

"No tracking"
</dt> <dd>

No se está realizando el seguimiento de la disponibilidad de las cal por usuario de RDS.

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de cal por usuario de RDS. Será uno de los valores siguientes.

<dt>

"Por dispositivo"
</dt> <dd>

Las cal por usuario de RDS se emiten por dispositivo.

</dd> <dt>

"Por usuario"
</dt> <dd>

Las cal por usuario de RDS se emiten por usuario.

</dd> <dt>

Unknown
</dt> <dd>

Se desconoce el tipo de cal por usuario de RDS.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





