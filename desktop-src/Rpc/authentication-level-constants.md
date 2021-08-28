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
ms.openlocfilehash: 03c27fa63a437c3c8a93c3d2e5e1f1983e341d5709e986c83459a3f505b46c6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080925"
---
# <a name="authentication-level-constants"></a>Constantes de nivel de autenticación

Las constantes de nivel de autenticación representan los niveles de autenticación pasados a varias funciones en tiempo de ejecución. Estos niveles se enumeran en orden de aumento de la autenticación. Cada nuevo nivel se agrega a la autenticación proporcionada por el nivel anterior. Si la biblioteca en tiempo de ejecución de RPC no admite el nivel especificado, se actualiza automáticamente al siguiente nivel superior admitido.



| Constante                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT**</dt> </dl>                    | Usa el nivel de autenticación predeterminado para el servicio de autenticación especificado.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ NONE**</dt> </dl>                             | No realiza ninguna autenticación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**CONEXIÓN \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE \_ RPC C**</dt> </dl>                    | Solo se realiza la autenticación cuando el cliente establece una relación con un servidor.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**LLAMADA \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE \_ RPC C**</dt> </dl>                             | Solo se autentica al principio de cada llamada a procedimiento remoto cuando el servidor recibe la solicitud. No se aplica a las llamadas a procedimientos remotos realizadas mediante las secuencias de protocolo basadas en conexiones (las que comienzan con el prefijo "ncacn"). Si la secuencia de protocolo de un identificador de enlace es una secuencia de protocolo basada en conexiones y especifica este nivel, esta rutina usa en su lugar la constante \_ RPC C \_ AUTHN \_ LEVEL \_ PKT.<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT**</dt> </dl>                                | Autentica solo que todos los datos recibidos son del cliente esperado. No valida los propios datos.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**INTEGRIDAD PKT DE NIVEL DE \_ \_ \_ \_ AUTENTICACIÓN RPC \_ C**</dt> </dl> | Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**</dt> </dl>       | Incluye todos los niveles anteriores y garantiza que solo el remitente y el receptor puedan ver los datos de texto no especificado. En el caso local, esto implica el uso de un canal seguro. En el caso remoto, esto implica cifrar el valor del argumento de cada llamada a procedimiento remoto.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Comentarios

Independientemente del valor especificado por la constante, **ncalrpc** siempre usa RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





