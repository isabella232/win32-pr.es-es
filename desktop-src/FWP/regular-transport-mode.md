---
title: modo de transporte
description: El escenario de la directiva IPsec del modo de transporte requiere protección del modo de transporte IPsec para todo el tráfico coincidente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb927aff1b3f0e3c7fd13a192f0fcb18fc3ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420626"
---
# <a name="transport-mode"></a><span data-ttu-id="56b11-103">modo de transporte</span><span class="sxs-lookup"><span data-stu-id="56b11-103">Transport Mode</span></span>

<span data-ttu-id="56b11-104">El escenario de la directiva IPsec del modo de transporte requiere protección del modo de transporte IPsec para todo el tráfico coincidente.</span><span class="sxs-lookup"><span data-stu-id="56b11-104">The Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="56b11-105">Cualquier tráfico de texto no cifrado coincidente se quita hasta que la negociación IKE o AuthIP se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="56b11-105">Any matching clear text traffic is dropped until the IKE or AuthIP negotiation has completed successfully.</span></span> <span data-ttu-id="56b11-106">Si se produce un error en la negociación, la conectividad con la dirección IP correspondiente permanecerá rota.</span><span class="sxs-lookup"><span data-stu-id="56b11-106">If the negotiation fails, connectivity with the corresponding IP address will remain broken.</span></span>

<span data-ttu-id="56b11-107">Un ejemplo de posible escenario de modo de transporte es "proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte de IPsec".</span><span class="sxs-lookup"><span data-stu-id="56b11-107">An example of a possible Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode."</span></span>

<span data-ttu-id="56b11-108">Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.</span><span class="sxs-lookup"><span data-stu-id="56b11-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="56b11-109">**En la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6} Directiva de negociación del programa de instalación**</span><span class="sxs-lookup"><span data-stu-id="56b11-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="56b11-110">Agregue uno de los siguientes contextos de proveedor de directivas MM o ambos.</span><span class="sxs-lookup"><span data-stu-id="56b11-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="56b11-111">Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="56b11-111">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="56b11-112">Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="56b11-112">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="56b11-113">Se negociará un módulo de creación de claves común y se aplicará la Directiva MM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="56b11-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="56b11-114">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="56b11-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="56b11-115">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="56b11-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="56b11-116">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="56b11-116">Filter property</span></span>        | <span data-ttu-id="56b11-117">Value</span><span class="sxs-lookup"><span data-stu-id="56b11-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="56b11-118">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="56b11-118">Filtering conditions</span></span>   | <span data-ttu-id="56b11-119">Vacía.</span><span class="sxs-lookup"><span data-stu-id="56b11-119">Empty.</span></span> <span data-ttu-id="56b11-120">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="56b11-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="56b11-121">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="56b11-121">**providerContextKey**</span></span> | <span data-ttu-id="56b11-122">GUID del contexto del proveedor MM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="56b11-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="56b11-123">**En la \_ capa de FWPM \_ IPSec \_ V {4 \| 6} configuración de la Directiva de negociación de QM y em**</span><span class="sxs-lookup"><span data-stu-id="56b11-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="56b11-124">Agregue uno o ambos de los siguientes contextos de proveedor de directivas de modo de transporte de QM.</span><span class="sxs-lookup"><span data-stu-id="56b11-124">Add one or both of the following QM transport mode policy provider contexts.</span></span>  
    -   <span data-ttu-id="56b11-125">En el caso de IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE del Protocolo de \_ \_ transporte \_**.</span><span class="sxs-lookup"><span data-stu-id="56b11-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="56b11-126">Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec AuthIP en el \_ \_ \_ \_ contexto de transporte**.</span><span class="sxs-lookup"><span data-stu-id="56b11-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="56b11-127">Este contexto puede contener opcionalmente la Directiva de negociación de modo extendido de AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="56b11-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="56b11-128">Se negociará un módulo de creación de claves común y se aplicará la Directiva de QM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="56b11-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="56b11-129">AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.</span><span class="sxs-lookup"><span data-stu-id="56b11-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="56b11-130">Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="56b11-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="56b11-131">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="56b11-131">Filter property</span></span>        | <span data-ttu-id="56b11-132">Value</span><span class="sxs-lookup"><span data-stu-id="56b11-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="56b11-133">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="56b11-133">Filtering conditions</span></span>   | <span data-ttu-id="56b11-134">Vacía.</span><span class="sxs-lookup"><span data-stu-id="56b11-134">Empty.</span></span> <span data-ttu-id="56b11-135">Todo el tráfico coincidirá con el filtro.</span><span class="sxs-lookup"><span data-stu-id="56b11-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="56b11-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="56b11-136">**providerContextKey**</span></span> | <span data-ttu-id="56b11-137">GUID del contexto del proveedor de QM agregado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="56b11-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="56b11-138">**En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquete de entrada**</span><span class="sxs-lookup"><span data-stu-id="56b11-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="56b11-139">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="56b11-139">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="56b11-140">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="56b11-140">Filter property</span></span>                                                   | <span data-ttu-id="56b11-141">Value</span><span class="sxs-lookup"><span data-stu-id="56b11-141">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="56b11-142">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="56b11-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="56b11-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="56b11-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="56b11-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="56b11-144">**action.type**</span></span>                                                   | <span data-ttu-id="56b11-145">\_ \_ terminando llamada de acción de FWP \_</span><span class="sxs-lookup"><span data-stu-id="56b11-145">FWP\_ACTION\_CALLOUT\_TERMINATING</span></span>                             |
    | <span data-ttu-id="56b11-146">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="56b11-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="56b11-147">Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="56b11-147">FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>             |

        
2.  <span data-ttu-id="56b11-148">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="56b11-148">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="56b11-149">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="56b11-149">Filter property</span></span>                                                  | <span data-ttu-id="56b11-150">Value</span><span class="sxs-lookup"><span data-stu-id="56b11-150">Value</span></span>                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | <span data-ttu-id="56b11-151">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="56b11-151">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="56b11-152">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="56b11-152">NlatUnicast</span></span>                                                               |
    | <span data-ttu-id="56b11-153">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="56b11-153">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>            | <span data-ttu-id="56b11-154">IPPROTO \_ ICMP {V6} estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="56b11-154">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/>    |
    | <span data-ttu-id="56b11-155">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="56b11-155">**action.type**</span></span>                                                  | <span data-ttu-id="56b11-156">\_permitir acción de FWP \_</span><span class="sxs-lookup"><span data-stu-id="56b11-156">FWP\_ACTION\_PERMIT</span></span>                                                       |
    | <span data-ttu-id="56b11-157">**weight**</span><span class="sxs-lookup"><span data-stu-id="56b11-157">**weight**</span></span>                                                       | [<span data-ttu-id="56b11-158">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="56b11-158">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md) |

        

<span data-ttu-id="56b11-159">**En el nivel de FWPM de \_ \_ transporte de salida \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquetes salientes**</span><span class="sxs-lookup"><span data-stu-id="56b11-159">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="56b11-160">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="56b11-160">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="56b11-161">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="56b11-161">Filter property</span></span>                                                   | <span data-ttu-id="56b11-162">Value</span><span class="sxs-lookup"><span data-stu-id="56b11-162">Value</span></span>                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | <span data-ttu-id="56b11-163">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="56b11-163">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="56b11-164">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="56b11-164">NlatUnicast</span></span>                                        |
    | <span data-ttu-id="56b11-165">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="56b11-165">**action.type**</span></span>                                                   | <span data-ttu-id="56b11-166">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="56b11-166">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>              |
    | <span data-ttu-id="56b11-167">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="56b11-167">**action.calloutKey**</span></span>                                             | <span data-ttu-id="56b11-168">Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="56b11-168">FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span> |

        
2.  <span data-ttu-id="56b11-169">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="56b11-169">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="56b11-170">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="56b11-170">Filter property</span></span>                                                   | <span data-ttu-id="56b11-171">Value</span><span class="sxs-lookup"><span data-stu-id="56b11-171">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="56b11-172">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="56b11-172">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="56b11-173">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="56b11-173">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="56b11-174">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="56b11-174">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="56b11-175">IPPROTO \_ ICMP {V6} estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="56b11-175">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="56b11-176">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="56b11-176">**action.type**</span></span>                                                   | <span data-ttu-id="56b11-177">\_permitir acción de FWP \_</span><span class="sxs-lookup"><span data-stu-id="56b11-177">FWP\_ACTION\_PERMIT</span></span>                                                    |
    | <span data-ttu-id="56b11-178">**weight**</span><span class="sxs-lookup"><span data-stu-id="56b11-178">**weight**</span></span>                                                        | <span data-ttu-id="56b11-179">\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_</span><span class="sxs-lookup"><span data-stu-id="56b11-179">FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="56b11-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56b11-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b11-181">Código de ejemplo: uso del modo de transporte</span><span class="sxs-lookup"><span data-stu-id="56b11-181">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="56b11-182">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="56b11-182">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="56b11-183">**Tipos de contexto de proveedor**</span><span class="sxs-lookup"><span data-stu-id="56b11-183">**Provider Context Types**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[<span data-ttu-id="56b11-184">Condiciones de filtrado</span><span class="sxs-lookup"><span data-stu-id="56b11-184">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="56b11-185">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="56b11-185">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="56b11-186">**Identificadores de llamada integrados**</span><span class="sxs-lookup"><span data-stu-id="56b11-186">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> </dl>

 

