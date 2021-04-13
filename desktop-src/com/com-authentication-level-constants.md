---
title: Constantes de nivel de autenticación (Rpcdce. h)
description: Estos valores especifican un nivel de autenticación, que indica la cantidad de autenticación proporcionada para ayudar a proteger la integridad de los datos. Cada nivel incluye la protección proporcionada por los niveles anteriores.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
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
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535446"
---
# <a name="authentication-level-constants"></a>Constantes de nivel de autenticación

Estos valores especifican un nivel de autenticación, que indica la cantidad de autenticación proporcionada para ayudar a proteger la integridad de los datos. Cada nivel incluye la protección proporcionada por los niveles anteriores.



| Constante o valor                                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ \_ \_ \_ Valor predeterminado de nivel de autenticación de C**</dt> <dt>0</dt> </dl>                    | Indica a DCOM que elija el nivel de autenticación mediante su algoritmo de negociación global de seguridad normal. Para obtener más información, vea negociación de la [capa de seguridad](security-blanket-negotiation.md). <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ authn \_ nivel \_ ninguno**</dt> <dt>1</dt> </dl>                             | No realiza ninguna autenticación.<br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ C \_ authn \_ LEVEL \_ Connect**</dt> <dt>2</dt> </dl>                    | Autentica las credenciales del cliente solo cuando el cliente establece una relación con el servidor. Los transportes de datagramas siempre utilizan el nivel de introducción de autenticación de RPC \_ \_ \_ . <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_ \_ \_ \_ Llamada de nivel**</dt> <dt>3</dt> de autenticación de C </dl>                             | Solo se autentica al principio de cada llamada a procedimiento remoto cuando el servidor recibe la solicitud. Los transportes de datagramas usan \_ PKT de nivel de autenticación de RPC C \_ \_ \_ en su lugar.<br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ \_Nivel de autenticación \_ \_ de C**</dt> <dt>4</dt> </dl>                                | Autentica que todos los datos recibidos provienen del cliente esperado.<br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ \_Integridad de la \_ \_ PKT \_ de nivel de autenticación de C**</dt> <dt>5</dt> </dl> | Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.<br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ \_ \_ \_ \_ Privacidad de nivel de autenticación de C**</dt> <dt></dt> </dl>       | Autentica todos los niveles anteriores y cifra el valor del argumento de cada llamada a procedimiento remoto.<br/>                                                                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





