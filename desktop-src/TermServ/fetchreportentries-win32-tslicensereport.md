---
title: Método FetchReportEntries de la clase Win32_TSLicenseReport
description: Recupera los detalles de las licencias de acceso de cliente de Servicios de Escritorio remoto por usuario (RDS \ 160; Cal por usuario) del informe. Cada entrada representa un RDS \ 160; CAL por usuario que está actualmente en uso.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Método FetchReportEntries Servicios de Escritorio remoto
- Método FetchReportEntries Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método FetchReportEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535235"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportEntries de la \_ clase TSLicenseReport de Win32

Recupera detalles de las licencias de acceso de cliente de Servicios de Escritorio remoto por usuario (cal por usuario de RDS) del informe. Cada entrada representa una CAL por usuario de RDS que está actualmente en uso.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartIndex* \[ de\]
</dt> <dd>

Índice de la primera entrada del informe que se va a recibir. La primera entrada del informe tiene un índice de cero.

</dd> <dt>

*Recuento* \[ in, out\]
</dt> <dd>

Número de entradas de informe que se van a recuperar del objeto de informe. Un valor de cero indica que se recuperarán todas las entradas del informe que comienzan en *StartIndex* . En la devolución, contiene el número de entradas de la matriz *ReportEntries* .

</dd> <dt>

*ReportEntries* \[ enuncia\]
</dt> <dd>

Devuelve una matriz de [**clases \_ TSLicenseReportEntry de Win32**](win32-tslicensereportentry.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Un valor de **LSERVER \_ I \_ no hay \_ más \_ datos** (0x4001) indica que no hay más entradas de informe.

## <a name="remarks"></a>Observaciones

No es un método estático. Se debe llamar a este método desde un objeto de informe de uso de licencias por usuario.

Para llamar a este método, debe ser miembro del grupo administradores.

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

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

