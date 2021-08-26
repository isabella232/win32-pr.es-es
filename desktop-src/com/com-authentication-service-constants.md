---
title: Constantes del servicio de autenticación (RpcDce.h)
description: Define los servicios de autenticación mediante la identificación del paquete de seguridad que proporciona el servicio, como NTLMSSP, Kerberos o Schannel.
ms.assetid: c16a8e52-a7f9-40d9-99ef-10b382b5cb3c
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_KERNEL
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_PKU2U
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14cf6f0ab42b03d028d52df8160cad286e8c37af3988d8ca3b9736dad538012e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993785"
---
# <a name="authentication-service-constants"></a>Constantes del servicio de autenticación

Define los servicios de autenticación mediante la identificación del paquete de seguridad que proporciona el servicio, como NTLMSSP, Kerberos o Schannel.



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ NONE**</dt> <dt>0</dt> </dl>                              | Sin autenticación.<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ PRIVATE**</dt> <dt>1</dt> </dl>        | Autenticación de clave privada de DCE.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ PUBLIC**</dt> <dt>2</dt> </dl>           | Autenticación de clave pública de DCE.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DEC \_ PUBLIC**</dt> <dt>4</dt> </dl>           | Autenticación de clave pública de DEC. Reservado para uso futuro.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ NEGOTIATE**</dt> <dt>9</dt> </dl>  | Proveedor de soporte técnico de seguridad de Snego.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ WINNT**</dt> <dt>10</dt> </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL**</dt> <dt>14</dt> </dl>    | Proveedor de soporte técnico de seguridad de Schannel. Este servicio de autenticación admite SSL 2.0, SSL 3.0, TLS y PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS**</dt> <dt>16</dt> </dl>    | Proveedor de compatibilidad de seguridad de Kerberos.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DPA**</dt> <dt>17</dt> </dl>                                | Proveedor de soporte técnico de seguridad de DPA.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MSN**</dt> <dt>18</dt> </dl>                                | Proveedor de soporte técnico de seguridad MSN.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ KERNEL 20 de C \_ \_ AUTHN**</dt> <dt></dt> </dl>                       | Proveedor de compatibilidad con la seguridad del kernel.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DIGEST**</dt> <dt>21</dt> </dl>                       | Proveedor de compatibilidad de seguridad implícita.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ EXTENSOR \_ \_ NEGO \_ DE C AUTHN**</dt> <dt>30</dt> </dl> | Proveedor de compatibilidad de seguridad extensor NEGO.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ PKU2U**</dt> <dt>31</dt> </dl>                          | Proveedor de soporte técnico de seguridad PKU2U.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MQ**</dt> <dt>100</dt> </dl>                                  | Proveedor de compatibilidad de seguridad de MQ.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DEFAULT**</dt> <dt>0xFFFFFFFFL</dt> </dl>           | Servicio de autenticación predeterminado del sistema. Cuando se especifica este valor, COM usa su algoritmo de negociación normal de negociación de seguridad para elegir un servicio de autenticación. Para obtener más información, vea [Negociación de negociación de negociación de negociación de seguridad.](security-blanket-negotiation.md) <br/> |



## <a name="remarks"></a>Comentarios

Estas constantes se usan en las estructuras [**SOLE \_ AUTHENTICATION SERVICE \_ y**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) [**SOLE AUTHENTICATION \_ \_ INFO.**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) El servidor pasa la estructura **SOLE \_ AUTHENTICATION \_ SERVICE** a la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y la función [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) puede recuperarla. El cliente pasa un puntero a **una estructura SOLE AUTHENTICATION \_ \_ INFO** a **CoInitializeSecurity.** Para obtener más información sobre los paquetes de seguridad identificados por estos valores, como NTLMSSP y Kerberos, vea [COM y Paquetes de seguridad](com-and-security-packages.md).

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

 

