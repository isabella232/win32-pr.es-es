---
title: Modo de transporte de detección de negociación en modo de límite
description: El escenario de transporte de detección de negociación en modo de límite Directiva de IPsec solicita la protección del modo de transporte de IPsec para todo el tráfico coincidente.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9869be61923bff1c392c5abe2bd98099a0c3c89f
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314598"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a><span data-ttu-id="d89a4-103">Modo de transporte de detección de negociación en modo de límite</span><span class="sxs-lookup"><span data-stu-id="d89a4-103">Negotiation Discovery Transport Mode in Boundary Mode</span></span>

<span data-ttu-id="d89a4-104">El escenario de transporte de detección de negociación en modo de límite Directiva de IPsec solicita la protección del modo de transporte de IPsec para todo el tráfico coincidente.</span><span class="sxs-lookup"><span data-stu-id="d89a4-104">The Negotiation Discovery Transport Mode in Boundary Mode IPsec policy scenario requests IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="d89a4-105">Si se produce un error en la negociación de IKE/AuthIP, se permite que las conexiones entrantes y salientes se reproduzcan en texto sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="d89a4-105">If the IKE/AuthIP negotiation fails, both inbound and outbound connections are allowed to fallback to clear-text .</span></span>

<span data-ttu-id="d89a4-106">Esta directiva IPsec se usa normalmente en equipos a los que se tiene acceso mediante máquinas con capacidad IPsec y no compatibles con IPsec.</span><span class="sxs-lookup"><span data-stu-id="d89a4-106">This IPsec policy is typically used on machines that are accessed by both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="d89a4-107">Un ejemplo de un posible escenario de modo de transporte de detección de negociación es "proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte de IPsec y habilitar la detección de negociación en el modo límite".</span><span class="sxs-lookup"><span data-stu-id="d89a4-107">An example of a potential Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode and enable negotiation discovery in boundary mode."</span></span>

<span data-ttu-id="d89a4-108">Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.</span><span class="sxs-lookup"><span data-stu-id="d89a4-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="d89a4-109">**En la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6} Directiva de negociación del programa de instalación**</span><span class="sxs-lookup"><span data-stu-id="d89a4-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="d89a4-110">Agregue uno de los siguientes contextos de proveedor de directivas MM o ambos.</span><span class="sxs-lookup"><span data-stu-id="d89a4-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="d89a4-111">Para IKE, un contexto de proveedor de directivas de tipo FWPM \_ IPSec \_ IKE \_ mm \_ context.</span><span class="sxs-lookup"><span data-stu-id="d89a4-111">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="d89a4-112">Para AuthIP, un contexto de proveedor de directivas de tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ context.</span><span class="sxs-lookup"><span data-stu-id="d89a4-112">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="d89a4-113">Se negociará un módulo de creación de claves común y se aplicará la Directiva MM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d89a4-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="d89a4-114">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="d89a4-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="d89a4-115">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d89a4-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="d89a4-116">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="d89a4-116">Filter property</span></span>        | <span data-ttu-id="d89a4-117">Value</span><span class="sxs-lookup"><span data-stu-id="d89a4-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="d89a4-118">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="d89a4-118">Filtering conditions</span></span>   | <span data-ttu-id="d89a4-119">Vacía.</span><span class="sxs-lookup"><span data-stu-id="d89a4-119">Empty.</span></span> <span data-ttu-id="d89a4-120">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="d89a4-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="d89a4-121">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="d89a4-121">**providerContextKey**</span></span> | <span data-ttu-id="d89a4-122">GUID del contexto del proveedor MM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="d89a4-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="d89a4-123">**En la \_ capa de FWPM \_ IPSec \_ V {4 \| 6} configuración de la Directiva de negociación de QM y em**</span><span class="sxs-lookup"><span data-stu-id="d89a4-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="d89a4-124">Agregue uno o ambos de los siguientes contextos de proveedor de directivas del modo de transporte de QM y establezca la marca de límite de la [**\_ marca de directiva \_ \_ \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="d89a4-124">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_BOUNDARY**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="d89a4-125">En el caso de IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE del Protocolo de \_ \_ transporte \_**.</span><span class="sxs-lookup"><span data-stu-id="d89a4-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="d89a4-126">Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec AuthIP en el \_ \_ \_ \_ contexto de transporte**.</span><span class="sxs-lookup"><span data-stu-id="d89a4-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="d89a4-127">Este contexto puede contener opcionalmente la Directiva de negociación de modo extendido de AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="d89a4-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="d89a4-128">Se negociará un módulo de creación de claves común y se aplicará la Directiva de QM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d89a4-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="d89a4-129">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="d89a4-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="d89a4-130">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d89a4-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="d89a4-131">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="d89a4-131">Filter property</span></span>        | <span data-ttu-id="d89a4-132">Value</span><span class="sxs-lookup"><span data-stu-id="d89a4-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="d89a4-133">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="d89a4-133">Filtering conditions</span></span>   | <span data-ttu-id="d89a4-134">Vacía.</span><span class="sxs-lookup"><span data-stu-id="d89a4-134">Empty.</span></span> <span data-ttu-id="d89a4-135">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="d89a4-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="d89a4-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="d89a4-136">**providerContextKey**</span></span> | <span data-ttu-id="d89a4-137">GUID del contexto del proveedor de QM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="d89a4-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="d89a4-138">**En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquete de entrada**</span><span class="sxs-lookup"><span data-stu-id="d89a4-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="d89a4-139">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d89a4-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="d89a4-140">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="d89a4-140">Filter property</span></span>                                                   | <span data-ttu-id="d89a4-141">Value</span><span class="sxs-lookup"><span data-stu-id="d89a4-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d89a4-142">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="d89a4-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="d89a4-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="d89a4-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="d89a4-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="d89a4-144">**action.type**</span></span>                                                   | <span data-ttu-id="d89a4-145">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="d89a4-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="d89a4-146">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="d89a4-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="d89a4-147">**Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="d89a4-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="d89a4-148">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="d89a4-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="d89a4-149">**contexto de FWPM de \_ \_ \_ seguridad de \_ conexión persistente de entrada IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d89a4-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="d89a4-150">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d89a4-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="d89a4-151">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="d89a4-151">Filter property</span></span>                                                   | <span data-ttu-id="d89a4-152">Value</span><span class="sxs-lookup"><span data-stu-id="d89a4-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="d89a4-153">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="d89a4-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="d89a4-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="d89a4-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="d89a4-155">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="d89a4-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="d89a4-156">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="d89a4-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="d89a4-157">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="d89a4-157">**action.type**</span></span>                                                   | <span data-ttu-id="d89a4-158">\_permitir acción de FWP \_</span><span class="sxs-lookup"><span data-stu-id="d89a4-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="d89a4-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="d89a4-159">**weight**</span></span>                                                        | [<span data-ttu-id="d89a4-160">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="d89a4-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="d89a4-161">**En el nivel de FWPM de \_ \_ transporte de salida \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquetes salientes**</span><span class="sxs-lookup"><span data-stu-id="d89a4-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="d89a4-162">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d89a4-162">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="d89a4-163">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="d89a4-163">Filter property</span></span>                                                   | <span data-ttu-id="d89a4-164">Value</span><span class="sxs-lookup"><span data-stu-id="d89a4-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d89a4-165">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="d89a4-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="d89a4-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="d89a4-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="d89a4-167">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="d89a4-167">**action.type**</span></span>                                                   | <span data-ttu-id="d89a4-168">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="d89a4-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="d89a4-169">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="d89a4-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="d89a4-170">**Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="d89a4-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="d89a4-171">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="d89a4-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="d89a4-172">**FWPM \_ contexto de la detección de \_ \_ negociación saliente de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d89a4-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="d89a4-173">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d89a4-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="d89a4-174">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="d89a4-174">Filter property</span></span>                                                   | <span data-ttu-id="d89a4-175">Value</span><span class="sxs-lookup"><span data-stu-id="d89a4-175">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="d89a4-176">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="d89a4-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="d89a4-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="d89a4-177">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="d89a4-178">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="d89a4-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="d89a4-179">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="d89a4-179">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="d89a4-180">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="d89a4-180">**action.type**</span></span>                                                   | <span data-ttu-id="d89a4-181">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="d89a4-181">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="d89a4-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="d89a4-182">**weight**</span></span>                                                        | <span data-ttu-id="d89a4-183">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="d89a4-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

> [!Note]  
> <span data-ttu-id="d89a4-184">En lugar del modo de transporte de detección de negociación, para el modo de transporte de detección de negociación en la Directiva de modo límite, no es necesario agregar un filtro en las capas de FWPM de autenticación Ale de la capa de la **\_ recepción de \_ \_ \_ \_ aceptación \_ V {4 \| 6}** porque esta directiva permite conexiones entrantes sin protección de texto no protegido.</span><span class="sxs-lookup"><span data-stu-id="d89a4-184">As opposed to Negotiation Discovery Transport Mode, for Negotiation Discovery Transport Mode in Boundary Mode policy there is no need to add a filter at the **FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}** layers because this policy allows inbound unprotected clear-text connections.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d89a4-185">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d89a4-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d89a4-186">Código de ejemplo: uso del modo de transporte</span><span class="sxs-lookup"><span data-stu-id="d89a4-186">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="d89a4-187">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="d89a4-187">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="d89a4-188">**Identificadores de llamada integrados**</span><span class="sxs-lookup"><span data-stu-id="d89a4-188">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="d89a4-189">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="d89a4-189">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="d89a4-190">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="d89a4-190">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="d89a4-191">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="d89a4-191">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="d89a4-192">**\_tipo de \_ contexto de proveedor de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="d89a4-192">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

