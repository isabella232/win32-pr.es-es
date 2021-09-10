---
title: Constantes de nivel de autenticación (Rpcdce.h)
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369631"
---
# <a name="authentication-level-constants"></a>Constantes de nivel de autenticación

Estos valores especifican un nivel de autenticación, que indica la cantidad de autenticación proporcionada para ayudar a proteger la integridad de los datos. Cada nivel incluye la protección proporcionada por los niveles anteriores.



| Constante o valor                                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT**</dt> <dt>0</dt> </dl>                    | Indica a DCOM que elija el nivel de autenticación mediante su algoritmo de negociación normal de negociación de seguridad. Para obtener más información, vea [Negociación de negociación de seguridad.](security-blanket-negotiation.md) <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ NONE**</dt> <dt>1</dt> </dl>                             | No realiza ninguna autenticación.<br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT**</dt> <dt>2</dt> </dl>                    | Autentica las credenciales del cliente solo cuando el cliente establece una relación con el servidor. Los transportes de datagramas siempre usan RPC \_ AUTHN \_ LEVEL \_ PKT en su lugar. <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ CALL**</dt> <dt>3</dt> </dl>                             | Solo se autentica al principio de cada llamada a procedimiento remoto cuando el servidor recibe la solicitud. Los transportes de datagramas usan RPC \_ C \_ AUTHN \_ LEVEL \_ PKT en su lugar.<br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT**</dt> <dt>4</dt> </dl>                                | Autentica que todos los datos recibidos son del cliente esperado.<br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ INTEGRIDAD PKT DE NIVEL DE \_ \_ \_ AUTENTICACIÓN \_ DE C**</dt> <dt>5</dt> </dl> | Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.<br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**</dt> <dt>6</dt> </dl>       | Autentica todos los niveles anteriores y cifra el valor del argumento de cada llamada a procedimiento remoto.<br/>                                                                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



 

 





