---
title: Método SetPasswordAllowed de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad PasswordAllowed, que habilita o deshabilita la compatibilidad con el uso de una contraseña para conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 2d2dfc45-ac2c-41dc-b2c1-4c8eab42c442
ms.tgt_platform: multiple
keywords:
- Método SetPasswordAllowed Servicios de Escritorio remoto
- Método SetPasswordAllowed Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetPasswordAllowed
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
ms.openlocfilehash: 5c8bda5fde2fd79cc02697fd270fc307ef5f410f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422567"
---
# <a name="setpasswordallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetPasswordAllowed de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32

Establece la propiedad **PasswordAllowed** , que habilita o deshabilita la compatibilidad con el uso de una contraseña para conectarse al servidor de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPasswordAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Permitido* \[ de\]
</dt> <dd>

Nuevo valor de **PasswordAllowed** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

