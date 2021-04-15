---
title: Método GenerateReport de la clase Win32_TSLicenseReport (GPMgmt. h)
description: GenerateReport ya no está disponible para su uso a partir de Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Método GenerateReport Servicios de Escritorio remoto
- Método GenerateReport Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método GenerateReport
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
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422480"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>Método GenerateReport de la \_ clase TSLicenseReport de Win32

\[**GenerateReport** ya no está disponible para su uso a partir de Windows Server 2012. En su lugar, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]

No se admite este método.

**Windows server 2008 R2 y Windows server 2008:** Genera un informe de uso de licencias por usuario actual en el servidor de licencias de Escritorio remoto.

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

*ScopeType* \[ de\]
</dt> <dd>

Ámbito del informe de uso de licencias. Puede tener los valores siguientes.

<dt>

1
</dt> <dd>

El informe se generará para todo el dominio.

</dd> <dt>

2
</dt> <dd>

El informe se generará para la unidad organizativa (OU) que se especifica en el parámetro *ScopeValue* .

</dd> <dt>

3
</dt> <dd>

El informe se generará para todos los dominios de confianza.

</dd> </dl> </dd> <dt>

*ScopeValue* \[ de\]
</dt> <dd>

Si el parámetro *ScopeType* es 2, *ScopeType* especifica la unidad organizativa para la que se generará el informe. Debe especificar *ScopeValue* con el formato **ou =**_OUName1_*_, ou =_*_OUName2_*_.._*..

</dd> <dt>

*Nombre de archivo* \[ enuncia\]
</dt> <dd>

Nombre de archivo del informe generado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **WBEM \_ E \_ no \_ compatible**.

**Windows server 2008 R2 y Windows server 2008:** Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Se trata de un método estático.

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                         |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| Encabezado<br/>                   | <dl> <dt>GPMgmt. h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

