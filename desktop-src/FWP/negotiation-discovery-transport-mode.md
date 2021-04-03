---
title: Modo de transporte de detección de negociación
description: El escenario de directiva IPsec del modo de transporte de detección de negociación requiere la protección del modo de transporte IPsec para todo el tráfico entrante coincidente y solicita protección de IPsec para que coincida con el tráfico saliente.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9477d18f2fe478f5c885c071f47d0bf2baaad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904521"
---
# <a name="negotiation-discovery-transport-mode"></a><span data-ttu-id="790de-103">Modo de transporte de detección de negociación</span><span class="sxs-lookup"><span data-stu-id="790de-103">Negotiation Discovery Transport Mode</span></span>

<span data-ttu-id="790de-104">El escenario de directiva IPsec del modo de transporte de detección de negociación requiere la protección del modo de transporte IPsec para todo el tráfico entrante coincidente y solicita protección de IPsec para que coincida con el tráfico saliente.</span><span class="sxs-lookup"><span data-stu-id="790de-104">The Negotiation Discovery Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching inbound traffic, and requests IPsec protection for matching outbound traffic.</span></span> <span data-ttu-id="790de-105">Por lo tanto, las conexiones salientes pueden retroceder a texto sin cifrar, mientras que las conexiones entrantes no.</span><span class="sxs-lookup"><span data-stu-id="790de-105">Therefore, outbound connections are allowed to fallback to clear-text while inbound connections are not.</span></span>

<span data-ttu-id="790de-106">Con esta Directiva, cuando el equipo host intenta una nueva conexión saliente y no hay ninguna SA IPsec existente que coincida con el tráfico, el host envía simultáneamente los paquetes en texto sin cifrar e inicia una negociación IKE o AuthIP.</span><span class="sxs-lookup"><span data-stu-id="790de-106">With this policy, when the host machine attempts a new outbound connection and there is no existing IPsec SA matching the traffic, the host simultaneously sends the packets in clear-text and starts an IKE or AuthIP negotiation.</span></span> <span data-ttu-id="790de-107">Si la negociación se realiza correctamente, la conexión se actualiza a protegido por IPsec.</span><span class="sxs-lookup"><span data-stu-id="790de-107">If the negotiation succeeds, the connection is upgraded to IPsec-protected.</span></span> <span data-ttu-id="790de-108">De lo contrario, la conexión permanece en texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="790de-108">Otherwise, the connection stays in clear-text.</span></span> <span data-ttu-id="790de-109">Una vez protegida por IPsec, una conexión nunca se puede degradar a texto sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="790de-109">Once IPsec-protected, a connection can never be downgraded to clear-text.</span></span>

<span data-ttu-id="790de-110">El modo de transporte de detección de negociación se usa normalmente en entornos que incluyen máquinas compatibles con IPsec y no compatibles con IPsec.</span><span class="sxs-lookup"><span data-stu-id="790de-110">Negotiation Discovery Transport Mode is typically used in environments that include both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="790de-111">Un ejemplo de un posible escenario de modo de transporte de detección de negociación es "proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte IPsec y habilitar la detección de negociaciones".</span><span class="sxs-lookup"><span data-stu-id="790de-111">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, and enable negotiation discovery."</span></span>

<span data-ttu-id="790de-112">Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.</span><span class="sxs-lookup"><span data-stu-id="790de-112">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="790de-113">**En la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6} configuración de la Directiva de negociación mm**</span><span class="sxs-lookup"><span data-stu-id="790de-113">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} set up MM negotiation policy**</span></span>  

1.  <span data-ttu-id="790de-114">Agregue uno de los siguientes contextos de proveedor de directivas MM o ambos.</span><span class="sxs-lookup"><span data-stu-id="790de-114">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="790de-115">Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="790de-115">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="790de-116">Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="790de-116">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="790de-117">Se negociará un módulo de creación de claves común y se aplicará la Directiva MM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="790de-117">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="790de-118">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="790de-118">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="790de-119">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="790de-119">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="790de-120">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="790de-120">Filter property</span></span>        | <span data-ttu-id="790de-121">Value</span><span class="sxs-lookup"><span data-stu-id="790de-121">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="790de-122">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="790de-122">Filtering conditions</span></span>   | <span data-ttu-id="790de-123">Vacía.</span><span class="sxs-lookup"><span data-stu-id="790de-123">Empty.</span></span> <span data-ttu-id="790de-124">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="790de-124">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="790de-125">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="790de-125">**providerContextKey**</span></span> | <span data-ttu-id="790de-126">GUID del contexto del proveedor MM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="790de-126">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="790de-127">**En el \_ nivel de FWPM \_ IPSec \_ V {4 \| 6} configuración de la Directiva de negociación de QM y em**</span><span class="sxs-lookup"><span data-stu-id="790de-127">**At FWPM\_LAYER\_IPSEC\_V{4\|6} set up QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="790de-128">Agregue uno o ambos de los siguientes contextos de proveedor de directivas del modo de transporte de QM y establezca la marca de directiva de IPSec como marca de [**\_ \_ \_ \_ seguridad segura**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="790de-128">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="790de-129">En el caso de IKE, un contexto de proveedor de directivas de tipo FWPM \_ IPSec \_ IKE del Protocolo de \_ \_ transporte \_ .</span><span class="sxs-lookup"><span data-stu-id="790de-129">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT.</span></span>
    -   <span data-ttu-id="790de-130">Para AuthIP, un contexto de proveedor de directivas de tipo FWPM \_ IPSec AuthIP en el \_ contexto de \_ \_ transporte \_ .</span><span class="sxs-lookup"><span data-stu-id="790de-130">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT.</span></span> <span data-ttu-id="790de-131">Este contexto puede contener opcionalmente la Directiva de negociación de modo extendido de AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="790de-131">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="790de-132">Se negociará un módulo de creación de claves común y se aplicará la Directiva de QM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="790de-132">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="790de-133">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="790de-133">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="790de-134">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="790de-134">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="790de-135">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="790de-135">Filter property</span></span>        | <span data-ttu-id="790de-136">Value</span><span class="sxs-lookup"><span data-stu-id="790de-136">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="790de-137">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="790de-137">Filtering conditions</span></span>   | <span data-ttu-id="790de-138">Vacía.</span><span class="sxs-lookup"><span data-stu-id="790de-138">Empty.</span></span> <span data-ttu-id="790de-139">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="790de-139">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="790de-140">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="790de-140">**providerContextKey**</span></span> | <span data-ttu-id="790de-141">GUID del contexto del proveedor de QM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="790de-141">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="790de-142">**En el \_ transporte de entrada de capa FWPM \_ \_ \_ V {4 \| 6} configurar reglas de filtrado por paquetes entrantes**</span><span class="sxs-lookup"><span data-stu-id="790de-142">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} set up inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="790de-143">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="790de-143">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="790de-144">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="790de-144">Filter property</span></span>                                                   | <span data-ttu-id="790de-145">Value</span><span class="sxs-lookup"><span data-stu-id="790de-145">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="790de-146">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-146">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="790de-147">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="790de-147">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="790de-148">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="790de-148">**action.type**</span></span>                                                   | <span data-ttu-id="790de-149">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="790de-149">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="790de-150">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="790de-150">**action.calloutKey**</span></span>                                             | <span data-ttu-id="790de-151">**Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="790de-151">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="790de-152">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="790de-152">**rawContext**</span></span>                                                    | [<span data-ttu-id="790de-153">**contexto de FWPM de \_ \_ \_ seguridad de \_ conexión persistente de entrada IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="790de-153">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="790de-154">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="790de-154">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="790de-155">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="790de-155">Filter property</span></span>                                                   | <span data-ttu-id="790de-156">Value</span><span class="sxs-lookup"><span data-stu-id="790de-156">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="790de-157">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-157">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="790de-158">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="790de-158">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="790de-159">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-159">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="790de-160">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="790de-160">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="790de-161">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="790de-161">**action.type**</span></span>                                                   | <span data-ttu-id="790de-162">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="790de-162">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="790de-163">**weight**</span><span class="sxs-lookup"><span data-stu-id="790de-163">**weight**</span></span>                                                        | [<span data-ttu-id="790de-164">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="790de-164">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="790de-165">**En \_ el transporte de salida de nivel FWPM \_ \_ \_ V {4 \| 6} configurar reglas de filtrado por paquete de salida**</span><span class="sxs-lookup"><span data-stu-id="790de-165">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} set up outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="790de-166">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="790de-166">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="790de-167">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="790de-167">Filter property</span></span>                                                   | <span data-ttu-id="790de-168">Value</span><span class="sxs-lookup"><span data-stu-id="790de-168">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="790de-169">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-169">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="790de-170">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="790de-170">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="790de-171">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="790de-171">**action.type**</span></span>                                                   | <span data-ttu-id="790de-172">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="790de-172">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="790de-173">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="790de-173">**action.calloutKey**</span></span>                                             | <span data-ttu-id="790de-174">**Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="790de-174">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="790de-175">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="790de-175">**rawContext**</span></span>                                                    | [<span data-ttu-id="790de-176">**FWPM \_ contexto de la detección de \_ \_ negociación saliente de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="790de-176">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="790de-177">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="790de-177">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="790de-178">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="790de-178">Filter property</span></span>                                                   | <span data-ttu-id="790de-179">Value</span><span class="sxs-lookup"><span data-stu-id="790de-179">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="790de-180">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-180">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="790de-181">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="790de-181">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="790de-182">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-182">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="790de-183">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="790de-183">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="790de-184">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="790de-184">**action.type**</span></span>                                                   | <span data-ttu-id="790de-185">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="790de-185">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="790de-186">**weight**</span><span class="sxs-lookup"><span data-stu-id="790de-186">**weight**</span></span>                                                        | <span data-ttu-id="790de-187">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="790de-187">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="790de-188">**En el nivel FWPM, se ha \_ \_ \_ \_ aceptado la recepción de autenticación Ale de \_ \_ \| la capa**</span><span class="sxs-lookup"><span data-stu-id="790de-188">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} set up inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="790de-189">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="790de-189">Add a filter with the following properties.</span></span> <span data-ttu-id="790de-190">Este filtro solo permitirá intentos de conexión entrantes si están protegidos por IPsec.</span><span class="sxs-lookup"><span data-stu-id="790de-190">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 
    | <span data-ttu-id="790de-191">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="790de-191">Filter property</span></span>                                                   | <span data-ttu-id="790de-192">Value</span><span class="sxs-lookup"><span data-stu-id="790de-192">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="790de-193">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-193">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="790de-194">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="790de-194">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="790de-195">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="790de-195">**action.type**</span></span>                                                   | <span data-ttu-id="790de-196">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="790de-196">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="790de-197">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="790de-197">**action.calloutKey**</span></span>                                             | <span data-ttu-id="790de-198">**Llamada de FWPM de \_ \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="790de-198">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="790de-199">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="790de-199">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="790de-200">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="790de-200">Filter property</span></span>                                                   | <span data-ttu-id="790de-201">Value</span><span class="sxs-lookup"><span data-stu-id="790de-201">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="790de-202">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-202">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="790de-203">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="790de-203">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="790de-204">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="790de-204">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="790de-205">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="790de-205">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="790de-206">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="790de-206">**action.type**</span></span>                                                   | <span data-ttu-id="790de-207">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="790de-207">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="790de-208">**weight**</span><span class="sxs-lookup"><span data-stu-id="790de-208">**weight**</span></span>                                                        | <span data-ttu-id="790de-209">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="790de-209">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="790de-210">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="790de-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="790de-211">Código de ejemplo: uso del modo de transporte</span><span class="sxs-lookup"><span data-stu-id="790de-211">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="790de-212">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="790de-212">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="790de-213">**Identificadores de llamada integrados**</span><span class="sxs-lookup"><span data-stu-id="790de-213">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="790de-214">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="790de-214">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="790de-215">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="790de-215">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="790de-216">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="790de-216">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="790de-217">**\_tipo de \_ contexto de proveedor de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="790de-217">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

