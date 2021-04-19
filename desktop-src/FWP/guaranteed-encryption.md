---
title: Cifrado garantizado
description: El escenario de directiva IPsec de cifrado garantizado requiere cifrado IPsec para todo el tráfico coincidente. Esta Directiva debe especificarse junto con una de las opciones de directiva de modo de transporte.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbffa3d78a9e178850f3afaa4d6b7fa9831be875
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314648"
---
# <a name="guaranteed-encryption"></a><span data-ttu-id="59645-104">Cifrado garantizado</span><span class="sxs-lookup"><span data-stu-id="59645-104">Guaranteed Encryption</span></span>

<span data-ttu-id="59645-105">El escenario de directiva IPsec de cifrado garantizado requiere cifrado IPsec para todo el tráfico coincidente.</span><span class="sxs-lookup"><span data-stu-id="59645-105">The Guaranteed Encryption IPsec policy scenario requires IPsec encryption for all matching traffic.</span></span> <span data-ttu-id="59645-106">Esta Directiva debe especificarse junto con una de las opciones de directiva de modo de transporte.</span><span class="sxs-lookup"><span data-stu-id="59645-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="59645-107">El cifrado garantizado se usa normalmente para cifrar el tráfico confidencial en función de cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="59645-107">Guaranteed Encryption is typically used to encrypt sensitive traffic on a per application basis.</span></span>

<span data-ttu-id="59645-108">Un ejemplo de un posible escenario de cifrado garantizado es "proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte IPsec, habilitar la detección de negociación y requerir cifrado garantizado para todo el tráfico de unidifusión correspondiente al puerto local TCP 5555".</span><span class="sxs-lookup"><span data-stu-id="59645-108">An example of a possible Guaranteed Encryption scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and require guaranteed encryption for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="59645-109">Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.</span><span class="sxs-lookup"><span data-stu-id="59645-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="59645-110">**En la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6} Directiva de negociación del programa de instalación**</span><span class="sxs-lookup"><span data-stu-id="59645-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="59645-111">Agregue uno de los siguientes contextos de proveedor de directivas MM o ambos.</span><span class="sxs-lookup"><span data-stu-id="59645-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="59645-112">Para IKE, un contexto de proveedor de directivas de tipo FWPM \_ IPSec \_ IKE \_ mm \_ context.</span><span class="sxs-lookup"><span data-stu-id="59645-112">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="59645-113">Para AuthIP, un contexto de proveedor de directivas de tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ context.</span><span class="sxs-lookup"><span data-stu-id="59645-113">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="59645-114">Se negociará un módulo de creación de claves común y se aplicará la Directiva MM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="59645-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="59645-115">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="59645-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="59645-116">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="59645-117">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-117">Filter property</span></span>        | <span data-ttu-id="59645-118">Value</span><span class="sxs-lookup"><span data-stu-id="59645-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="59645-119">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="59645-119">Filtering conditions</span></span>   | <span data-ttu-id="59645-120">Vacía.</span><span class="sxs-lookup"><span data-stu-id="59645-120">Empty.</span></span> <span data-ttu-id="59645-121">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="59645-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="59645-122">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="59645-122">**providerContextKey**</span></span> | <span data-ttu-id="59645-123">GUID del contexto del proveedor MM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="59645-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="59645-124">**En la \_ capa de FWPM \_ IPSec \_ V {4 \| 6} configuración de la Directiva de negociación de QM y em**</span><span class="sxs-lookup"><span data-stu-id="59645-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="59645-125">Agregue uno o ambos de los siguientes contextos de proveedor de directivas del modo de transporte de QM y establezca la marca de directiva de IPSec como marca de [**\_ \_ \_ \_ seguridad segura**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="59645-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="59645-126">En el caso de IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE del Protocolo de \_ \_ transporte \_**.</span><span class="sxs-lookup"><span data-stu-id="59645-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="59645-127">Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec AuthIP en el \_ \_ \_ \_ contexto de transporte**.</span><span class="sxs-lookup"><span data-stu-id="59645-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="59645-128">Este contexto puede contener opcionalmente la Directiva de negociación de modo extendido de AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="59645-128">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="59645-129">Se negociará un módulo de creación de claves común y se aplicará la Directiva de QM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="59645-129">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="59645-130">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="59645-130">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="59645-131">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-131">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="59645-132">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-132">Filter property</span></span>        | <span data-ttu-id="59645-133">Value</span><span class="sxs-lookup"><span data-stu-id="59645-133">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="59645-134">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="59645-134">Filtering conditions</span></span>   | <span data-ttu-id="59645-135">Vacía.</span><span class="sxs-lookup"><span data-stu-id="59645-135">Empty.</span></span> <span data-ttu-id="59645-136">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="59645-136">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="59645-137">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="59645-137">**providerContextKey**</span></span> | <span data-ttu-id="59645-138">GUID del contexto del proveedor de QM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="59645-138">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="59645-139">**En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquete de entrada**</span><span class="sxs-lookup"><span data-stu-id="59645-139">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="59645-140">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-140">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="59645-141">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-141">Filter property</span></span>                                               | <span data-ttu-id="59645-142">Value</span><span class="sxs-lookup"><span data-stu-id="59645-142">Value</span></span>                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="59645-143">Condición de FWPM estado de \_ \_ filtrado de \_ tipo de dirección IP local \_ \_</span><span class="sxs-lookup"><span data-stu-id="59645-143">FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE filtering condition</span></span> | [<span data-ttu-id="59645-144">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="59645-144">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="59645-145">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="59645-145">**action.type**</span></span>                                               | <span data-ttu-id="59645-146">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="59645-146">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="59645-147">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="59645-147">**action.calloutKey**</span></span>                                         | <span data-ttu-id="59645-148">**Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="59645-148">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="59645-149">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="59645-149">**rawContext**</span></span>                                                | [<span data-ttu-id="59645-150">**contexto de FWPM de \_ \_ \_ seguridad de \_ conexión persistente de entrada IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="59645-150">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="59645-151">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-151">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="59645-152">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-152">Filter property</span></span>                                                   | <span data-ttu-id="59645-153">Value</span><span class="sxs-lookup"><span data-stu-id="59645-153">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="59645-154">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-154">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="59645-155">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="59645-155">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="59645-156">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-156">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="59645-157">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="59645-157">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="59645-158">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="59645-158">**action.type**</span></span>                                                   | <span data-ttu-id="59645-159">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="59645-159">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="59645-160">**weight**</span><span class="sxs-lookup"><span data-stu-id="59645-160">**weight**</span></span>                                                        | [<span data-ttu-id="59645-161">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="59645-161">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="59645-162">**En el nivel de FWPM de \_ \_ transporte de salida \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquetes salientes**</span><span class="sxs-lookup"><span data-stu-id="59645-162">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="59645-163">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-163">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="59645-164">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-164">Filter property</span></span>                                                   | <span data-ttu-id="59645-165">Value</span><span class="sxs-lookup"><span data-stu-id="59645-165">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="59645-166">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-166">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="59645-167">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="59645-167">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="59645-168">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="59645-168">**action.type**</span></span>                                                   | <span data-ttu-id="59645-169">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="59645-169">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="59645-170">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="59645-170">**action.calloutKey**</span></span>                                             | <span data-ttu-id="59645-171">**Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="59645-171">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="59645-172">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="59645-172">**rawContext**</span></span>                                                    | [<span data-ttu-id="59645-173">**FWPM \_ contexto de la detección de \_ \_ negociación saliente de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="59645-173">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="59645-174">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-174">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="59645-175">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-175">Filter property</span></span>                                                   | <span data-ttu-id="59645-176">Value</span><span class="sxs-lookup"><span data-stu-id="59645-176">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="59645-177">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-177">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="59645-178">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="59645-178">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="59645-179">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-179">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="59645-180">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="59645-180">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="59645-181">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="59645-181">**action.type**</span></span>                                                   | <span data-ttu-id="59645-182">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="59645-182">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="59645-183">**weight**</span><span class="sxs-lookup"><span data-stu-id="59645-183">**weight**</span></span>                                                        | <span data-ttu-id="59645-184">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="59645-184">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="59645-185">**En la capa de FWPM, la \_ \_ \_ \_ recepción de autenticación Ale \_ acepta \_ V {4 \| 6} configuración de reglas de filtrado por conexión de entrada**</span><span class="sxs-lookup"><span data-stu-id="59645-185">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="59645-186">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-186">Add a filter with the following properties.</span></span> <span data-ttu-id="59645-187">Este filtro solo permitirá intentos de conexión entrantes si están protegidos por IPsec.</span><span class="sxs-lookup"><span data-stu-id="59645-187">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="59645-188">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-188">Filter property</span></span>                                                   | <span data-ttu-id="59645-189">Value</span><span class="sxs-lookup"><span data-stu-id="59645-189">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="59645-190">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-190">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="59645-191">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="59645-191">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="59645-192">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="59645-192">**action.type**</span></span>                                                   | <span data-ttu-id="59645-193">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="59645-193">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="59645-194">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="59645-194">**action.calloutKey**</span></span>                                             | <span data-ttu-id="59645-195">**Llamada de FWPM de \_ \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="59645-195">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="59645-196">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-196">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="59645-197">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-197">Filter property</span></span>                                                   | <span data-ttu-id="59645-198">Value</span><span class="sxs-lookup"><span data-stu-id="59645-198">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="59645-199">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-199">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="59645-200">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="59645-200">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="59645-201">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-201">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="59645-202">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="59645-202">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="59645-203">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="59645-203">**action.type**</span></span>                                                   | <span data-ttu-id="59645-204">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="59645-204">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="59645-205">**weight**</span><span class="sxs-lookup"><span data-stu-id="59645-205">**weight**</span></span>                                                        | <span data-ttu-id="59645-206">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="59645-206">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="59645-207">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-207">Add a filter with the following properties.</span></span> <span data-ttu-id="59645-208">Este filtro solo permitirá conexiones entrantes al puerto TCP 5555 si están cifrados.</span><span class="sxs-lookup"><span data-stu-id="59645-208">This filter will only permit inbound connections to TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="59645-209">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-209">Filter property</span></span>                                                   | <span data-ttu-id="59645-210">Value</span><span class="sxs-lookup"><span data-stu-id="59645-210">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="59645-211">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-211">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="59645-212">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="59645-212">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="59645-213">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-213">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="59645-214">**IPPROTO \_ TCP** esta constante se define en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="59645-214">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="59645-215">**FWPM \_ Condición de filtrado de \_ \_ \_ puerto local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-215">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="59645-216">5555</span><span class="sxs-lookup"><span data-stu-id="59645-216">5555</span></span>                                                                                                  |
    | <span data-ttu-id="59645-217">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="59645-217">**action.type**</span></span>                                                   | <span data-ttu-id="59645-218">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="59645-218">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="59645-219">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="59645-219">**action.calloutKey**</span></span>                                             | <span data-ttu-id="59645-220">**Llamada de FWPM de \_ \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="59645-220">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>                                          |
    | <span data-ttu-id="59645-221">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="59645-221">**rawContext**</span></span>                                                    | [<span data-ttu-id="59645-222">**la \_ conexión del conjunto Ale de FWPM de contexto \_ \_ \_ \_ requiere \_ \_ cifrado IPSec**</span><span class="sxs-lookup"><span data-stu-id="59645-222">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

        

<span data-ttu-id="59645-223">**En la capa de FWPM, \_ \_ \_ conexión Ale \_ \_ V {4 \| 6} configuración de reglas de filtrado por conexión salientes**</span><span class="sxs-lookup"><span data-stu-id="59645-223">**At FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6} setup outbound per-connection filtering rules**</span></span>

-   <span data-ttu-id="59645-224">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="59645-224">Add a filter with the following properties.</span></span> <span data-ttu-id="59645-225">Este filtro solo permitirá las conexiones salientes desde el puerto TCP 5555 si están cifradas.</span><span class="sxs-lookup"><span data-stu-id="59645-225">This filter will only permit outbound connections from TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="59645-226">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="59645-226">Filter property</span></span>                                                   | <span data-ttu-id="59645-227">Value</span><span class="sxs-lookup"><span data-stu-id="59645-227">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="59645-228">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="59645-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="59645-229">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="59645-230">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="59645-231">**IPPROTO \_ TCP** esta constante se define en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="59645-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="59645-232">**FWPM \_ Condición de filtrado de \_ \_ \_ puerto local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="59645-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="59645-233">5555</span><span class="sxs-lookup"><span data-stu-id="59645-233">5555</span></span>                                                                                                  |
    | <span data-ttu-id="59645-234">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="59645-234">**action.type**</span></span>                                                   | <span data-ttu-id="59645-235">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="59645-235">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="59645-236">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="59645-236">**action.calloutKey**</span></span>                                             | <span data-ttu-id="59645-237">**Llamada FWPM de la \_ \_ \_ conexión Ale de IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="59645-237">**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V{4\|6}**</span></span>                                                       |
    | <span data-ttu-id="59645-238">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="59645-238">**rawContext**</span></span>                                                    | [<span data-ttu-id="59645-239">**la \_ conexión del conjunto Ale de FWPM de contexto \_ \_ \_ \_ requiere \_ \_ cifrado IPSec**</span><span class="sxs-lookup"><span data-stu-id="59645-239">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="59645-240">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59645-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59645-241">Código de ejemplo: uso del modo de transporte</span><span class="sxs-lookup"><span data-stu-id="59645-241">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="59645-242">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="59645-242">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="59645-243">**Identificadores de llamada integrados**</span><span class="sxs-lookup"><span data-stu-id="59645-243">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="59645-244">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="59645-244">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="59645-245">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="59645-245">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="59645-246">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="59645-246">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="59645-247">**\_tipo de \_ contexto de proveedor de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="59645-247">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

