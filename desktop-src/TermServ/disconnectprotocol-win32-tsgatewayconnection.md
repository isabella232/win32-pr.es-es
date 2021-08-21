---
title: Método DisconnectProtocol de la Win32_TSGatewayConnection clase
description: Desconecta todas las conexiones del protocolo especificado del servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Método DisconnectProtocol Servicios de Escritorio remoto
- Método DisconnectProtocol Servicios de Escritorio remoto , Win32_TSGatewayConnection clase
- Win32_TSGatewayConnection clase Servicios de Escritorio remoto , método DisconnectProtocol
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c3c987a07dddfee5814cc32fbab8e77e2b7af5d6e55768965294cfeadaf5fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856251"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a>Método DisconnectProtocol de la clase \_ TSGatewayConnection de Win32

Desconecta todas las conexiones del protocolo especificado del servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtocolName* \[ En\]
</dt> <dd>

Nombre del protocolo para una conexión específica. Esto se puede recuperar de la **propiedad ProtocolName** de la **clase \_ TSGatewayConnection de Win32.**

<dt>

"TS"
</dt> <dd>

Protocolo para el servidor de puerta de enlace de Escritorio remoto.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> </dl>

 

