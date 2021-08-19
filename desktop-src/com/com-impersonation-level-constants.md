---
title: Constantes de nivel de suplantación (RpcDce.h)
description: Especifica un nivel de suplantación, que indica la cantidad de autoridad que se da al servidor cuando suplanta al cliente.
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
ms.openlocfilehash: 7dbc4b4a74871eb111b778d798587e53027053fe57cc8cda837a3aafb7c24d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048495"
---
# <a name="impersonation-level-constants"></a>Constantes de nivel de suplantación

Especifica un nivel de suplantación, que indica la cantidad de autoridad que se da al servidor cuando suplanta al cliente.



| Constante o valor                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ DEFAULT**</dt> <dt>0</dt> </dl>             | DCOM puede elegir el nivel de suplantación mediante su algoritmo de negociación normal de negociación de seguridad. Para obtener más información, vea [Negociación de negociación de negociación de negociación de negociación de seguridad.](security-blanket-negotiation.md)<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS**</dt> <dt>1</dt> </dl>       | El cliente es anónimo para el servidor. El proceso de servidor puede suplantar al cliente, pero el token de suplantación no contendrá ninguna información y no se puede usar.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_ IDENTIFICACIÓN \_ DE NIVEL DE \_ IMP \_**</dt> DE C <dt>2</dt> </dl>          | El servidor puede obtener la identidad del cliente. El servidor puede suplantar al cliente para la comprobación de ACL, pero no puede acceder a los objetos del sistema como el cliente. <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_ \_ \_ SUPLANTACIÓN \_**</dt> DE NIVEL DE IMP DE C <dt>3</dt> </dl> | El proceso de servidor puede suplantar el contexto de seguridad del cliente mientras actúa en nombre del cliente. Este nivel de suplantación puede utilizarse para obtener acceso a recursos locales, como los archivos. Al suplantar en este nivel, el token de suplantación solo se puede pasar a través de un límite de máquina. El [servicio de autenticación Schannel](schannel.md) solo admite este nivel de suplantación. <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_ DELEGADO \_ DE NIVEL DE \_ \_ IMP**</dt> DE C <dt>4</dt> </dl>          | El proceso de servidor puede suplantar el contexto de seguridad del cliente mientras actúa en nombre del cliente. El proceso de servidor también puede realizar llamadas salientes a otros servidores mientras actúa en nombre del cliente, mediante el uso de la creación de un dispositivo. El servidor puede usar el contexto de seguridad del cliente en otras máquinas para acceder a recursos locales y remotos como el cliente. Al suplantar en este nivel, el token de suplantación se puede pasar a través de cualquier número de límites del equipo.<br/> |



## <a name="remarks"></a>Comentarios

[**GetUserName producirá**](/windows/desktop/api/winbase/nf-winbase-getusernamea) un error al suplantar en el nivel de identificación. La solución alternativa consiste en suplantar, llamar [**a OpenThreadToken,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)revertir, llamar a [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)y, por último, llamar a [**LookupAccountSid.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) Con [**CoSetProxyBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)el cliente establece el nivel de suplantación

Con [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), el cliente establece el nivel de suplantación y la identidad de proxy que estarán disponibles cuando un servidor llame a [**CoImpersonateClient.**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient) La identidad que verá el servidor cuando se lleve a cabo la suplantación se describe en [La suplantación.](cloaking.md) Tenga en cuenta que al realizar una llamada mientras se suplanta, el destinatario normalmente recibirá el token de proceso del autor de la llamada, no el token de suplantación del autor de la llamada. Para recibir el token de suplantación del autor de la llamada, el autor de la llamada debe habilitar la activación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>RpcDce.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ocultación](cloaking.md)
</dt> </dl>

 

