---
title: Constantes de autorización (RpcDce.h)
description: Define lo que autoriza el servidor.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb89786a0c27c66177bc29861fdcf53a9341f73e498b5627e1cb826e83f61cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048673"
---
# <a name="authorization-constants"></a>Constantes de autorización

Define lo que autoriza el servidor.



| Constante o valor                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NONE**</dt> <dt>0</dt> </dl>                   | El servidor no realiza ninguna autorización. Actualmente, RPC \_ C \_ AUTHN \_ WINNT, RPC \_ C \_ AUTHN \_ GSS SCHANNEL y RPC \_ C \_ \_ AUTHN GSS KERBEROS solo usan RPC \_ C \_ \_ \_ AUTHZ \_ NONE.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NAME**</dt> <dt>1</dt> </dl>                   | El servidor realiza la autorización en función del nombre principal del cliente. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | El servidor realiza la comprobación de autorización mediante la información del certificado de atributo de privilegios (PAC) del DCE del cliente, que se envía al servidor con cada llamada a procedimiento remoto realizada mediante el identificador de enlace. Por lo general, el acceso se comprueba en las listas de control de acceso (ACL) de DCE. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DEFAULT**</dt> <dt>0xffffffff</dt> </dl> | DCOM puede elegir el nivel de autorización mediante su algoritmo de negociación normal de negociación de negociación de seguridad. Para obtener más información, vea [Negociación de negociación de negociación de negociación de seguridad.](security-blanket-negotiation.md)<br/>                                                                                           |



## <a name="remarks"></a>Comentarios

Estos métodos de la interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) usan estas constantes. Se usan en la estructura [**SOLE \_ AUTHENTICATION \_ SERVICE,**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) que recupera la [**función CoQueryAuthenticationServices.**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) También se usan en la estructura [**SOLE \_ AUTHENTICATION \_ INFO,**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) que a su vez es miembro de la [**estructura SOLE AUTHENTICATION \_ \_ LIST.**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) Esta estructura, que es una lista de servicios de autenticación, los servicios de autorización que realizan y la información de autenticación de cada servicio, se pasa a la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y al método [**IClientSecurity::SetBlanket.**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>RpcDce.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**INFORMACIÓN \_ DE \_ AUTENTICACIÓN ÚNICA**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**SERVICIO \_ DE AUTENTICACIÓN \_ ÚNICA**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

