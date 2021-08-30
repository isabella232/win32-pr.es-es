---
title: Método EnumAuthenticationPlugins de la Win32_TSGatewayServerSettings clase
description: Enumera todos los complementos de autenticación registrados.
ms.assetid: a5c1859d-e20c-4c72-aef5-ef9941edf73e
ms.tgt_platform: multiple
keywords:
- Método EnumAuthenticationPlugins Servicios de Escritorio remoto
- Método EnumAuthenticationPlugins Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , Método EnumAuthenticationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthenticationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff57d92b2e1b71abd2ed9ec459ff3a0cff3e3894c0d2728af057dee8cbdf570c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080175"
---
# <a name="enumauthenticationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnumAuthenticationPlugins de la clase \_ TSGatewayServerSettings de Win32

Enumera todos los complementos de autenticación registrados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnumAuthenticationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PluginNames* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz **de** cadenas que recibe los nombres de los complementos de autenticación registrados.

</dd> <dt>

*CLSID* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz **de** cadenas que recibe los CLID de los complementos de autenticación registrados.

</dd> <dt>

*Descripciones* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz **de** cadenas que recibe las descripciones de los complementos de autenticación registrados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

