---
title: Método EnableLogEvent de la Win32_TSGatewayServerSettings clase
description: Habilita o deshabilita el registro del tipo de evento especificado.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Método EnableLogEvent Servicios de Escritorio remoto
- Método EnableLogEvent Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , método EnableLogEvent
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd70902649f6fadc66308ad35ce165a6d2fdb4654b73e056c3bc38f1850b3e07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871726"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableLogEvent de la clase \_ TSGatewayServerSettings de Win32

Habilita o deshabilita el registro del tipo de evento especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EventName* \[ En\]
</dt> <dd>

Nombre del evento. Este valor se debe recuperar mediante el [**método GetLogEventName.**](getlogeventname-win32-tsgatewayserversettings.md)

<dt>

LogChannelDisconnect
</dt> <dd>

El usuario se desconectó correctamente del recurso.

</dd> <dt>

LogFailedChannelConnect
</dt> <dd>

El usuario no pudo conectarse al recurso.

</dd> <dt>

LogFailureNetworkAccessCheck
</dt> <dd>

Error de autorización de conexión del usuario.

</dd> <dt>

LogFailureResourceAccessCheck
</dt> <dd>

Error de autorización de recursos del usuario.

</dd> <dt>

LogSuccessChannelConnect
</dt> <dd>

El usuario se ha conectado correctamente al recurso.

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

El usuario ha pasado correctamente la autorización de conexión.

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

El usuario ha pasado correctamente la autorización de recursos.

</dd> </dl> </dd> <dt>

*Habilitado* \[ En\]
</dt> <dd>

Especifica si el evento debe habilitarse o deshabilitarse.

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

