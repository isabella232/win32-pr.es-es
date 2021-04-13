---
title: Constantes de Authorization-Service (Rpcdce. h)
description: Las constantes del servicio de autorización representan los servicios de autorización pasados a varias funciones en tiempo de ejecución.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535596"
---
# <a name="authorization-service-constants"></a><span data-ttu-id="4f87f-103">Constantes de Authorization-Service</span><span class="sxs-lookup"><span data-stu-id="4f87f-103">Authorization-Service Constants</span></span>

<span data-ttu-id="4f87f-104">Las constantes del servicio de autorización representan los servicios de autorización pasados a varias funciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4f87f-104">The authorization service constants represent the authorization services passed to various run-time functions.</span></span>

<span data-ttu-id="4f87f-105">Las siguientes constantes son valores válidos para el parámetro *AuthzSvc* .</span><span class="sxs-lookup"><span data-stu-id="4f87f-105">The following constants are valid values for the *AuthzSvc* parameter.</span></span> <span data-ttu-id="4f87f-106">La mayoría de las aplicaciones buscan RPC \_ C \_ AUTHZ \_ insuficiente.</span><span class="sxs-lookup"><span data-stu-id="4f87f-106">Most applications find RPC\_C\_AUTHZ\_NON sufficient.</span></span>



| <span data-ttu-id="4f87f-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="4f87f-107">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="4f87f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f87f-108">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="4f87f-109"><dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f87f-109"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="4f87f-110">El servidor no realiza ninguna autorización.</span><span class="sxs-lookup"><span data-stu-id="4f87f-110">Server performs no authorization.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="4f87f-111"><dt>**RPC \_ C \_ AUTHZ \_ nombre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4f87f-111"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="4f87f-112">El servidor realiza la autorización en función del nombre principal del cliente.</span><span class="sxs-lookup"><span data-stu-id="4f87f-112">Server performs authorization based on the client's principal name.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="4f87f-113"><dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4f87f-113"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="4f87f-114">El servidor realiza una comprobación de autorización mediante la información del certificado de atributo de privilegio (PAC) del cliente, que se envía al servidor con cada llamada a procedimiento remoto realizada mediante el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="4f87f-114">Server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="4f87f-115">Por lo general, se comprueba el acceso a las listas de control de acceso ([ACL](/windows/desktop/api/winnt/ns-winnt-acl)) de DCE.</span><span class="sxs-lookup"><span data-stu-id="4f87f-115">Generally, access is checked against DCE access control lists ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)).</span></span><br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="4f87f-116"><dt>**RPC \_ C \_ AUTHZ \_ default**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="4f87f-116"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="4f87f-117">El servidor utiliza el servicio de autorización predeterminado para el SSP actual.</span><span class="sxs-lookup"><span data-stu-id="4f87f-117">Server uses the default authorization service for the current SSP.</span></span><br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="4f87f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f87f-118">Requirements</span></span>



| <span data-ttu-id="4f87f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f87f-119">Requirement</span></span> | <span data-ttu-id="4f87f-120">Value</span><span class="sxs-lookup"><span data-stu-id="4f87f-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4f87f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f87f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f87f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4f87f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4f87f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f87f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f87f-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f87f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4f87f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f87f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f87f-126"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f87f-126"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f87f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f87f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f87f-128">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="4f87f-128">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="4f87f-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="4f87f-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="4f87f-130">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="4f87f-130">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="4f87f-131">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="4f87f-131">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="4f87f-132">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="4f87f-132">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="4f87f-133">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="4f87f-133">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[<span data-ttu-id="4f87f-134">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="4f87f-134">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

