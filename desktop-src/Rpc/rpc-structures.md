---
title: Estructuras RPC
description: En esta sección se explican las estructuras definidas y utilizadas por Microsoft RPC.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- RPC, referencia, estructuras de llamada a procedimiento remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793203"
---
# <a name="rpc-structures"></a><span data-ttu-id="18369-104">Estructuras RPC</span><span class="sxs-lookup"><span data-stu-id="18369-104">RPC Structures</span></span>

<span data-ttu-id="18369-105">En esta sección se explican las estructuras definidas y utilizadas por Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="18369-105">This section explains the structures defined and used by Microsoft RPC.</span></span>

-   <span data-ttu-id="18369-106">[**NDR \_ SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="18369-106">[**NDR\_SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span></span>
-   [<span data-ttu-id="18369-107">**VOLUMEN**</span><span class="sxs-lookup"><span data-stu-id="18369-107">**GUID**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [<span data-ttu-id="18369-108">**\_información de \_ serialización de usuario NDR \_**</span><span class="sxs-lookup"><span data-stu-id="18369-108">**NDR\_USER\_MARSHAL\_INFO**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [<span data-ttu-id="18369-109">**\_Información de \_ serialización de usuario NDR \_ \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="18369-109">**NDR\_USER\_MARSHAL\_INFO\_LEVEL1**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [<span data-ttu-id="18369-110">**información de notificación de RPC \_ Async \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18369-110">**RPC\_ASYNC\_NOTIFICATION\_INFO**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [<span data-ttu-id="18369-111">**Estado de RPC \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="18369-111">**RPC\_ASYNC\_STATE**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [<span data-ttu-id="18369-112">**\_Opciones de identificador de enlace RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="18369-112">**RPC\_BINDING\_HANDLE\_OPTIONS\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [<span data-ttu-id="18369-113">**\_Seguridad de controlador de enlace RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="18369-113">**RPC\_BINDING\_HANDLE\_SECURITY\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [<span data-ttu-id="18369-114">**\_Plantilla de identificador de enlace RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="18369-114">**RPC\_BINDING\_HANDLE\_TEMPLATE\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [<span data-ttu-id="18369-115">**\_Vector de enlace RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-115">**RPC\_BINDING\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [<span data-ttu-id="18369-116">**\_descriptor de \_ \_ autenticación de cookies de \_ RPC C \_**</span><span class="sxs-lookup"><span data-stu-id="18369-116">**RPC\_C\_OPT\_COOKIE\_AUTH\_DESCRIPTOR**</span></span>](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [<span data-ttu-id="18369-117">**\_Atributos de llamada RPC \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="18369-117">**RPC\_CALL\_ATTRIBUTES\_V1**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [<span data-ttu-id="18369-118">**\_Atributos de llamada RPC \_ \_ V2**</span><span class="sxs-lookup"><span data-stu-id="18369-118">**RPC\_CALL\_ATTRIBUTES\_V2**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [<span data-ttu-id="18369-119">**\_Dirección local de llamada RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="18369-119">**RPC\_CALL\_LOCAL\_ADDRESS\_V1**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [<span data-ttu-id="18369-120">**\_interfaz de cliente RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-120">**RPC\_CLIENT\_INTERFACE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [<span data-ttu-id="18369-121">**\_tabla de envío de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-121">**RPC\_DISPATCH\_TABLE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [<span data-ttu-id="18369-122">**parámetro de información de RPC \_ EE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18369-122">**RPC\_EE\_INFO\_PARAM**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [<span data-ttu-id="18369-123">**\_plantilla de extremo RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-123">**RPC\_ENDPOINT\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [<span data-ttu-id="18369-124">**\_identificador de \_ enumeración de error de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-124">**RPC\_ERROR\_ENUM\_HANDLE**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [<span data-ttu-id="18369-125">**\_información de \_ error \_ extendido de RPC**</span><span class="sxs-lookup"><span data-stu-id="18369-125">**RPC\_EXTENDED\_ERROR\_INFO**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [<span data-ttu-id="18369-126">**\_ \_ credenciales de transporte http RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-126">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [<span data-ttu-id="18369-127">**\_ \_ Credenciales de transporte http RPC \_ \_ V2**</span><span class="sxs-lookup"><span data-stu-id="18369-127">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [<span data-ttu-id="18369-128">**\_Credenciales de transporte http de RPC \_ \_ \_ V3**</span><span class="sxs-lookup"><span data-stu-id="18369-128">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [<span data-ttu-id="18369-129">**RPC \_ If \_ ID**</span><span class="sxs-lookup"><span data-stu-id="18369-129">**RPC\_IF\_ID**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [<span data-ttu-id="18369-130">**Vector de RPC \_ If \_ ID \_**</span><span class="sxs-lookup"><span data-stu-id="18369-130">**RPC\_IF\_ID\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [<span data-ttu-id="18369-131">**\_plantilla de interfaz RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-131">**RPC\_INTERFACE\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [<span data-ttu-id="18369-132">**\_Directiva RPC**</span><span class="sxs-lookup"><span data-stu-id="18369-132">**RPC\_POLICY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [<span data-ttu-id="18369-133">**\_Vector PROTSEQ de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-133">**RPC\_PROTSEQ\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [<span data-ttu-id="18369-134">**\_QoS de seguridad RPC \_**</span><span class="sxs-lookup"><span data-stu-id="18369-134">**RPC\_SECURITY\_QOS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [<span data-ttu-id="18369-135">**\_QoS de seguridad RPC \_ \_ V2**</span><span class="sxs-lookup"><span data-stu-id="18369-135">**RPC\_SECURITY\_QOS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [<span data-ttu-id="18369-136">**\_QoS de seguridad RPC \_ \_ V3**</span><span class="sxs-lookup"><span data-stu-id="18369-136">**RPC\_SECURITY\_QOS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [<span data-ttu-id="18369-137">**\_QoS de seguridad RPC \_ \_ V4**</span><span class="sxs-lookup"><span data-stu-id="18369-137">**RPC\_SECURITY\_QOS\_V4**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [<span data-ttu-id="18369-138">**QoS de seguridad de RPC \_ \_ \_ V5**</span><span class="sxs-lookup"><span data-stu-id="18369-138">**RPC\_SECURITY\_QOS\_V5**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [<span data-ttu-id="18369-139">**Vector de estadísticas de RPC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18369-139">**RPC\_STATS\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [<span data-ttu-id="18369-140">**\_identidad de autenticación de WinNT s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18369-140">**SEC\_WINNT\_AUTH\_IDENTITY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [<span data-ttu-id="18369-141">**UUID**</span><span class="sxs-lookup"><span data-stu-id="18369-141">**UUID**</span></span>](./rpcdce/ns-rpcdce-uuid.md)
-   [<span data-ttu-id="18369-142">**Vector de UUID \_**</span><span class="sxs-lookup"><span data-stu-id="18369-142">**UUID\_VECTOR**</span></span>](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 