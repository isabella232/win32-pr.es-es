---
title: Marcas de registro de interfaz (Rpcdce. h)
description: Las constantes siguientes se usan en el parámetro flags de las funciones RpcServerRegisterIf2 y RpcServerRegisterIfEx.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150959"
---
# <a name="interface-registration-flags"></a><span data-ttu-id="0f4b4-103">Marcas de registro de interfaz</span><span class="sxs-lookup"><span data-stu-id="0f4b4-103">Interface Registration Flags</span></span>

<span data-ttu-id="0f4b4-104">Las constantes siguientes se usan en el parámetro *Flags* de las funciones [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) y [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) .</span><span class="sxs-lookup"><span data-stu-id="0f4b4-104">The following constants are used in the *Flags* parameter of the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) and [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) functions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0f4b4-105">Constante</span><span class="sxs-lookup"><span data-stu-id="0f4b4-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0f4b4-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f4b4-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <span data-ttu-id="0f4b4-107"><dt><strong>0,1</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0f4b4-107"><dt><strong>0</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f4b4-108">Semántica de la interfaz estándar.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-108">Standard interface semantics.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <span data-ttu-id="0f4b4-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0f4b4-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f4b4-110">Cuando se registra esta marca de interfaz, el tiempo de ejecución de RPC invoca la devolución de llamada de seguridad registrada para todas las llamadas, independientemente de la identidad, la secuencia de protocolo o el nivel de autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-110">When this interface flag is registered, the RPC runtime invokes the registered security callback for all calls, regardless of identity, protocol sequence, or authentication level of the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0f4b4-111">Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-111">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span> <span data-ttu-id="0f4b4-112">Cuando no se establece esta marca, RPC filtra automáticamente todas las llamadas no autenticadas antes de que lleguen a la devolución de llamada de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-112">When this flag is not set, RPC automatically filters all unauthenticated calls before they reach the security callback.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <span data-ttu-id="0f4b4-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0f4b4-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f4b4-114">Cuando se registra esta marca de interfaz, el tiempo de ejecución de RPC rechaza las llamadas realizadas por los clientes remotos.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-114">When this interface flag is registered, the RPC runtime rejects calls made by remote clients.</span></span> <span data-ttu-id="0f4b4-115">También se rechazan todas las llamadas locales que usan secuencias de protocolo ncadg_ \* y ncacn_ \*, con la excepción de ncacn_np.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-115">All local calls using ncadg_\* and ncacn_\* protocol sequences are also rejected, with the exception of ncacn_np.</span></span> <span data-ttu-id="0f4b4-116">RPC solo permite llamadas ncacn_NP si la llamada no procede de SRV.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-116">RPC allows ncacn_NP calls only if the call does not come from SRV.</span></span> <span data-ttu-id="0f4b4-117">Siempre se procesan las llamadas desde ncalrpc.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-117">Calls from ncalrpc are always processed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0f4b4-118">Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-118">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <span data-ttu-id="0f4b4-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0f4b4-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f4b4-120">Se trata de una interfaz <strong>de escucha automática</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f4b4-120">This is an <strong>auto-listen</strong> interface.</span></span> <span data-ttu-id="0f4b4-121">El tiempo de ejecución comienza a escuchar las llamadas en cuanto se registra la primera interfaz autoliston y se detiene la escucha cuando se anula el registro de la última interfaz autoliston.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-121">The run time begins listening for calls as soon as the first autolisten interface is registered, and stops listening when the last autolisten interface is unregistered.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <span data-ttu-id="0f4b4-122"><dt><strong>RPC_IF_OLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0f4b4-122"><dt><strong>RPC_IF_OLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f4b4-123">Reservado para OLE.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-123">Reserved for OLE.</span></span> <span data-ttu-id="0f4b4-124">No use esta marca.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-124">Do not use this flag.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <span data-ttu-id="0f4b4-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0f4b4-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f4b4-126">No implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-126">Currently not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <span data-ttu-id="0f4b4-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0f4b4-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f4b4-128">Limita las conexiones a los clientes que usan un nivel de autorización superior a RPC_C_AUTHN_LEVEL_NONE.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-128">Limits connections to clients that use an authorization level higher than RPC_C_AUTHN_LEVEL_NONE.</span></span> <span data-ttu-id="0f4b4-129">Si se especifica esta marca, los clientes pueden pasar a través de la sesión <strong>nula</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f4b4-129">Specifying this flag allows clients to come through on the <strong>NULL</strong> session.</span></span> <span data-ttu-id="0f4b4-130">En Windows XP y Windows Server 2003, estos clientes no están permitidos.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-130">On Windows XP and Windows Server 2003, such clients are not allowed.</span></span> <span data-ttu-id="0f4b4-131">Los clientes que no superan la prueba de RPC_IF_ALLOW_SECURE_ONLY reciben un error de RPC_S_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-131">Clients that fail the RPC_IF_ALLOW_SECURE_ONLY test receive an RPC_S_ACCESS_DENIED error.</span></span> <span data-ttu-id="0f4b4-132">El uso de la marca RPC_IF_ALLOW_SECURE_ONLY no implica ni garantiza un alto nivel de privilegios en la parte del usuario que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-132">Using the RPC_IF_ALLOW_SECURE_ONLY flag does not imply or guarantee a high level of privilege on the part of the calling user.</span></span> <span data-ttu-id="0f4b4-133">RPC solo comprueba si el usuario tiene credenciales válidas; el usuario que realiza la llamada puede estar usando la cuenta invitado u otras cuentas con pocos privilegios.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-133">RPC only checks that the user has valid credentials; the calling user may be using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="0f4b4-134">No asuma privilegios elevados cuando se use RPC_IF_ALLOW_SECURE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-134">Do not assume high privilege when RPC_IF_ALLOW_SECURE_ONLY is used.</span></span><br/> <span data-ttu-id="0f4b4-135"><strong>Windows NT 4,0 y Windows Me/98/95:  </strong></span><span class="sxs-lookup"><span data-stu-id="0f4b4-135"><strong>Windows NT 4.0 and Windows Me/98/95:  </strong></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <span data-ttu-id="0f4b4-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0f4b4-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0f4b4-137">Deshabilita el almacenamiento en caché de devolución de llamada de seguridad, lo que fuerza una devolución de llamada de seguridad para cada llamada RPC en una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-137">Disables security callback caching, forcing a security callback for each RPC call on a given interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0f4b4-138">Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="0f4b4-138">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="0f4b4-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f4b4-139">Requirements</span></span>



| <span data-ttu-id="0f4b4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f4b4-140">Requirement</span></span> | <span data-ttu-id="0f4b4-141">Value</span><span class="sxs-lookup"><span data-stu-id="0f4b4-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f4b4-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f4b4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0f4b4-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0f4b4-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f4b4-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f4b4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0f4b4-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f4b4-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f4b4-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f4b4-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f4b4-147"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f4b4-147"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





