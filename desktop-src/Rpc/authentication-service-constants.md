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
# <a name="authentication-service-constants"></a><span data-ttu-id="e5074-103">Constantes de Authentication-Service</span><span class="sxs-lookup"><span data-stu-id="e5074-103">Authentication-Service Constants</span></span>

<span data-ttu-id="e5074-104">Las constantes del servicio de autenticación representan los servicios de autenticación pasados a varias funciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e5074-104">The authentication service constants represent the authentication services passed to various run-time functions.</span></span>

<span data-ttu-id="e5074-105">Las siguientes constantes son valores válidos para el parámetro *AuthnSvc* .</span><span class="sxs-lookup"><span data-stu-id="e5074-105">The following constants are valid values for the *AuthnSvc* parameter.</span></span>



| <span data-ttu-id="e5074-106">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="e5074-106">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="e5074-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5074-107">Description</span></span>                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <span data-ttu-id="e5074-108"><dt>**RPC \_ C \_ authn \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-108"><dt>**RPC\_C\_AUTHN\_NONE**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="e5074-109">Sin autenticación.</span><span class="sxs-lookup"><span data-stu-id="e5074-109">No authentication.</span></span><br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <span data-ttu-id="e5074-110"><dt>**RPC \_ C \_ authn \_ DCE \_ privado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-110"><dt>**RPC\_C\_AUTHN\_DCE\_PRIVATE**</dt> <dt>1</dt></span></span> </dl>        | <span data-ttu-id="e5074-111">Use la autenticación de clave privada del entorno de computación distribuida (DCE).</span><span class="sxs-lookup"><span data-stu-id="e5074-111">Use Distributed Computing Environment (DCE) private key authentication.</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <span data-ttu-id="e5074-112"><dt>**RPC \_ C \_ authn \_ DCE \_ público**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-112"><dt>**RPC\_C\_AUTHN\_DCE\_PUBLIC**</dt> <dt>2</dt></span></span> </dl>           | <span data-ttu-id="e5074-113">Autenticación de clave pública DCE (reservada para uso futuro).</span><span class="sxs-lookup"><span data-stu-id="e5074-113">DCE public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <span data-ttu-id="e5074-114"><dt>**RPC \_ C \_ authn \_ Dec \_ público**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-114"><dt>**RPC\_C\_AUTHN\_DEC\_PUBLIC**</dt> <dt>4</dt></span></span> </dl>           | <span data-ttu-id="e5074-115">Autenticación de clave pública DEC (reservada para uso futuro).</span><span class="sxs-lookup"><span data-stu-id="e5074-115">DEC public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <span data-ttu-id="e5074-116"><dt>**RPC \_ C \_ authn \_ GSS \_ Negotiate Negotiate**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-116"><dt>**RPC\_C\_AUTHN\_GSS\_NEGOTIATE**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="e5074-117">Use [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span><span class="sxs-lookup"><span data-stu-id="e5074-117">Use the [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span></span> <span data-ttu-id="e5074-118">Este SSP negocia entre el uso de los proveedores de compatibilidad de seguridad (SSP) de NTLM y Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e5074-118">This SSP negotiates between the use of the NTLM and Kerberos protocol Security Support Providers (SSP).</span></span><br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <span data-ttu-id="e5074-119"><dt>**RPC \_ C \_ authn \_ WinNT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-119"><dt>**RPC\_C\_AUTHN\_WINNT**</dt> <dt>10</dt></span></span> </dl>                          | <span data-ttu-id="e5074-120">Use el [proveedor de Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).</span><span class="sxs-lookup"><span data-stu-id="e5074-120">Use the [Microsoft NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm).</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <span data-ttu-id="e5074-121"><dt>**RPC \_ C \_ authn \_ GSS \_ Schannel**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-121"><dt>**RPC\_C\_AUTHN\_GSS\_SCHANNEL**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="e5074-122">Usar el [SSP de Schannel](/windows/desktop/SecAuthN/secure-channel).</span><span class="sxs-lookup"><span data-stu-id="e5074-122">Use the [Schannel SSP](/windows/desktop/SecAuthN/secure-channel).</span></span> <span data-ttu-id="e5074-123">Este SSP es compatible con la capa de sockets seguros (SSL), la tecnología de comunicaciones privadas (PCT) y la seguridad de nivel de transporte (TLS).</span><span class="sxs-lookup"><span data-stu-id="e5074-123">This SSP supports Secure Socket Layer (SSL), private communication technology (PCT), and transport level security (TLS).</span></span><br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <span data-ttu-id="e5074-124"><dt>**RPC \_ C \_ authn \_ GSS \_ Kerberos**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-124"><dt>**RPC\_C\_AUTHN\_GSS\_KERBEROS**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="e5074-125">Usar [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span><span class="sxs-lookup"><span data-stu-id="e5074-125">Use the [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span></span><br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <span data-ttu-id="e5074-126"><dt>**RPC \_ C \_ authn \_ DPA**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-126"><dt>**RPC\_C\_AUTHN\_DPA**</dt> <dt>17</dt></span></span> </dl>                                | <span data-ttu-id="e5074-127">Usar la autenticación de contraseña distribuida (DPA).</span><span class="sxs-lookup"><span data-stu-id="e5074-127">Use Distributed Password Authentication (DPA).</span></span><br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <span data-ttu-id="e5074-128"><dt>**RPC \_ C \_ authn \_ MSN**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-128"><dt>**RPC\_C\_AUTHN\_MSN**</dt> <dt>18</dt></span></span> </dl>                                | <span data-ttu-id="e5074-129">Protocolo de autenticación SSP utilizado para la red de Microsoft (MSN).</span><span class="sxs-lookup"><span data-stu-id="e5074-129">Authentication protocol SSP used for the Microsoft Network (MSN).</span></span><br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <span data-ttu-id="e5074-130"><dt>**RPC \_ \_ \_ Resumen de autenticación de C**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-130"><dt>**RPC\_C\_AUTHN\_DIGEST**</dt> <dt>21</dt></span></span> </dl>                       | <span data-ttu-id="e5074-131">Windows XP o posterior: usar el [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span><span class="sxs-lookup"><span data-stu-id="e5074-131">Windows XP or later: Use the [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span></span><br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <span data-ttu-id="e5074-132"><dt>**RPC \_ \_ \_ \_ Extensor nego de C authn**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-132"><dt>**RPC\_C\_AUTHN\_NEGO\_EXTENDER**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="e5074-133">Windows 7 o posterior: reservado.</span><span class="sxs-lookup"><span data-stu-id="e5074-133">Windows 7 or later: Reserved.</span></span> <span data-ttu-id="e5074-134">No debe usarse</span><span class="sxs-lookup"><span data-stu-id="e5074-134">Do not use</span></span><br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <span data-ttu-id="e5074-135"><dt>**RPC \_ C \_ authn \_ MQ**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-135"><dt>**RPC\_C\_AUTHN\_MQ**</dt> <dt>100</dt></span></span> </dl>                                  | <span data-ttu-id="e5074-136">Este SSP proporciona un contenedor compatible con SSPI para el protocolo de nivel de transporte de Microsoft Message Queue (MSMQ).</span><span class="sxs-lookup"><span data-stu-id="e5074-136">This SSP provides an SSPI-compatible wrapper for the Microsoft Message Queue (MSMQ) transport-level protocol.</span></span><br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <span data-ttu-id="e5074-137"><dt>**RPC \_ C \_ authn \_ default**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-137"><dt>**RPC\_C\_AUTHN\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl>            | <span data-ttu-id="e5074-138">Usar el servicio de autenticación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e5074-138">Use the default authentication service.</span></span><br/>                                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="e5074-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5074-139">Remarks</span></span>

<span data-ttu-id="e5074-140">Especifique RPC \_ C \_ authn \_ None para desactivar la autenticación de llamadas a procedimientos remotos realizadas en un identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="e5074-140">Specify RPC\_C\_AUTHN\_NONE to turn off authentication for remote procedure calls made over a binding handle.</span></span> <span data-ttu-id="e5074-141">Cuando se especifica el \_ valor predeterminado de autenticación de RPC c \_ \_ , la biblioteca en tiempo de ejecución de RPC utiliza el \_ \_ \_ servicio de autenticación WinNT de RPC c authn para las llamadas a procedimiento remoto realizadas mediante el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="e5074-141">When you specify RPC\_C\_AUTHN\_DEFAULT, the RPC run-time library uses the RPC\_C\_AUTHN\_WINNT authentication service for remote procedure calls made using the binding handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5074-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5074-142">Requirements</span></span>



| <span data-ttu-id="e5074-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5074-143">Requirement</span></span> | <span data-ttu-id="e5074-144">Value</span><span class="sxs-lookup"><span data-stu-id="e5074-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e5074-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5074-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e5074-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e5074-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e5074-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5074-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e5074-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5074-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e5074-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5074-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5074-150"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5074-150"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5074-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5074-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5074-152">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="e5074-152">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="e5074-153">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="e5074-153">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="e5074-154">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="e5074-154">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="e5074-155">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="e5074-155">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="e5074-156">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e5074-156">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="e5074-157">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e5074-157">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

