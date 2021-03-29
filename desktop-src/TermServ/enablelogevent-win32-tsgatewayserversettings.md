---
title: Método EnableLogEvent de la clase Win32_TSGatewayServerSettings
description: Habilita o deshabilita el registro del tipo de evento especificado.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Método EnableLogEvent Servicios de Escritorio remoto
- Método EnableLogEvent Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método EnableLogEvent
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
ms.openlocfilehash: e72f7cb8567c7f2d5c3ca79d241013e2bd64a5e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493210"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableLogEvent de la \_ clase TSGatewayServerSettings de Win32

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

*EventName* \[ de\]
</dt> <dd>

Nombre del evento. Este valor se debe recuperar mediante el método [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .

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

Error de autorización de conexión de usuario.

</dd> <dt>

LogFailureResourceAccessCheck
</dt> <dd>

Error de autorización de recursos del usuario.

</dd> <dt>

LogSuccessChannelConnect
</dt> <dd>

El usuario se conectó correctamente al recurso.

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

El usuario pasó correctamente la autorización de conexión.

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

El usuario ha pasado correctamente la autorización de recursos.

</dd> </dl> </dd> <dt>

*Habilitado* \[ de\]
</dt> <dd>

Especifica si el evento debe estar habilitado o deshabilitado.

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

