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
# <a name="authorization-constants"></a><span data-ttu-id="25347-103">Constantes de autorización</span><span class="sxs-lookup"><span data-stu-id="25347-103">Authorization Constants</span></span>

<span data-ttu-id="25347-104">Define lo que el servidor autoriza.</span><span class="sxs-lookup"><span data-stu-id="25347-104">Defines what the server authorizes.</span></span>



| <span data-ttu-id="25347-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="25347-105">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="25347-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="25347-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="25347-107"><dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="25347-107"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="25347-108">El servidor no realiza ninguna autorización.</span><span class="sxs-lookup"><span data-stu-id="25347-108">The server performs no authorization.</span></span> <span data-ttu-id="25347-109">Actualmente, RPC \_ c \_ authn \_ WinNT, RPC \_ c \_ authn \_ GSS \_ Schannel y RPC \_ c \_ authn \_ GSS \_ Kerberos usan solo RPC \_ c \_ AUTHZ \_ None.</span><span class="sxs-lookup"><span data-stu-id="25347-109">Currently, RPC\_C\_AUTHN\_WINNT, RPC\_C\_AUTHN\_GSS\_SCHANNEL, and RPC\_C\_AUTHN\_GSS\_KERBEROS all use only RPC\_C\_AUTHZ\_NONE.</span></span><br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="25347-110"><dt>**RPC \_ C \_ AUTHZ \_ nombre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="25347-110"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="25347-111">El servidor realiza la autorización en función del nombre principal del cliente.</span><span class="sxs-lookup"><span data-stu-id="25347-111">The server performs authorization based on the client's principal name.</span></span> <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="25347-112"><dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="25347-112"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="25347-113">El servidor realiza la comprobación de autorización utilizando la información del certificado de atributo de privilegio (PAC) del cliente, que se envía al servidor con cada llamada a procedimiento remoto realizada mediante el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="25347-113">The server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="25347-114">Por lo general, se comprueba el acceso a las listas de control de acceso (ACL) de DCE.</span><span class="sxs-lookup"><span data-stu-id="25347-114">Generally, access is checked against DCE access control lists (ACLs).</span></span> <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="25347-115"><dt>**RPC \_ C \_ AUTHZ \_ default**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="25347-115"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="25347-116">DCOM puede elegir el nivel de autorización mediante su algoritmo normal de negociación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="25347-116">DCOM can choose the authorization level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="25347-117">Para obtener más información, vea negociación de la [capa de seguridad](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="25347-117">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="25347-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25347-118">Remarks</span></span>

<span data-ttu-id="25347-119">Los métodos de la interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) usan estas constantes.</span><span class="sxs-lookup"><span data-stu-id="25347-119">These constants are used by methods of the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="25347-120">Se usan en la única estructura del [**\_ \_ servicio de autenticación**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , que se recupera mediante la función [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .</span><span class="sxs-lookup"><span data-stu-id="25347-120">They are used in the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) structure, which is retrieved by the [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) function.</span></span> <span data-ttu-id="25347-121">También se usan en la estructura [**de \_ \_ información de autenticación única**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , que a su vez es miembro de la estructura de la [**\_ \_ lista de autenticación única**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) .</span><span class="sxs-lookup"><span data-stu-id="25347-121">They are also used in the [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structure, which in turn is a member of the [**SOLE\_AUTHENTICATION\_LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) structure.</span></span> <span data-ttu-id="25347-122">Esta estructura, que es una lista de servicios de autenticación, los servicios de autorización que realizan y la información de autenticación para cada servicio, se pasa a la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y al método [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .</span><span class="sxs-lookup"><span data-stu-id="25347-122">This structure, which is a list of authentication services, the authorization services they perform, and the authentication information for each service, is passed to the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function and the [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="25347-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25347-123">Requirements</span></span>



| <span data-ttu-id="25347-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="25347-124">Requirement</span></span> | <span data-ttu-id="25347-125">Value</span><span class="sxs-lookup"><span data-stu-id="25347-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25347-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25347-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25347-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="25347-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="25347-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25347-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25347-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25347-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="25347-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25347-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="25347-131"><dt>RpcDce. h</dt></span><span class="sxs-lookup"><span data-stu-id="25347-131"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25347-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="25347-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25347-133">**Fall**</span><span class="sxs-lookup"><span data-stu-id="25347-133">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="25347-134">**CoQueryAuthenticationServices**</span><span class="sxs-lookup"><span data-stu-id="25347-134">**CoQueryAuthenticationServices**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[<span data-ttu-id="25347-135">**IClientSecurity**</span><span class="sxs-lookup"><span data-stu-id="25347-135">**IClientSecurity**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[<span data-ttu-id="25347-136">**\_información de autenticación única \_**</span><span class="sxs-lookup"><span data-stu-id="25347-136">**SOLE\_AUTHENTICATION\_INFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[<span data-ttu-id="25347-137">**\_servicio de autenticación único \_**</span><span class="sxs-lookup"><span data-stu-id="25347-137">**SOLE\_AUTHENTICATION\_SERVICE**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

