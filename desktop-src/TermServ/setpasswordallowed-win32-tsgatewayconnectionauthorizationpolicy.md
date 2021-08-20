---
title: Método SetPasswordAllowed de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Establece la propiedad PasswordAllowed, que habilita o deshabilita la compatibilidad con el uso de una contraseña para conectarse al servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 2d2dfc45-ac2c-41dc-b2c1-4c8eab42c442
ms.tgt_platform: multiple
keywords:
- Método SetPasswordAllowed Servicios de Escritorio remoto
- Método SetPasswordAllowed Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto método , SetPasswordAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetPasswordAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4139858d2f69f71433df7b984d62fe84054b17be5ac7161b166abcb604b3f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058523"
---
# <a name="setpasswordallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetPasswordAllowed de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Establece la **propiedad PasswordAllowed,** que habilita o deshabilita la compatibilidad con el uso de una contraseña para conectarse al servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPasswordAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Permitido* \[ En\]
</dt> <dd>

Nuevo **valor PasswordAllowed.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

