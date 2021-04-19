---
title: Autorización de identidad remota
description: El escenario de directiva IPsec de autorización de identidad remota requiere que las conexiones entrantes provienen de un conjunto específico de entidades de seguridad remotas que se especifican en una lista de control de acceso (ACL) del descriptor de seguridad de Windows (SD).
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57287a0dd9af4686b1a2dab162677912213559a7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314838"
---
# <a name="remote-identity-authorization"></a><span data-ttu-id="325c0-103">Autorización de identidad remota</span><span class="sxs-lookup"><span data-stu-id="325c0-103">Remote Identity Authorization</span></span>

<span data-ttu-id="325c0-104">El escenario de directiva IPsec de autorización de identidad remota requiere que las conexiones entrantes provienen de un conjunto específico de entidades de seguridad remotas que se especifican en una lista de control de acceso (ACL) del descriptor de seguridad de Windows (SD).</span><span class="sxs-lookup"><span data-stu-id="325c0-104">The Remote Identity Authorization IPsec policy scenario requires that inbound connections come from a specific set of remote security principals which are specified in a Windows security descriptor (SD) access control list (ACL).</span></span> <span data-ttu-id="325c0-105">Si la identidad remota (determinada por IPsec) no coincide con el conjunto de identidades permitidas, se quitará la conexión.</span><span class="sxs-lookup"><span data-stu-id="325c0-105">If the remote identity (as determined by IPsec) does not match the set of allowed identities, the connection will be dropped.</span></span> <span data-ttu-id="325c0-106">Esta Directiva debe especificarse junto con una de las opciones de directiva de modo de transporte.</span><span class="sxs-lookup"><span data-stu-id="325c0-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="325c0-107">Si se habilita AuthIP, se pueden especificar dos descriptores de seguridad, uno correspondiente al modo principal de AuthIP y el otro correspondiente al modo extendido de AuthIP.</span><span class="sxs-lookup"><span data-stu-id="325c0-107">If AuthIP is enabled, two security descriptors can be specified, one corresponding to AuthIP main mode, and the other corresponding to AuthIP extended mode.</span></span>

<span data-ttu-id="325c0-108">Un ejemplo de un posible escenario de modo de transporte de detección de negociación es "proteger todo el tráfico de datos de unidifusión, a excepción de ICMP, el uso del modo de transporte de IPsec, la habilitación de la detección de negociación y la restricción del acceso de entrada a identidades remotas permitidas según el descriptor de seguridad SD1 (que corresponde al modo principal de IKE/AuthIP) y el descriptor de seguridad SD2 (correspondiente al modo extendido de AuthIP), para todo el tráfico de unidifusión correspondiente 5555</span><span class="sxs-lookup"><span data-stu-id="325c0-108">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and restrict inbound access to remote identities allowed as per security descriptor SD1 (corresponding to IKE/AuthIP main mode) and security descriptor SD2 (corresponding to AuthIP extended mode), for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="325c0-109">Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.</span><span class="sxs-lookup"><span data-stu-id="325c0-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="325c0-110">**En la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6} Directiva de negociación del programa de instalación**</span><span class="sxs-lookup"><span data-stu-id="325c0-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="325c0-111">Agregue uno de los siguientes contextos de proveedor de directivas MM o ambos.</span><span class="sxs-lookup"><span data-stu-id="325c0-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="325c0-112">Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="325c0-112">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="325c0-113">Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="325c0-113">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="325c0-114">Se negociará un módulo de creación de claves común y se aplicará la Directiva MM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="325c0-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="325c0-115">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="325c0-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="325c0-116">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="325c0-117">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-117">Filter property</span></span>        | <span data-ttu-id="325c0-118">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="325c0-119">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="325c0-119">Filtering conditions</span></span>   | <span data-ttu-id="325c0-120">Vacía.</span><span class="sxs-lookup"><span data-stu-id="325c0-120">Empty.</span></span> <span data-ttu-id="325c0-121">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="325c0-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="325c0-122">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="325c0-122">**providerContextKey**</span></span> | <span data-ttu-id="325c0-123">GUID del contexto del proveedor MM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="325c0-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="325c0-124">**En la \_ capa de FWPM \_ IPSec \_ V {4 \| 6} configuración de la Directiva de negociación de QM y em**</span><span class="sxs-lookup"><span data-stu-id="325c0-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="325c0-125">Agregue uno o ambos de los siguientes contextos de proveedor de directivas del modo de transporte de QM y establezca la marca de directiva de IPSec como marca de [**\_ \_ \_ \_ seguridad segura**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="325c0-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="325c0-126">En el caso de IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE del Protocolo de \_ \_ transporte \_**.</span><span class="sxs-lookup"><span data-stu-id="325c0-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="325c0-127">Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ AuthIP del Protocolo de \_ transporte de QM \_ \_** que contiene la Directiva de negociación de modo extendido de AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="325c0-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT** that contains the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="325c0-128">Se negociará un módulo de creación de claves común y se aplicará la Directiva de QM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="325c0-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="325c0-129">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="325c0-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="325c0-130">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="325c0-131">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-131">Filter property</span></span>        | <span data-ttu-id="325c0-132">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="325c0-133">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="325c0-133">Filtering conditions</span></span>   | <span data-ttu-id="325c0-134">Vacía.</span><span class="sxs-lookup"><span data-stu-id="325c0-134">Empty.</span></span> <span data-ttu-id="325c0-135">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="325c0-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="325c0-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="325c0-136">**providerContextKey**</span></span> | <span data-ttu-id="325c0-137">GUID del contexto del proveedor de QM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="325c0-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="325c0-138">**En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquete de entrada**</span><span class="sxs-lookup"><span data-stu-id="325c0-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="325c0-139">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="325c0-140">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-140">Filter property</span></span>                                                   | <span data-ttu-id="325c0-141">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="325c0-142">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="325c0-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="325c0-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="325c0-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="325c0-144">**action.type**</span></span>                                                   | <span data-ttu-id="325c0-145">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="325c0-146">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="325c0-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="325c0-147">**Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="325c0-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="325c0-148">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="325c0-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="325c0-149">**contexto de FWPM de \_ \_ \_ seguridad de \_ conexión persistente de entrada IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="325c0-150">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="325c0-151">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-151">Filter property</span></span>                                                   | <span data-ttu-id="325c0-152">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="325c0-153">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="325c0-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="325c0-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="325c0-155">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="325c0-156">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="325c0-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="325c0-157">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="325c0-157">**action.type**</span></span>                                                   | <span data-ttu-id="325c0-158">\_permitir acción de FWP \_</span><span class="sxs-lookup"><span data-stu-id="325c0-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="325c0-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="325c0-159">**weight**</span></span>                                                        | [<span data-ttu-id="325c0-160">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="325c0-161">**En el nivel de FWPM de \_ \_ transporte de salida \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquetes salientes**</span><span class="sxs-lookup"><span data-stu-id="325c0-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="325c0-162">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-162">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="325c0-163">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-163">Filter property</span></span>                                                   | <span data-ttu-id="325c0-164">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="325c0-165">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="325c0-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="325c0-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="325c0-167">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="325c0-167">**action.type**</span></span>                                                   | <span data-ttu-id="325c0-168">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="325c0-169">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="325c0-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="325c0-170">**Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="325c0-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="325c0-171">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="325c0-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="325c0-172">**FWPM \_ contexto de la detección de \_ \_ negociación saliente de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="325c0-173">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="325c0-174">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-174">Filter property</span></span>                                                   | <span data-ttu-id="325c0-175">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-175">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="325c0-176">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="325c0-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="325c0-177">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="325c0-178">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="325c0-179">IPPROTO \_ ICMP {V6} estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="325c0-179">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="325c0-180">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="325c0-180">**action.type**</span></span>                                                   | <span data-ttu-id="325c0-181">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-181">**FWP\_ACTION\_PERMIT**</span></span>                                                |
    | <span data-ttu-id="325c0-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="325c0-182">**weight**</span></span>                                                        | <span data-ttu-id="325c0-183">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                               |

        

<span data-ttu-id="325c0-184">**En la capa de FWPM, la \_ \_ \_ \_ recepción de autenticación Ale \_ acepta \_ V {4 \| 6} configuración de reglas de filtrado por conexión de entrada**</span><span class="sxs-lookup"><span data-stu-id="325c0-184">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="325c0-185">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-185">Add a filter with the following properties.</span></span> <span data-ttu-id="325c0-186">Este filtro solo permitirá intentos de conexión entrantes si están protegidos por IPsec.</span><span class="sxs-lookup"><span data-stu-id="325c0-186">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="325c0-187">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-187">Filter property</span></span>                                                   | <span data-ttu-id="325c0-188">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-188">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="325c0-189">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-189">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="325c0-190">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="325c0-190">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="325c0-191">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="325c0-191">**action.type**</span></span>                                                   | <span data-ttu-id="325c0-192">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-192">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="325c0-193">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="325c0-193">**action.calloutKey**</span></span>                                             | <span data-ttu-id="325c0-194">**Llamada de FWPM de \_ \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="325c0-194">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="325c0-195">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-195">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="325c0-196">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-196">Filter property</span></span>                                                   | <span data-ttu-id="325c0-197">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-197">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="325c0-198">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-198">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="325c0-199">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="325c0-199">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="325c0-200">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-200">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="325c0-201">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="325c0-201">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="325c0-202">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="325c0-202">**action.type**</span></span>                                                   | <span data-ttu-id="325c0-203">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-203">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="325c0-204">**weight**</span><span class="sxs-lookup"><span data-stu-id="325c0-204">**weight**</span></span>                                                        | <span data-ttu-id="325c0-205">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-205">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="325c0-206">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-206">Add a filter with the following properties.</span></span> <span data-ttu-id="325c0-207">Este filtro permitirá las conexiones entrantes al puerto TCP 5555 si las identidades remotas correspondientes están permitidas por SD1 y SD2.</span><span class="sxs-lookup"><span data-stu-id="325c0-207">This filter will permit inbound connections to TCP port 5555 if the corresponding remote identities are allowed by both SD1 and SD2.</span></span> 

    | <span data-ttu-id="325c0-208">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-208">Filter property</span></span>                                                   | <span data-ttu-id="325c0-209">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-209">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="325c0-210">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-210">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="325c0-211">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="325c0-211">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="325c0-212">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-212">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="325c0-213">**IPPROTO \_ TCP** esta constante se define en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="325c0-213">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="325c0-214">**FWPM \_ Condición de filtrado de \_ \_ \_ puerto local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-214">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="325c0-215">5555</span><span class="sxs-lookup"><span data-stu-id="325c0-215">5555</span></span>                                                               |
    | <span data-ttu-id="325c0-216">**\_identificador de \_ \_ máquina remota \_ de Ale de condición FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-216">**FWPM\_CONDITION\_ALE\_REMOTE\_MACHINE\_ID**</span></span>                     | <span data-ttu-id="325c0-217">SD1</span><span class="sxs-lookup"><span data-stu-id="325c0-217">SD1</span></span>                                                                |
    | <span data-ttu-id="325c0-218">**\_ \_ \_ \_ ID. de usuario remoto \_ de la condición FWPM**</span><span class="sxs-lookup"><span data-stu-id="325c0-218">**FWPM\_CONDITION\_ALE\_REMOTE\_USER\_ID**</span></span>                        | <span data-ttu-id="325c0-219">SD2</span><span class="sxs-lookup"><span data-stu-id="325c0-219">SD2</span></span>                                                                |
    | <span data-ttu-id="325c0-220">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="325c0-220">**action.type**</span></span>                                                   | <span data-ttu-id="325c0-221">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-221">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                              |
    | <span data-ttu-id="325c0-222">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="325c0-222">**action.calloutKey**</span></span>                                             | <span data-ttu-id="325c0-223">**Llamada de FWPM de \_ \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="325c0-223">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>       |

        
4.  <span data-ttu-id="325c0-224">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="325c0-224">Add a filter with the following properties.</span></span> <span data-ttu-id="325c0-225">Este filtro bloqueará las demás conexiones entrantes al puerto TCP 5555 que no coinciden con el filtro anterior.</span><span class="sxs-lookup"><span data-stu-id="325c0-225">This filter will block any other inbound connections to TCP port 5555 that did not match the previous filter.</span></span> 

    | <span data-ttu-id="325c0-226">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="325c0-226">Filter property</span></span>                                                   | <span data-ttu-id="325c0-227">Value</span><span class="sxs-lookup"><span data-stu-id="325c0-227">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="325c0-228">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="325c0-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="325c0-229">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="325c0-230">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="325c0-231">**IPPROTO \_ TCP** esta constante se define en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="325c0-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="325c0-232">**FWPM \_ Condición de filtrado de \_ \_ \_ puerto local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="325c0-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="325c0-233">5555</span><span class="sxs-lookup"><span data-stu-id="325c0-233">5555</span></span>                                                               |
    | <span data-ttu-id="325c0-234">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="325c0-234">**action.type**</span></span>                                                   | <span data-ttu-id="325c0-235">**\_bloque de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-235">**FWP\_ACTION\_BLOCK**</span></span>                                             |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="325c0-236">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="325c0-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="325c0-237">Código de ejemplo: uso del modo de transporte</span><span class="sxs-lookup"><span data-stu-id="325c0-237">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="325c0-238">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="325c0-238">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="325c0-239">**Identificadores de llamada integrados**</span><span class="sxs-lookup"><span data-stu-id="325c0-239">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="325c0-240">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="325c0-240">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="325c0-241">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="325c0-241">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="325c0-242">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="325c0-242">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="325c0-243">**\_tipo de \_ contexto de proveedor de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="325c0-243">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

