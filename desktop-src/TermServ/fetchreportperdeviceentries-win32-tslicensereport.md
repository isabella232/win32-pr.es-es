---
title: Método FetchReportPerDeviceEntries de la Win32_TSLicenseReport clase
description: Recupera información de licencias de acceso de cliente Servicios de Escritorio remoto por dispositivo (RDS \ 160; Por CAL de dispositivo) del informe.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Método FetchReportPerDeviceEntries Servicios de Escritorio remoto
- Método FetchReportPerDeviceEntries Servicios de Escritorio remoto , Win32_TSLicenseReport clase
- Win32_TSLicenseReport clase Servicios de Escritorio remoto , método FetchReportPerDeviceEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3a5ef050002da069f7eda56352f204797cac521885248bc7e63dfd77f840f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737565"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportPerDeviceEntries de la clase \_ TSLicenseReport de Win32

Recupera la información de las licencias Servicios de Escritorio remoto acceso de cliente por dispositivo (CAL de RDS por dispositivo) del informe.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
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

Número de entradas de informe que se recuperarán del objeto de informe. Un valor de cero indica que se van a recuperar todas las entradas de informe que comienzan *en StartIndex.* En la devolución, contiene el número de entradas de la *matriz ReportPerDeviceEntries.*

</dd> <dt>

*ReportPerDeviceEntries* \[ out\]
</dt> <dd>

Una matriz [**de clases \_ TSLicenseReportPerDeviceEntry de Win32**](win32-tslicensereportperdeviceentry.md) representa las entradas de licencia recuperadas. El *parámetro Count* contiene el número de elementos de esta matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

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

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

 





