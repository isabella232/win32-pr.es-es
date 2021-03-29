---
title: Constantes de Authentication-Level (Rpcdce. h)
description: Las constantes de nivel de autenticación representan los niveles de autenticación pasados a varias funciones en tiempo de ejecución.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535115"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="5df7c-103">Constantes de nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="5df7c-103">Authentication-Level Constants</span></span>

<span data-ttu-id="5df7c-104">Las constantes de nivel de autenticación representan los niveles de autenticación pasados a varias funciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5df7c-104">The authentication-level constants represent authentication levels passed to various run-time functions.</span></span> <span data-ttu-id="5df7c-105">Estos niveles se muestran en orden de autenticación incremental.</span><span class="sxs-lookup"><span data-stu-id="5df7c-105">These levels are listed in order of increasing authentication.</span></span> <span data-ttu-id="5df7c-106">Cada nuevo nivel agrega a la autenticación proporcionada por el nivel anterior.</span><span class="sxs-lookup"><span data-stu-id="5df7c-106">Each new level adds to the authentication provided by the previous level.</span></span> <span data-ttu-id="5df7c-107">Si la biblioteca en tiempo de ejecución de RPC no admite el nivel especificado, se actualiza automáticamente al siguiente nivel admitido superior.</span><span class="sxs-lookup"><span data-stu-id="5df7c-107">If the RPC run-time library does not support the specified level, it automatically upgrades to the next higher supported level.</span></span>



| <span data-ttu-id="5df7c-108">Constante</span><span class="sxs-lookup"><span data-stu-id="5df7c-108">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="5df7c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5df7c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="5df7c-110"><dt>**\_ \_ \_ nivel predeterminado de autenticación de RPC C \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5df7c-110"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt></span></span> </dl>                    | <span data-ttu-id="5df7c-111">Usa el nivel de autenticación predeterminado para el servicio de autenticación especificado.</span><span class="sxs-lookup"><span data-stu-id="5df7c-111">Uses the default authentication level for the specified authentication service.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="5df7c-112"><dt>**nivel de autenticación de RPC \_ C \_ \_ \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="5df7c-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="5df7c-113">No realiza ninguna autenticación.</span><span class="sxs-lookup"><span data-stu-id="5df7c-113">Performs no authentication.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="5df7c-114"><dt>**\_conexión de \_ nivel de \_ autenticación \_ de RPC C**</dt></span><span class="sxs-lookup"><span data-stu-id="5df7c-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt></span></span> </dl>                    | <span data-ttu-id="5df7c-115">Solo se realiza la autenticación cuando el cliente establece una relación con un servidor.</span><span class="sxs-lookup"><span data-stu-id="5df7c-115">Authenticates only when the client establishes a relationship with a server.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="5df7c-116"><dt>**\_llamada de \_ nivel de \_ autenticación \_ de RPC C**</dt></span><span class="sxs-lookup"><span data-stu-id="5df7c-116"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt></span></span> </dl>                             | <span data-ttu-id="5df7c-117">Solo se autentica al principio de cada llamada a procedimiento remoto cuando el servidor recibe la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5df7c-117">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="5df7c-118">No se aplica a las llamadas a procedimientos remotos realizadas mediante secuencias de protocolo basadas en conexión (las que comienzan con el prefijo "ncacn").</span><span class="sxs-lookup"><span data-stu-id="5df7c-118">Does not apply to remote procedure calls made using the connection-based protocol sequences (those that start with the prefix "ncacn").</span></span> <span data-ttu-id="5df7c-119">Si la secuencia de protocolo en un identificador de enlace es una secuencia de protocolo basada en conexión y se especifica este nivel, en su lugar, esta rutina usa la constante PKT de nivel de autenticación de RPC \_ C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5df7c-119">If the protocol sequence in a binding handle is a connection-based protocol sequence and you specify this level, this routine instead uses the RPC\_C\_AUTHN\_LEVEL\_PKT constant.</span></span><br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="5df7c-120"><dt>**\_PKT de \_ nivel de \_ autenticación \_ de RPC C**</dt></span><span class="sxs-lookup"><span data-stu-id="5df7c-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt></span></span> </dl>                                | <span data-ttu-id="5df7c-121">Solo autentica que todos los datos recibidos provienen del cliente esperado.</span><span class="sxs-lookup"><span data-stu-id="5df7c-121">Authenticates only that all data received is from the expected client.</span></span> <span data-ttu-id="5df7c-122">No valida los datos en sí.</span><span class="sxs-lookup"><span data-stu-id="5df7c-122">Does not validate the data itself.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="5df7c-123"><dt>**integridad de la PKT de nivel de autenticación de RPC \_ C \_ \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5df7c-123"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt></span></span> </dl> | <span data-ttu-id="5df7c-124">Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="5df7c-124">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="5df7c-125"><dt>**\_privacidad de \_ nivel de \_ autenticación \_ de RPC C \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5df7c-125"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt></span></span> </dl>       | <span data-ttu-id="5df7c-126">Incluye todos los niveles anteriores y garantiza que los datos de texto no cifrado solo los puede visualizar el remitente y el receptor.</span><span class="sxs-lookup"><span data-stu-id="5df7c-126">Includes all previous levels, and ensures clear text data can only be seen by the sender and the receiver.</span></span> <span data-ttu-id="5df7c-127">En el caso local, esto implica el uso de un canal seguro.</span><span class="sxs-lookup"><span data-stu-id="5df7c-127">In the local case, this involves using a secure channel.</span></span> <span data-ttu-id="5df7c-128">En el caso remoto, esto implica cifrar el valor del argumento de cada llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="5df7c-128">In the remote case, this involves encrypting the argument value of each remote procedure call.</span></span><br/>                                                                                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="5df7c-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5df7c-129">Remarks</span></span>

<span data-ttu-id="5df7c-130">Independientemente del valor especificado por la constante, **ncalrpc** siempre usa la privacidad de nivel de autenticación de RPC \_ C \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5df7c-130">Regardless of the value specified by the constant, **ncalrpc** always uses RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df7c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5df7c-131">Requirements</span></span>



| <span data-ttu-id="5df7c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5df7c-132">Requirement</span></span> | <span data-ttu-id="5df7c-133">Value</span><span class="sxs-lookup"><span data-stu-id="5df7c-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5df7c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5df7c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5df7c-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5df7c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5df7c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5df7c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5df7c-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5df7c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5df7c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5df7c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5df7c-139"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df7c-139"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5df7c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5df7c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df7c-141">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="5df7c-141">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="5df7c-142">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="5df7c-142">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="5df7c-143">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="5df7c-143">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[<span data-ttu-id="5df7c-144">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="5df7c-144">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="5df7c-145">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="5df7c-145">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="5df7c-146">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="5df7c-146">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="5df7c-147">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="5df7c-147">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





