---
title: Win32_TSLicenseReport (clase)
description: Proporciona instancias de Servicios de Escritorio remoto licencia de acceso de cliente por usuario (RDS \ 160; Los informes de uso de CAL por usuario) que se generan en el servidor de licencias de Escritorio remoto, y métodos para las operaciones de generación, recuperación y eliminación de informes de licencias.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReport de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905046"
---
# <a name="win32_tslicensereport-class"></a>\_Clase Win32 TSLicenseReport

Proporciona instancias de Servicios de Escritorio remoto informes de uso de licencias de acceso de cliente por usuario (CAL por usuario de RDS) que se generan en el servidor de licencias de Escritorio remoto y métodos para la generación de informes de licencias, la recuperación y las operaciones de eliminación.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSLicenseReport de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TSLicenseReport** tiene estos métodos.



| Método                                                                                                         | Descripción                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Elimina un objeto de informe en el servidor de licencias de Escritorio remoto. No es un método estático.<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | Recupera entradas en el objeto de informe.<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Recupera los detalles de las licencias de acceso de cliente por usuario (cal por usuario de RDS) con Servicios de Escritorio remoto error en el informe.<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Recupera información de Resumen de las licencias de acceso de cliente por usuario de Servicios de Escritorio remoto con errores (cal por usuario de RDS) del informe.<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Recupera la información de las licencias de acceso de cliente por dispositivo de Servicios de Escritorio remoto emitidas (cal por dispositivo de RDS) del informe.<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Recupera los resúmenes de licencia del objeto de informe.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | No se admite este método.<br/> **Windows server 2008 R2 y Windows server 2008:** Genera un informe de uso de licencias por usuario actual en el servidor de licencias de Escritorio remoto.<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | Genera un informe de uso de licencias por usuario actual en el servidor de licencias de Escritorio remoto.<br/>                                                                                              |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseReport de Win32** tiene estas propiedades.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del informe.

</dd> <dt>

**GenerationDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora de generación de informes de licencias de escritorio remoto.

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no es compatible.

**Windows server 2008 R2 y Windows server 2008:** Número de cal por usuario de RDS instaladas.

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no es compatible.

**Windows server 2008 R2 y Windows server 2008:** Número de cal por usuario de RDS que están actualmente en uso.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no es compatible.

**Windows server 2008 R2 y Windows server 2008:** Tipo de ámbito de informe de licencias de escritorio remoto.

</dd> <dt>

**ScopeValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no es compatible.

**Windows server 2008 R2 y Windows server 2008:** Valor de ámbito del informe de licencias de escritorio remoto.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión del informe de licencias de escritorio remoto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los informes que se generan mediante WMI se muestran en el administrador de licencias de escritorio remoto. Los informes que se eliminan mediante WMI también se eliminan del administrador de licencias de escritorio remoto.

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

