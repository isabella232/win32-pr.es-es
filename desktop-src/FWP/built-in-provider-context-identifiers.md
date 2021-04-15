---
title: Identificadores de contexto de proveedor integrados (Fwpmu. h)
description: Los contextos de proveedor integrados identifican las directivas predeterminadas que se usarán con los sockets seguros.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488998"
---
# <a name="built-in-provider-context-identifiers"></a><span data-ttu-id="70936-103">Identificadores de contexto de proveedor integrados</span><span class="sxs-lookup"><span data-stu-id="70936-103">Built-in Provider Context Identifiers</span></span>

<span data-ttu-id="70936-104">Los identificadores de los contextos de proveedor integrados en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="70936-104">The identifiers for the provider contexts that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="70936-105">Estos contextos de proveedor integrados identifican las directivas predeterminadas que se usarán con los sockets seguros.</span><span class="sxs-lookup"><span data-stu-id="70936-105">These built-in provider contexts identify the default policies to use with secure sockets.</span></span>

<span data-ttu-id="70936-106">Estos identificadores se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="70936-106">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="70936-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**\_proveedor de \_ \_ \_ sockets seguros \_ AUTHIP de contexto de proveedor FWPM**</span><span class="sxs-lookup"><span data-stu-id="70936-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="70936-108">Directiva predeterminada de modo principal de protocolo de Internet autenticado (AuthIP) para sockets seguros.</span><span class="sxs-lookup"><span data-stu-id="70936-108">Authenticated Internet Protocol (AuthIP) main mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70936-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**\_contexto de proveedor \_ seguro de \_ \_ sockets seguros \_ IPSec de FWPM**</span><span class="sxs-lookup"><span data-stu-id="70936-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="70936-110">Directiva predeterminada de modo rápido del Protocolo de seguridad de Internet (IPsec) para sockets seguros.</span><span class="sxs-lookup"><span data-stu-id="70936-110">Internet Protocol Security (IPsec) quick mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70936-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70936-111">Requirements</span></span>



| <span data-ttu-id="70936-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="70936-112">Requirement</span></span> | <span data-ttu-id="70936-113">Value</span><span class="sxs-lookup"><span data-stu-id="70936-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70936-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70936-114">Minimum supported client</span></span><br/> | <span data-ttu-id="70936-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70936-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="70936-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70936-116">Minimum supported server</span></span><br/> | <span data-ttu-id="70936-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="70936-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="70936-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70936-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="70936-119"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="70936-119"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





