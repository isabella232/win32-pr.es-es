---
title: Método DisableClipboard de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Establece la propiedad ClipboardDisabled. Si la propiedad DeviceRedirectionType tiene un valor de \ 0034;2 \ 0034;, la propiedad ClipboardDisabled controla el redireccionamiento del Portapapeles para las sesiones que se establecen a través del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de Escritorio remoto).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Método DisableClipboard Servicios de Escritorio remoto
- Método DisableClipboard Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto método , DisableClipboard
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
ms.openlocfilehash: 01b5e8d2449bae2ee7f344c78b54850eb9ae300f4233c36b6eb2d84ad0b6132f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609620"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método DisableClipboard de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Establece la **propiedad ClipboardDisabled.** Si la propiedad **DeviceRedirectionType** tiene el valor "2", la propiedad **ClipboardDisabled** controla el redireccionamiento del Portapapeles para las sesiones que se establecen a través del servidor de Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Deshabilitado* \[ En\]
</dt> <dd>

Nuevo valor para la **propiedad ClipboardDisabled.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

