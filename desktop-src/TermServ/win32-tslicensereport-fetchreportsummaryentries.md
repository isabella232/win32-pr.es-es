---
title: Método FetchReportSummaryEntries de la clase Win32_TSLicenseReport
description: Recupera resúmenes de las licencias de acceso de cliente de Servicios de Escritorio remoto por usuario (RDS \ 160; Cal por usuario) del informe.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Método FetchReportSummaryEntries Servicios de Escritorio remoto
- Método FetchReportSummaryEntries Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método FetchReportSummaryEntries
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
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149958"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a>Método FetchReportSummaryEntries de la \_ clase TSLicenseReport de Win32

Recupera resúmenes de Servicios de Escritorio remoto licencias de acceso de cliente por usuario (cal por usuario de RDS) del informe.

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

*StartIndex* \[ de\]
</dt> <dd>

Índice de la primera entrada del informe que se va a recibir. La primera entrada del informe tiene un índice de cero.

</dd> <dt>

*Recuento* \[ in, out\]
</dt> <dd>

Número de entradas de informe que se van a recuperar del objeto de informe. Un valor de cero indica que se recuperarán todas las entradas del informe que comienzan en *StartIndex* . En la devolución, contiene el número de entradas de la matriz *ReportSummaryEntries* .

</dd> <dt>

*ReportSummaryEntries* \[ enuncia\]
</dt> <dd>

Devuelve una matriz de [**clases \_ TSLicenseReportSummaryEntry de Win32**](win32-tslicensereportsummaryentry.md) .

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

[**Win32 \_ TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

