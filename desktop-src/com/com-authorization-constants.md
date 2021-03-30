---
title: Constantes de autorización (RpcDce. h)
description: Define lo que el servidor autoriza.
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
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803932"
---
# <a name="authorization-constants"></a>Constantes de autorización

Define lo que el servidor autoriza.



| Constante o valor                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt> </dl>                   | El servidor no realiza ninguna autorización. Actualmente, RPC \_ c \_ authn \_ WinNT, RPC \_ c \_ authn \_ GSS \_ Schannel y RPC \_ c \_ authn \_ GSS \_ Kerberos usan solo RPC \_ c \_ AUTHZ \_ None.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ nombre**</dt> <dt>1</dt> </dl>                   | El servidor realiza la autorización en función del nombre principal del cliente. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | El servidor realiza la comprobación de autorización utilizando la información del certificado de atributo de privilegio (PAC) del cliente, que se envía al servidor con cada llamada a procedimiento remoto realizada mediante el identificador de enlace. Por lo general, se comprueba el acceso a las listas de control de acceso (ACL) de DCE. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ default**</dt> <dt>0xFFFFFFFF</dt> </dl> | DCOM puede elegir el nivel de autorización mediante su algoritmo normal de negociación de seguridad. Para obtener más información, vea negociación de la [capa de seguridad](security-blanket-negotiation.md).<br/>                                                                                           |



## <a name="remarks"></a>Observaciones

Los métodos de la interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) usan estas constantes. Se usan en la única estructura del [**\_ \_ servicio de autenticación**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , que se recupera mediante la función [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . También se usan en la estructura [**de \_ \_ información de autenticación única**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , que a su vez es miembro de la estructura de la [**\_ \_ lista de autenticación única**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) . Esta estructura, que es una lista de servicios de autenticación, los servicios de autorización que realizan y la información de autenticación para cada servicio, se pasa a la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y al método [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>RpcDce. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Fall**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**\_información de autenticación única \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**\_servicio de autenticación único \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

