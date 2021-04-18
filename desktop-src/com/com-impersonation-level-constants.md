---
title: Constantes de nivel de suplantación (RpcDce. h)
description: Especifica un nivel de suplantación, que indica la cantidad de autoridad proporcionada al servidor cuando suplanta al cliente.
ms.assetid: ea5a3b46-b607-4192-a3cc-b2ec55ca94a6
topic_type:
- apiref
api_name:
- RPC_C_IMP_LEVEL_DEFAULT
- RPC_C_IMP_LEVEL_ANONYMOUS
- RPC_C_IMP_LEVEL_IDENTIFY
- RPC_C_IMP_LEVEL_IMPERSONATE
- RPC_C_IMP_LEVEL_DELEGATE
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f16ed07235e52d9aefd7bffff9ce430c3978d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359750"
---
# <a name="impersonation-level-constants"></a>Constantes de nivel de suplantación

Especifica un nivel de suplantación, que indica la cantidad de autoridad proporcionada al servidor cuando suplanta al cliente.



| Constante o valor                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_ \_ \_ \_ Valor predeterminado de nivel IMP C**</dt> <dt>0</dt> </dl>             | DCOM puede elegir el nivel de suplantación mediante su algoritmo normal de negociación de seguridad. Para obtener más información, vea negociación de la [capa de seguridad](security-blanket-negotiation.md).<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_ \_Nivel Imp de C \_ \_ anónimo**</dt> <dt>1</dt> </dl>       | El cliente es anónimo para el servidor. El proceso de servidor puede suplantar al cliente, pero el token de suplantación no contendrá ninguna información y no se podrá usar.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_ \_Nivel de \_ \_ IMP**</dt> . de C. <dt>2</dt> </dl>          | El servidor puede obtener la identidad del cliente. El servidor puede suplantar al cliente para la comprobación de la ACL, pero no puede tener acceso a los objetos del sistema como el cliente. <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_ \_ \_ \_ Suplantación de nivel Imp de C**</dt> <dt>3</dt> </dl> | El proceso de servidor puede suplantar el contexto de seguridad del cliente mientras actúa en nombre del cliente. Este nivel de suplantación puede utilizarse para obtener acceso a recursos locales, como los archivos. Al realizar la suplantación en este nivel, el token de suplantación solo se puede pasar a través de un límite de máquina. El servicio de autenticación de [Schannel](schannel.md) solo admite este nivel de suplantación. <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_ \_Delegado de \_ nivel \_ Imp de C**</dt> <dt>4</dt> </dl>          | El proceso de servidor puede suplantar el contexto de seguridad del cliente mientras actúa en nombre del cliente. El proceso de servidor también puede realizar llamadas salientes a otros servidores mientras actúa en nombre del cliente, mediante la ocultación. El servidor puede usar el contexto de seguridad del cliente en otros equipos para tener acceso a los recursos locales y remotos como cliente. Al realizar la suplantación en este nivel, el token de suplantación se puede pasar a través de cualquier número de límites del equipo.<br/> |



## <a name="remarks"></a>Observaciones

[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea) producirá un error durante la suplantación en el nivel de identificación. La solución alternativa es suplantar, llamar a [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken), revertir, llamar a [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)y, por último, llamar a [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Con [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), el cliente establece el nivel de suplantación.

Con [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), el cliente establece el nivel de suplantación y la identidad del proxy que estarán disponibles cuando un servidor llame a [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). La identidad que el servidor verá cuando tenga lugar la suplantación se describe en [Cloaking](cloaking.md). Tenga en cuenta que al efectuar una llamada durante la suplantación, el destinatario recibirá normalmente el token de proceso del llamador, no el token de suplantación del llamador. Para recibir el token de suplantación del autor de la llamada, el autor de la llamada debe habilitar la ocultación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>RpcDce. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Esconder](cloaking.md)
</dt> </dl>

 

