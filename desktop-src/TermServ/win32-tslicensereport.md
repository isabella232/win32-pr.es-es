---
title: Win32_TSLicenseReport clase
description: Proporciona instancias de Servicios de Escritorio remoto licencia de acceso de cliente por usuario (RDS \ 160; Por cal de usuario) informes de uso que se generan en el servidor de licencias de Escritorio remoto y métodos para las operaciones de generación, captura y eliminación de informes de licencias.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport clase Servicios de Escritorio remoto
- Win32_TSLicenseReport clase Servicios de Escritorio remoto , descrita
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
ms.openlocfilehash: 93280c00cbd20993907901e1f9b8c16330863a47bddd4e08bc86d51b4b837233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137838"
---
# <a name="win32_tslicensereport-class"></a>Clase \_ TSLicenseReport de Win32

Proporciona instancias de Servicios de Escritorio remoto informes de uso de la licencia de acceso de cliente por usuario (CAL de RDS por usuario) que se generan en el servidor de licencias de Escritorio remoto y métodos para las operaciones de generación, captura y eliminación de informes de licencias.

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

La **clase \_ TSLicenseReport de Win32** tiene estos métodos.



| Método                                                                                                         | Descripción                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Elimina un objeto de informe en el Escritorio remoto de licencias. No se trata de un método estático.<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | Recupera las entradas del objeto de informe.<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Recupera los detalles de los Servicios de Escritorio remoto licencias de acceso de cliente por usuario (CAL de RDS por usuario) del informe.<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Recupera la información de resumen de los Servicios de Escritorio remoto licencias de acceso de cliente por usuario (CAL de RDS por usuario) del informe.<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Recupera la información de las licencias Servicios de Escritorio remoto acceso de cliente por dispositivo (CAL de RDS por dispositivo) del informe.<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Recupera resúmenes de licencia del objeto de informe.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | No se admite este método.<br/> **Windows Server 2008 R2 y Windows Server 2008:** Genera un informe de uso de licencias por usuario actual en Escritorio remoto servidor de licencias.<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | Genera un informe de uso de licencias por usuario actual en Escritorio remoto servidor de licencias.<br/>                                                                                              |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSLicenseReport de Win32** tiene estas propiedades.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del informe.

</dd> <dt>

**GenerationDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora de generación de informes de licencias de Escritorio remoto.

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **EN DESUSO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no es compatible.

**Windows Server 2008 R2 y Windows Server 2008:** Número de CAL de RDS por usuario que están instaladas.

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **EN DESUSO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no es compatible.

**Windows Server 2008 R2 y Windows Server 2008:** Número de CAL de RDS por usuario que están actualmente en uso.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **EN DESUSO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no es compatible.

**Windows Server 2008 R2 y Windows Server 2008:** Tipo de ámbito de informe de licencias de Escritorio remoto.

</dd> <dt>

**ScopeValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **EN DESUSO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propiedad no es compatible.

**Windows Server 2008 R2 y Windows Server 2008:** Valor del ámbito del informe de licencias de Escritorio remoto.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión del informe de licencias de Escritorio remoto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los informes generados mediante WMI se muestran en el Administrador de licencias de Escritorio remoto. Los informes que se eliminan mediante WMI también se eliminan del Administrador de licencias de Escritorio remoto.

Debe ser miembro del grupo Administradores para usar esta clase.

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

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

