---
title: Método IsLogEventEnabled de la Win32_TSGatewayServerSettings clase
description: Indica si el tipo de registro de eventos especificado está habilitado.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Método IsLogEventEnabled Servicios de Escritorio remoto
- Método IsLogEventEnabled Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , método IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243531"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Método IsLogEventEnabled de la clase \_ TSGatewayServerSettings de Win32

Indica si el tipo de registro de eventos especificado está habilitado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EventName* \[ En\]
</dt> <dd>

Nombre del tipo de registro de eventos. Este valor se debe recuperar mediante el [**método GetLogEventName.**](getlogeventname-win32-tsgatewayserversettings.md)

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

*Habilitado* \[ out\]
</dt> <dd>

Indica si el tipo de registro de eventos especificado está habilitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

