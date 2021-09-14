---
title: Authentication-Service constantes (Rpcdce.h)
description: Las constantes del servicio de autenticación representan los servicios de autenticación pasados a varias funciones en tiempo de ejecución.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
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
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173545"
---
# <a name="authentication-service-constants"></a>Authentication-Service constantes

Las constantes del servicio de autenticación representan los servicios de autenticación pasados a varias funciones en tiempo de ejecución.

Las siguientes constantes son valores válidos para el *parámetro AuthnSvc.*



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ NONE**</dt> <dt>0</dt> </dl>                              | Sin autenticación.<br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ PRIVATE**</dt> <dt>1</dt> </dl>        | Use la autenticación de clave privada de Distributed Computing Environment (DCE).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ PUBLIC**</dt> <dt>2</dt> </dl>           | Autenticación de clave pública de DCE (reservada para uso futuro).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DEC \_ PUBLIC**</dt> <dt>4</dt> </dl>           | Autenticación de clave pública de DEC (reservada para uso futuro).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ NEGOTIATE**</dt> <dt>9</dt> </dl>  | Use [el SSP de Microsoft Negotiate.](/windows/desktop/SecAuthN/microsoft-negotiate) Este SSP negocia entre el uso de los proveedores de compatibilidad de seguridad (SSP) del protocolo NTLM y Kerberos.<br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ WINNT**</dt> <dt>10</dt> </dl>                          | Use el [SSP de Microsoft NT LAN Manager (NTLM).](/windows/desktop/SecAuthN/microsoft-ntlm)<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL**</dt> <dt>14</dt> </dl>    | Use [SChannel SSP](/windows/desktop/SecAuthN/secure-channel). Este SSP admite Capa de sockets seguros (SSL), tecnología de comunicación privada (PCT) y seguridad de nivel de transporte (TLS).<br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS**</dt> <dt>16</dt> </dl>    | Use el [SSP de Microsoft Kerberos.](/windows/desktop/SecAuthN/microsoft-kerberos)<br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DPA**</dt> <dt>17</dt> </dl>                                | Use la autenticación con contraseña distribuida (DPA).<br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MSN**</dt> <dt>18</dt> </dl>                                | Protocolo de autenticación SSP usado para Microsoft Network (MSN).<br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DIGEST**</dt> <dt>21</dt> </dl>                       | Windows XP o posterior: Use el [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)<br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ EXTENSOR \_ \_ NEGO \_ DE C AUTHN**</dt> <dt>30</dt> </dl> | Windows 7 o posterior: Reservado. No debe usarse<br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MQ**</dt> <dt>100</dt> </dl>                                  | Este SSP proporciona un contenedor compatible con SSPI para el protocolo de nivel de transporte de cola de mensajes de Microsoft (MSMQ).<br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DEFAULT**</dt> <dt>0xffffffff</dt> </dl>            | Use el servicio de autenticación predeterminado.<br/>                                                                                                                                   |



## <a name="remarks"></a>Observaciones

Especifique RPC C AUTHN NONE para desactivar la autenticación de las llamadas a \_ \_ procedimiento remoto \_ realizadas a través de un identificador de enlace. Al especificar RPC C AUTHN DEFAULT, la biblioteca en tiempo de ejecución de RPC usa el servicio de autenticación \_ \_ RPC C \_ \_ \_ AUTHN \_ WINNT para las llamadas a procedimiento remoto realizadas mediante el identificador de enlace.

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

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

