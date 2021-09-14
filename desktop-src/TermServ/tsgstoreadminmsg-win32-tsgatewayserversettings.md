---
title: Método TSGStoreAdminMsg de la Win32_TSGatewayServerSettings clase
description: Actualiza el mensaje administrativo para el servidor de puerta de enlace.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- Método TSGStoreAdminMsg Servicios de Escritorio remoto
- Método TSGStoreAdminMsg Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto método , TSGStoreAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170605"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a>Método TSGStoreAdminMsg de la clase \_ TSGatewayServerSettings de Win32

Actualiza el mensaje administrativo para el servidor de puerta de enlace.

## <a name="syntax"></a>Sintaxis


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TSGAdmMsg* \[ En\]
</dt> <dd>

Tipo: **cadena**

Texto del mensaje administrativo.

</dd> <dt>

*MsgStartTime* \[ En\]
</dt> <dd>

Tipo: **cadena**

Hora de inicio del mensaje administrativo.

</dd> <dt>

*MsgEndTime* \[ En\]
</dt> <dd>

Tipo: **cadena**

Hora de finalización del mensaje administrativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayServerSettings de Win32 \_**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

