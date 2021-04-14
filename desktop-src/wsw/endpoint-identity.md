---
title: Identidad de extremo
description: Los tipos definidos en esta sección se usan para definir la identidad de seguridad de una dirección de extremo.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Servicios Web de identidad de extremo para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418395"
---
# <a name="endpoint-identity"></a><span data-ttu-id="333dd-106">Identidad de extremo</span><span class="sxs-lookup"><span data-stu-id="333dd-106">Endpoint Identity</span></span>

<span data-ttu-id="333dd-107">Los tipos definidos en esta sección se usan para definir la identidad de seguridad de una dirección de extremo.</span><span class="sxs-lookup"><span data-stu-id="333dd-107">The types defined in this section are used to define the security identity of an endpoint address.</span></span>

<span data-ttu-id="333dd-108">Los elementos de la API siguientes forman parte de la sangría del punto de conexión:</span><span class="sxs-lookup"><span data-stu-id="333dd-108">The following API elements are part of endpoint indentity:</span></span>



| <span data-ttu-id="333dd-109">Enumeración</span><span class="sxs-lookup"><span data-stu-id="333dd-109">Enumeration</span></span>                                                       | <span data-ttu-id="333dd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="333dd-110">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="333dd-111">**\_tipo de \_ identidad de extremo WS \_**</span><span class="sxs-lookup"><span data-stu-id="333dd-111">**WS\_ENDPOINT\_IDENTITY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | <span data-ttu-id="333dd-112">El tipo de la identidad del punto de conexión, que se usa como selector para los subtipos de [**\_ \_ identidad del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span><span class="sxs-lookup"><span data-stu-id="333dd-112">The type of the endpoint identity, used as a selector for subtypes of [**WS\_ENDPOINT\_IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span></span> |



 



| <span data-ttu-id="333dd-113">Estructura</span><span class="sxs-lookup"><span data-stu-id="333dd-113">Structure</span></span>                                                               | <span data-ttu-id="333dd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="333dd-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="333dd-115">**\_identidad del \_ punto de conexión de certificado WS \_**</span><span class="sxs-lookup"><span data-stu-id="333dd-115">**WS\_CERT\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | <span data-ttu-id="333dd-116">El tipo de la identidad del punto de conexión del certificado.</span><span class="sxs-lookup"><span data-stu-id="333dd-116">The type for certificate endpoint identity .</span></span>                                                 |
| [<span data-ttu-id="333dd-117">**\_identidad del \_ punto de conexión DNS de WS \_**</span><span class="sxs-lookup"><span data-stu-id="333dd-117">**WS\_DNS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | <span data-ttu-id="333dd-118">Tipo para especificar una identidad de extremo representada por un nombre DNS.</span><span class="sxs-lookup"><span data-stu-id="333dd-118">The type for specifying an endpoint identity represented by a DNS name.</span></span>                      |
| [<span data-ttu-id="333dd-119">**\_identidad del extremo de WS \_**</span><span class="sxs-lookup"><span data-stu-id="333dd-119">**WS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | <span data-ttu-id="333dd-120">El tipo base para todas las identidades de extremo.</span><span class="sxs-lookup"><span data-stu-id="333dd-120">The base type for all endpoint identities.</span></span>                                                   |
| [<span data-ttu-id="333dd-121">**\_identidad del \_ punto de conexión RSA de WS \_**</span><span class="sxs-lookup"><span data-stu-id="333dd-121">**WS\_RSA\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | <span data-ttu-id="333dd-122">Tipo de identidad de extremo RSA.</span><span class="sxs-lookup"><span data-stu-id="333dd-122">Type for RSA endpoint identity.</span></span>                                                              |
| [<span data-ttu-id="333dd-123">**identidad del extremo de WS \_ SPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="333dd-123">**WS\_SPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | <span data-ttu-id="333dd-124">Tipo para especificar una identidad de extremo representada por un SPN (nombre de entidad de seguridad de servicio).</span><span class="sxs-lookup"><span data-stu-id="333dd-124">The type for specifying an endpoint identity represented by an SPN (service principal name).</span></span> |
| [<span data-ttu-id="333dd-125">**\_identidad de \_ extremo \_ desconocido de WS**</span><span class="sxs-lookup"><span data-stu-id="333dd-125">**WS\_UNKNOWN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | <span data-ttu-id="333dd-126">El tipo para una identidad de extremo desconocida.</span><span class="sxs-lookup"><span data-stu-id="333dd-126">The type for an unknown endpoint identity.</span></span>                                                   |
| [<span data-ttu-id="333dd-127">**\_identidad del \_ extremo de UPN de WS \_**</span><span class="sxs-lookup"><span data-stu-id="333dd-127">**WS\_UPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | <span data-ttu-id="333dd-128">Tipo para especificar una identidad de extremo representada por un UPN (nombre principal de usuario).</span><span class="sxs-lookup"><span data-stu-id="333dd-128">The type for specifying an endpoint identity represented by a UPN (user principal name).</span></span>     |



 

 

 




