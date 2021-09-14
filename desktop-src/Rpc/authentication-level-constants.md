---
title: Authentication-Level constantes (Rpcdce.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173549"
---
# <a name="authentication-level-constants"></a>Constantes de nivel de autenticación

Las constantes de nivel de autenticación representan los niveles de autenticación pasados a varias funciones en tiempo de ejecución. Estos niveles se enumeran en orden de aumento de la autenticación. Cada nuevo nivel se agrega a la autenticación proporcionada por el nivel anterior. Si la biblioteca en tiempo de ejecución rpc no admite el nivel especificado, se actualiza automáticamente al siguiente nivel compatible superior.



| Constante                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT**</dt> </dl>                    | Usa el nivel de autenticación predeterminado para el servicio de autenticación especificado.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ NONE**</dt> </dl>                             | No realiza ninguna autenticación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**CONEXIÓN \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE RPC C \_**</dt> </dl>                    | Solo se realiza la autenticación cuando el cliente establece una relación con un servidor.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**LLAMADA \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE RPC C \_**</dt> </dl>                             | Solo se autentica al principio de cada llamada a procedimiento remoto cuando el servidor recibe la solicitud. No se aplica a las llamadas a procedimientos remotos realizadas mediante las secuencias de protocolo basadas en la conexión (aquellas que comienzan con el prefijo "ncacn"). Si la secuencia de protocolo de un identificador de enlace es una secuencia de protocolo basada en conexiones y especifica este nivel, esta rutina usa en su lugar la constante PKT RPC \_ C \_ AUTHN \_ \_ LEVEL.<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT**</dt> </dl>                                | Autentica solo que todos los datos recibidos son del cliente esperado. No valida los propios datos.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY**</dt> </dl> | Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**</dt> </dl>       | Incluye todos los niveles anteriores y garantiza que solo el remitente y el receptor puedan ver los datos de texto no deseado. En el caso local, esto implica el uso de un canal seguro. En el caso remoto, esto implica cifrar el valor del argumento de cada llamada a procedimiento remoto.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Observaciones

Independientemente del valor especificado por la constante, **ncalrpc** siempre usa RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



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

 

 





