---
title: Método GenerateReportEx de la Win32_TSLicenseReport clase
description: Genera un informe de uso de licencias actual para las licencias por usuario y por dispositivo.
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- Método GenerateReportEx Servicios de Escritorio remoto
- Método GenerateReportEx Servicios de Escritorio remoto , Win32_TSLicenseReport clase
- Win32_TSLicenseReport clase Servicios de Escritorio remoto método , GenerateReportEx
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bfe9bc9a8ed31c2f272f3ae081556f47d21f360d719abe1363a04c170afe5b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353832"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a>Método GenerateReportEx de la clase \_ TSLicenseReport de Win32

Genera un informe de uso de licencias actual para las licencias por usuario y por dispositivo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* \[ out\]
</dt> <dd>

Nombre de archivo del informe generado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Se trata de un método estático.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

