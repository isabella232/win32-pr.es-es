---
title: Método GenerateReport de la Win32_TSLicenseReport (Gpmgmt.h)
description: GenerateReport ya no está disponible para su uso a Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Método GenerateReport Servicios de Escritorio remoto
- Método GenerateReport Servicios de Escritorio remoto , Win32_TSLicenseReport clase
- Win32_TSLicenseReport clase Servicios de Escritorio remoto método , GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a619da8130187a4ab5d39de390315dd99b3ee7a171005a4cf66e7bb5677ae87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130784"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>Método GenerateReport de la clase \_ TSLicenseReport de Win32

\[**GenerateReport** ya no está disponible para su uso a Windows Server 2012. En su lugar, [**use GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]

No se admite este método.

**Windows Server 2008 R2 y Windows Server 2008:** Genera un informe de uso de licencias por usuario actual en Escritorio remoto servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ScopeType* \[ En\]
</dt> <dd>

Ámbito del informe de uso de licencias. Puede tener los siguientes valores.

<dt>

1
</dt> <dd>

El informe se generará para todo el dominio.

</dd> <dt>

2
</dt> <dd>

El informe se generará para la unidad organizativa (OU) especificada en el *parámetro ScopeValue.*

</dd> <dt>

3
</dt> <dd>

El informe se generará para todos los dominios de confianza.

</dd> </dl> </dd> <dt>

*ScopeValue* \[ En\]
</dt> <dd>

Si el *parámetro ScopeType* es 2, *ScopeType* especifica la unidad organizativa para la que se generará el informe. Debe especificar *ScopeValue con* el formato **OU=**_OUName1_*_, OU=_*_OUName2_*_..._*.

</dd> <dt>

*FileName* \[ out\]
</dt> <dd>

Nombre de archivo del informe generado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **WBEM \_ E NOT \_ \_ SUPPORTED**.

**Windows Server 2008 R2 y Windows Server 2008:** Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Se trata de un método estático.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                         |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Gpmgmt.h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSLicenseReport de Win32 \_**](win32-tslicensereport.md)
</dt> </dl>

 

