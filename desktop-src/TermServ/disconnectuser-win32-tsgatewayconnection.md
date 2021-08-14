---
title: Método DisconnectUser de la Win32_TSGatewayConnection (Tsgauthenticationengine.h)
description: Desconecta todas las conexiones del usuario especificado del servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Método DisconnectUser Servicios de Escritorio remoto
- Método DisconnectUser Servicios de Escritorio remoto , Win32_TSGatewayConnection clase
- Win32_TSGatewayConnection clase Servicios de Escritorio remoto método , DisconnectUser
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d31c7c89d285aed576024c551b07766a7387938762d60c252dec43e491037e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131000"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>Método DisconnectUser de la clase \_ TSGatewayConnection de Win32

Desconecta todas las conexiones del usuario especificado del servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserName* \[ En\]
</dt> <dd>

Nombre de usuario, en formato *Domain* **\\** _UserName,_ cuyas conexiones se van a desconectar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                       |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                             |
| Header<br/>                   | <dl> <dt>Tsgauthenticationengine.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl>             |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TSGatewayConnection de Win32 \_**](win32-tsgatewayconnection.md)
</dt> </dl>

 

