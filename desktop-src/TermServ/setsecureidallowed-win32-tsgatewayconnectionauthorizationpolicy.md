---
title: Método SetSecureIdAllowed de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Este método está reservado para un uso futuro.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- Método SetSecureIdAllowed Servicios de Escritorio remoto
- Método SetSecureIdAllowed Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto , método SetSecureIdAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99039cd541ad8ab1746ace55de13f35722ea1ba7ccf52fd1a3de93e39e56798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865115"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetSecureIdAllowed de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Este método está reservado para un uso futuro.

Establece la **propiedad SecureIdAllowed,** que está reservada para su uso futuro.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Permitido* \[ En\]
</dt> <dd>

Nuevo **valor SecureIdAllowed.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

