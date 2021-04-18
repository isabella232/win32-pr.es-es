---
title: Método DisableClipboard de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad ClipboardDisabled. Si la propiedad DeviceRedirectionType tiene un valor de \ 0034; 2 \ 0034;, la propiedad ClipboardDisabled controla la redirección del portapapeles para las sesiones que se establecen a través del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Método DisableClipboard Servicios de Escritorio remoto
- Método DisableClipboard Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método DisableClipboard
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685872"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método DisableClipboard de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32

Establece la propiedad **ClipboardDisabled** . Si la propiedad **DeviceRedirectionType** tiene un valor de "2", la propiedad **ClipboardDisabled** controla la redirección del portapapeles para las sesiones que se establecen a través del servidor de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Deshabilitado* \[ de\]
</dt> <dd>

Nuevo valor para la propiedad **ClipboardDisabled** .

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

 

