---
title: Constantes de Authentication-Level (Rpcdce. h)
description: Las constantes de nivel de autenticación representan los niveles de autenticación pasados a varias funciones en tiempo de ejecución.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535115"
---
# <a name="authentication-level-constants"></a>Constantes de nivel de autenticación

Las constantes de nivel de autenticación representan los niveles de autenticación pasados a varias funciones en tiempo de ejecución. Estos niveles se muestran en orden de autenticación incremental. Cada nuevo nivel agrega a la autenticación proporcionada por el nivel anterior. Si la biblioteca en tiempo de ejecución de RPC no admite el nivel especificado, se actualiza automáticamente al siguiente nivel admitido superior.



| Constante                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**\_ \_ \_ nivel predeterminado de autenticación de RPC C \_**</dt> </dl>                    | Usa el nivel de autenticación predeterminado para el servicio de autenticación especificado.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**nivel de autenticación de RPC \_ C \_ \_ \_ ninguno**</dt> </dl>                             | No realiza ninguna autenticación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**\_conexión de \_ nivel de \_ autenticación \_ de RPC C**</dt> </dl>                    | Solo se realiza la autenticación cuando el cliente establece una relación con un servidor.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**\_llamada de \_ nivel de \_ autenticación \_ de RPC C**</dt> </dl>                             | Solo se autentica al principio de cada llamada a procedimiento remoto cuando el servidor recibe la solicitud. No se aplica a las llamadas a procedimientos remotos realizadas mediante secuencias de protocolo basadas en conexión (las que comienzan con el prefijo "ncacn"). Si la secuencia de protocolo en un identificador de enlace es una secuencia de protocolo basada en conexión y se especifica este nivel, en su lugar, esta rutina usa la constante PKT de nivel de autenticación de RPC \_ C \_ \_ \_ .<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**\_PKT de \_ nivel de \_ autenticación \_ de RPC C**</dt> </dl>                                | Solo autentica que todos los datos recibidos provienen del cliente esperado. No valida los datos en sí.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**integridad de la PKT de nivel de autenticación de RPC \_ C \_ \_ \_ \_**</dt> </dl> | Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**\_privacidad de \_ nivel de \_ autenticación \_ de RPC C \_**</dt> </dl>       | Incluye todos los niveles anteriores y garantiza que los datos de texto no cifrado solo los puede visualizar el remitente y el receptor. En el caso local, esto implica el uso de un canal seguro. En el caso remoto, esto implica cifrar el valor del argumento de cada llamada a procedimiento remoto.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Observaciones

Independientemente del valor especificado por la constante, **ncalrpc** siempre usa la privacidad de nivel de autenticación de RPC \_ C \_ \_ \_ \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





