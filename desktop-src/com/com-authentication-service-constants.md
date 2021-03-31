---
title: Constantes del servicio de autenticación (RpcDce. h)
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
ms.openlocfilehash: 1227d2accdf871c2e57a25661837d10089c983ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151165"
---
# <a name="authentication-service-constants"></a>Constantes del servicio de autenticación

Define los servicios de autenticación mediante la identificación del paquete de seguridad que proporciona el servicio, como NTLMSSP, Kerberos o Schannel.



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ authn \_ None**</dt> <dt>0</dt> </dl>                              | Sin autenticación.<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ authn \_ DCE \_ privado**</dt> <dt>1</dt> </dl>        | Autenticación de clave privada de DCE.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ authn \_ DCE \_ público**</dt> <dt>2</dt> </dl>           | Autenticación de clave pública DCE.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ authn \_ Dec \_ público**</dt> <dt>4</dt> </dl>           | Autenticación de clave pública DEC. Reservado para uso futuro.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ Negotiate Negotiate**</dt> <dt>9</dt> </dl>  | Proveedor de compatibilidad con seguridad de Snego.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ authn \_ WinNT**</dt> <dt>10</dt> </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ Schannel**</dt> <dt>14</dt> </dl>    | Proveedor de compatibilidad con seguridad de Schannel. Este servicio de autenticación admite SSL 2,0, SSL 3,0, TLS y PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Proveedor de compatibilidad con seguridad de Kerberos.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ authn \_ DPA**</dt> <dt>17</dt> </dl>                                | Proveedor de compatibilidad con seguridad de DPA.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ authn \_ MSN**</dt> <dt>18</dt> </dl>                                | Proveedor de soporte técnico de seguridad de MSN.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ \_ \_ Kernel de autenticación de C**</dt> <dt>20</dt> </dl>                       | Proveedor de compatibilidad de seguridad del kernel.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ \_ \_ Resumen de autenticación de C**</dt> <dt>21</dt> </dl>                       | Proveedor de compatibilidad con seguridad implícita.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ \_ \_ \_ Extensor nego de C authn**</dt> <dt>30</dt> </dl> | Proveedor de compatibilidad con seguridad de NEGO extender.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C \_ authn \_ PKU2U**</dt> <dt>31</dt> </dl>                          | Proveedor de compatibilidad con seguridad de PKU2U.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ authn \_ MQ**</dt> <dt>100</dt> </dl>                                  | Proveedor de compatibilidad con seguridad MQ.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ authn \_ default**</dt> <dt>0xFFFFFFFFL</dt> </dl>           | Servicio de autenticación predeterminado del sistema. Cuando se especifica este valor, COM usa su algoritmo de negociación global de seguridad normal para elegir un servicio de autenticación. Para obtener más información, vea negociación de la [capa de seguridad](security-blanket-negotiation.md). <br/> |



## <a name="remarks"></a>Observaciones

Estas constantes se utilizan en el [**servicio de \_ autenticación \_ único**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) y las estructuras de [**\_ \_ información de autenticación única**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) . El servidor pasa la única estructura del **\_ \_ servicio de autenticación** a la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y se puede recuperar mediante la función [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . El cliente pasa a **CoInitializeSecurity** un puntero a una estructura de **\_ \_ información de autenticación única** . Para obtener más información sobre los paquetes de seguridad identificados por estos valores, como NTLMSSP y Kerberos, consulte [com and Security Packages](com-and-security-packages.md).

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

 

