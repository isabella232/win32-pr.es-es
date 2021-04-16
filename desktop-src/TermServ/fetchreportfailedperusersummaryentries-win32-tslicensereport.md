---
title: Método FetchReportFailedPerUserSummaryEntries de la clase Win32_TSLicenseReport
description: Recupera información de Resumen de las licencias de acceso de cliente de Servicios de Escritorio remoto de error por usuario (RDS \ 160; Cal por usuario) del informe.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Método FetchReportFailedPerUserSummaryEntries Servicios de Escritorio remoto
- Método FetchReportFailedPerUserSummaryEntries Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método FetchReportFailedPerUserSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686183"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportFailedPerUserSummaryEntries de la \_ clase TSLicenseReport de Win32

Recupera información de Resumen de las licencias de acceso de cliente por usuario de Servicios de Escritorio remoto con errores (cal por usuario de RDS) del informe.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartIndex* \[ de\]
</dt> <dd>

Índice de la primera entrada del informe que se va a recuperar. La primera entrada del informe tiene un índice de cero.

</dd> <dt>

*Recuento* \[ in, out\]
</dt> <dd>

Número de entradas de informe que se van a recuperar del objeto de informe. Un valor de cero indica que se recuperarán todas las entradas del informe que comienzan en *StartIndex* . En la devolución, contiene el número de entradas de la matriz *ReportFailedPerUserSummaryEntries* .

</dd> <dt>

*ReportFailedPerUserSummaryEntries* \[ enuncia\]
</dt> <dd>

Matriz de clases [**\_ TSLicenseReportFailedPerUserSummaryEntry de Win32**](win32-tslicensereportfailedperusersummaryentry.md) que representan las entradas de licencia recuperadas. El parámetro *Count* contiene el número de elementos de esta matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

 





