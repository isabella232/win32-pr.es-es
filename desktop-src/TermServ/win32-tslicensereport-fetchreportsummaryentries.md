---
title: Método FetchReportSummaryEntries de la Win32_TSLicenseReport clase
description: Recupera resúmenes de Servicios de Escritorio remoto licencias de acceso de cliente por usuario (RDS \ 160; CAL por usuario) del informe.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Método FetchReportSummaryEntries Servicios de Escritorio remoto
- Método FetchReportSummaryEntries Servicios de Escritorio remoto , Win32_TSLicenseReport clase
- Win32_TSLicenseReport clase Servicios de Escritorio remoto , método FetchReportSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094d7fe1f7aa3d5acabce7d7d248c16601b5005d09f2583cc23c7390c3642361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348580"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportSummaryEntries de la clase \_ TSLicenseReport de Win32

Recupera resúmenes de Servicios de Escritorio remoto licencias de acceso de cliente por usuario (CAL de RDS por usuario) del informe.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartIndex* \[ En\]
</dt> <dd>

Índice de la primera entrada de informe que se va a recibir. La primera entrada de informe tiene un índice de cero.

</dd> <dt>

*Recuento* \[ in, out\]
</dt> <dd>

Número de entradas de informe que se recuperarán del objeto de informe. Un valor de cero indica que se van a recuperar todas las entradas del informe a partir de *StartIndex.* En la devolución, contiene el número de entradas de la *matriz ReportSummaryEntries.*

</dd> <dt>

*ReportSummaryEntries* \[ out\]
</dt> <dd>

Devuelve una matriz de [**clases \_ TSLicenseReportSummaryEntry de Win32.**](win32-tslicensereportsummaryentry.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Un valor **de LSERVER \_ I NO \_ MORE \_ \_ DATA** (0x4001) indica que no hay más entradas de informe.

## <a name="remarks"></a>Comentarios

No se trata de un método estático. Se debe llamar a este método desde un objeto de informe de uso de licencias por usuario.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TSLicenseReport de Win32 \_**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

