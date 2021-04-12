---
title: Constantes de Authentication-Service (Rpcdce. h)
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535110"
---
# <a name="authentication-service-constants"></a>Constantes de Authentication-Service

Las constantes del servicio de autenticación representan los servicios de autenticación pasados a varias funciones en tiempo de ejecución.

Las siguientes constantes son valores válidos para el parámetro *AuthnSvc* .



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ authn \_ None**</dt> <dt>0</dt> </dl>                              | Sin autenticación.<br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ authn \_ DCE \_ privado**</dt> <dt>1</dt> </dl>        | Use la autenticación de clave privada del entorno de computación distribuida (DCE).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ authn \_ DCE \_ público**</dt> <dt>2</dt> </dl>           | Autenticación de clave pública DCE (reservada para uso futuro).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ authn \_ Dec \_ público**</dt> <dt>4</dt> </dl>           | Autenticación de clave pública DEC (reservada para uso futuro).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ Negotiate Negotiate**</dt> <dt>9</dt> </dl>  | Use [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate). Este SSP negocia entre el uso de los proveedores de compatibilidad de seguridad (SSP) de NTLM y Kerberos.<br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ authn \_ WinNT**</dt> <dt>10</dt> </dl>                          | Use el [proveedor de Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ Schannel**</dt> <dt>14</dt> </dl>    | Usar el [SSP de Schannel](/windows/desktop/SecAuthN/secure-channel). Este SSP es compatible con la capa de sockets seguros (SSL), la tecnología de comunicaciones privadas (PCT) y la seguridad de nivel de transporte (TLS).<br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Usar [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).<br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ authn \_ DPA**</dt> <dt>17</dt> </dl>                                | Usar la autenticación de contraseña distribuida (DPA).<br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ authn \_ MSN**</dt> <dt>18</dt> </dl>                                | Protocolo de autenticación SSP utilizado para la red de Microsoft (MSN).<br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ \_ \_ Resumen de autenticación de C**</dt> <dt>21</dt> </dl>                       | Windows XP o posterior: usar el [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)<br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ \_ \_ \_ Extensor nego de C authn**</dt> <dt>30</dt> </dl> | Windows 7 o posterior: reservado. No debe usarse<br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ authn \_ MQ**</dt> <dt>100</dt> </dl>                                  | Este SSP proporciona un contenedor compatible con SSPI para el protocolo de nivel de transporte de Microsoft Message Queue (MSMQ).<br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ authn \_ default**</dt> <dt>0xFFFFFFFF</dt> </dl>            | Usar el servicio de autenticación predeterminado.<br/>                                                                                                                                   |



## <a name="remarks"></a>Observaciones

Especifique RPC \_ C \_ authn \_ None para desactivar la autenticación de llamadas a procedimientos remotos realizadas en un identificador de enlace. Cuando se especifica el \_ valor predeterminado de autenticación de RPC c \_ \_ , la biblioteca en tiempo de ejecución de RPC utiliza el \_ \_ \_ servicio de autenticación WinNT de RPC c authn para las llamadas a procedimiento remoto realizadas mediante el identificador de enlace.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



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

 

