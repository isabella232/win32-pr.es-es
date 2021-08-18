---
title: Método FetchReportFailedPerUserEntries de la Win32_TSLicenseReport clase
description: Recupera los detalles de las licencias de acceso de cliente Servicios de Escritorio remoto por usuario (RDS \ 160; Por CAL de usuario) del informe.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- Método FetchReportFailedPerUserEntries Servicios de Escritorio remoto
- Método FetchReportFailedPerUserEntries Servicios de Escritorio remoto , Win32_TSLicenseReport clase
- Win32_TSLicenseReport clase Servicios de Escritorio remoto , método FetchReportFailedPerUserEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4d78ff13ff58f7e80c1f177728ded24dc98588b0a0fb25c3976e9dcc19fdc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737635"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportFailedPerUserEntries de la clase TSLicenseReport de Win32 \_

Recupera los detalles de los Servicios de Escritorio remoto licencias de acceso de cliente por usuario (CAL de RDS por usuario) del informe.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
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

Número de entradas de informe que se recuperarán del objeto de informe. Un valor de cero indica que se van a recuperar todas las entradas de informe que comienzan *en StartIndex.* En la devolución, contiene el número de entradas de la *matriz ReportFailedPerUserEntries.*

</dd> <dt>

*ReportFailedPerUserEntries* \[ out\]
</dt> <dd>

Matriz de [**clases \_ TSLicenseReportFailedPerUserEntry de Win32**](win32-tslicensereportfailedperuserentry.md) que representan las entradas de licencia recuperadas. El *parámetro Count* contiene el número de elementos de esta matriz.

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

 

 





