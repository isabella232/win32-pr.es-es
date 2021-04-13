---
title: Método FetchReportFailedPerUserEntries de la clase Win32_TSLicenseReport
description: Recupera los detalles de las licencias de acceso de cliente de Servicios de Escritorio remoto de error por usuario (RDS \ 160; Cal por usuario) del informe.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- Método FetchReportFailedPerUserEntries Servicios de Escritorio remoto
- Método FetchReportFailedPerUserEntries Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método FetchReportFailedPerUserEntries
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
ms.openlocfilehash: 159f980944c70dbad4c6948a614d0c9964a5f0cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535230"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportFailedPerUserEntries de la \_ clase TSLicenseReport de Win32

Recupera los detalles de las licencias de acceso de cliente por usuario (cal por usuario de RDS) con Servicios de Escritorio remoto error en el informe.

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

*StartIndex* \[ de\]
</dt> <dd>

Índice de la primera entrada del informe que se va a recuperar. La primera entrada del informe tiene un índice de cero.

</dd> <dt>

*Recuento* \[ in, out\]
</dt> <dd>

Número de entradas de informe que se van a recuperar del objeto de informe. Un valor de cero indica que se recuperarán todas las entradas del informe que comienzan en *StartIndex* . En la devolución, contiene el número de entradas de la matriz *ReportFailedPerUserEntries* .

</dd> <dt>

*ReportFailedPerUserEntries* \[ enuncia\]
</dt> <dd>

Matriz de clases [**\_ TSLicenseReportFailedPerUserEntry de Win32**](win32-tslicensereportfailedperuserentry.md) que representan las entradas de licencia recuperadas. El parámetro *Count* contiene el número de elementos de esta matriz.

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

 

 





