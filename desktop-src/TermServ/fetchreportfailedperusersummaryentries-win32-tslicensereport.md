---
title: Método FetchReportFailedPerUserSummaryEntries de la Win32_TSLicenseReport clase
description: Recupera información de resumen de las licencias de acceso de cliente Servicios de Escritorio remoto por usuario con errores (RDS \ 160; CAL por usuario) del informe.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Método FetchReportFailedPerUserSummaryEntries Servicios de Escritorio remoto
- Método FetchReportFailedPerUserSummaryEntries Servicios de Escritorio remoto , Win32_TSLicenseReport clase
- Win32_TSLicenseReport clase Servicios de Escritorio remoto , método FetchReportFailedPerUserSummaryEntries
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
ms.openlocfilehash: cc42cb36ad0d203389dd115eb6bf02b1135982f1c490a0f669e19d2f64e937ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737555"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportFailedPerUserSummaryEntries de la clase \_ TSLicenseReport de Win32

Recupera información de resumen de las licencias de acceso de cliente Servicios de Escritorio remoto por usuario (CAL por usuario de RDS) del informe.

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

*StartIndex* \[ En\]
</dt> <dd>

Índice de la primera entrada de informe que se va a recuperar. La primera entrada de informe tiene un índice de cero.

</dd> <dt>

*Recuento* \[ in, out\]
</dt> <dd>

Número de entradas de informe que se recuperarán del objeto de informe. Un valor de cero indica que se van a recuperar todas las entradas del informe a partir de *StartIndex.* En la devolución, contiene el número de entradas de la *matriz ReportFailedPerUserSummaryEntries.*

</dd> <dt>

*ReportFailedPerUserSummaryEntries* \[ out\]
</dt> <dd>

Matriz de [**clases \_ TSLicenseReportFailedPerUserSummaryEntry de Win32**](win32-tslicensereportfailedperusersummaryentry.md) que representan las entradas de licencia recuperadas. El *parámetro Count* contiene el número de elementos de esta matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

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

[**TSLicenseReport de Win32 \_**](win32-tslicensereport.md)
</dt> </dl>

 

 





