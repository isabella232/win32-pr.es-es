---
title: Marcas de condición de filtrado (Fwptypes. h)
description: Las marcas de condición de filtrado de la plataforma de filtrado de Windows (WFP) están representadas por un campo de bits.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803512"
---
# <a name="filtering-condition-flags"></a><span data-ttu-id="cedf9-103">Marcas de condición de filtrado</span><span class="sxs-lookup"><span data-stu-id="cedf9-103">Filtering Condition Flags</span></span>

<span data-ttu-id="cedf9-104">Las marcas de condición de filtrado de la plataforma de filtrado de Windows (WFP) están representadas por un campo de bits.</span><span class="sxs-lookup"><span data-stu-id="cedf9-104">The Windows Filtering Platform (WFP) filtering condition flags are each represented by a bitfield.</span></span>

<span data-ttu-id="cedf9-105">Estas marcas y las capas de filtrado donde se pueden usar se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="cedf9-105">These flags and the filtering layers where they can be used are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="cedf9-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**la \_ marca de condición de FWP \_ es de \_ \_ bucle invertido**</span><span class="sxs-lookup"><span data-stu-id="cedf9-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-107">Comprueba si el tráfico de red es un tráfico de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="cedf9-107">Tests if the network traffic is loopback traffic.</span></span>

<span data-ttu-id="cedf9-108">Filtrar capas:</span><span class="sxs-lookup"><span data-stu-id="cedf9-108">Filtering layers:</span></span>

-   <span data-ttu-id="cedf9-109">FWPM \_ de \_ entrada \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-109">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-110">FWPM de \_ salida de nivel de \_ \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-110">FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-111">\_Transporte de entrada de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-111">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-112">\_Transporte de salida de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-112">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-113">Flujo de capa de FWPM \_ \_ \_ {V4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-113">FWPM\_LAYER\_STREAM\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="cedf9-114">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-114">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="cedf9-115">\_Error ICMP entrante de la capa FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-115">FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="cedf9-116">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-116">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="cedf9-117">\_Error de \_ ICMP saliente de nivel FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-117">FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="cedf9-118">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-118">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="cedf9-119">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-119">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-120">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-120">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="cedf9-121">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-121">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="cedf9-122">\_Flujo ALE de capa de FWPM \_ establecido en \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-122">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="cedf9-123">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-123">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**la \_ marca de condición de FWP \_ \_ está \_ protegida por IPsec \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_SECURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-125">Comprueba si el tráfico de red está protegido por IPsec.</span><span class="sxs-lookup"><span data-stu-id="cedf9-125">Tests if the network traffic is protected by IPsec.</span></span>

<span data-ttu-id="cedf9-126">Filtrar capas:</span><span class="sxs-lookup"><span data-stu-id="cedf9-126">Filtering layers:</span></span>

-   <span data-ttu-id="cedf9-127">FWPM \_ de \_ entrada \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-127">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-128">\_Transporte de entrada de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-128">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-129">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-129">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-130">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-130">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**la \_ marca de condición de FWP \_ \_ se ha \_ reautorizado**</span><span class="sxs-lookup"><span data-stu-id="cedf9-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-132">Comprueba un cambio de directiva en lugar de una nueva conexión.</span><span class="sxs-lookup"><span data-stu-id="cedf9-132">Tests for a policy change as opposed to a new connection.</span></span>

<span data-ttu-id="cedf9-133">Filtrar capas:</span><span class="sxs-lookup"><span data-stu-id="cedf9-133">Filtering layers:</span></span>

-   <span data-ttu-id="cedf9-134">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-134">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-135">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-135">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**la \_ marca de condición de FWP \_ es un \_ \_ \_ enlace comodín**</span><span class="sxs-lookup"><span data-stu-id="cedf9-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-137">Comprueba si la aplicación especificó una dirección comodín al enlazar con una dirección de red local.</span><span class="sxs-lookup"><span data-stu-id="cedf9-137">Tests if the application specified a wildcard address when binding to a local network address.</span></span>

<span data-ttu-id="cedf9-138">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-138">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-139">\_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-139">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**la \_ marca de condición de FWP \_ es un punto de \_ \_ conexión sin formato \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-141">Comprueba si el punto de conexión local que está enviando y recibiendo tráfico es un punto de conexión sin formato.</span><span class="sxs-lookup"><span data-stu-id="cedf9-141">Tests if the local endpoint that is sending and receiving traffic is a raw endpoint.</span></span>

<span data-ttu-id="cedf9-142">Filtrar capas:</span><span class="sxs-lookup"><span data-stu-id="cedf9-142">Filtering layers:</span></span>

-   <span data-ttu-id="cedf9-143">\_Transporte de entrada de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-143">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="cedf9-144">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-144">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="cedf9-145">\_Transporte de salida de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-145">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="cedf9-146">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-146">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="cedf9-147">\_Datos de datagrama de capa FWPM \_ \_ \_ {V4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-147">FWPM\_LAYER\_DATAGRAM\_DATA\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="cedf9-148">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-148">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="cedf9-149">\_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-149">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-150">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-150">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-151">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-151">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**la \_ marca de condición de FWP \_ \_ es \_ FRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="cedf9-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-153">Comprueba si la estructura de la \_ lista de búferes de red que se \_ pasa a un controlador de llamada es un fragmento de paquetes IP.</span><span class="sxs-lookup"><span data-stu-id="cedf9-153">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver is an IP packet fragment.</span></span>

<span data-ttu-id="cedf9-154">Filtrar capas:</span><span class="sxs-lookup"><span data-stu-id="cedf9-154">Filtering layers:</span></span>

-   <span data-ttu-id="cedf9-155">FWPM \_ de \_ entrada \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-155">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-156">FWPM \_ \_ \_ IPPACKET \_ V {4 \| 6} \_ descartar</span><span class="sxs-lookup"><span data-stu-id="cedf9-156">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}\_DISCARD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**la \_ marca de condición de FWP \_ es un \_ \_ grupo de fragmentos \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-158">Comprueba si la \_ \_ estructura de la lista de búferes de red pasada a un controlador de llamada describe una lista vinculada de fragmentos de paquetes.</span><span class="sxs-lookup"><span data-stu-id="cedf9-158">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver describes a linked list of packet fragments.</span></span>

<span data-ttu-id="cedf9-159">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-159">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-160">\_Capa FWPM \_ IPFORWARD \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-160">FWPM\_LAYER\_IPFORWARD\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**la \_ marca de condición de FWP \_ \_ es \_ Natt de \_ \_ reclasificación de IPSec**</span><span class="sxs-lookup"><span data-stu-id="cedf9-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_NATT\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-162">Indica que el mismo paquete se está reclasificando en el nivel de transporte, cuando la corrección de compatibilidad de IPsec NAT traduce el valor del puerto remoto.</span><span class="sxs-lookup"><span data-stu-id="cedf9-162">Indicates that the same packet is being re-classified at the transport layer, when the IPsec NAT shim translates the remote port value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**la \_ marca de condición de FWP \_ \_ requiere \_ \_ clasificación Ale**</span><span class="sxs-lookup"><span data-stu-id="cedf9-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**FWP\_CONDITION\_FLAG\_REQUIRES\_ALE\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-164">Indica que el paquete se reclasificará en la capa de recepción y aceptación de ALE.</span><span class="sxs-lookup"><span data-stu-id="cedf9-164">Indicates that the packet will be reclassified at the ALE receive/accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**la \_ marca de condición de FWP \_ es un \_ \_ \_ enlace implícito**</span><span class="sxs-lookup"><span data-stu-id="cedf9-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_IMPLICIT\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-166">Comprueba si Windows Sockets realiza un enlace implícito.</span><span class="sxs-lookup"><span data-stu-id="cedf9-166">Tests if Windows Sockets is performing an implicit bind.</span></span>

<span data-ttu-id="cedf9-167">Solo está disponible en Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cedf9-167">Available only on Windows Vista and Windows Server 2008.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**la \_ marca de condición de FWP \_ \_ se \_ reensambla**</span><span class="sxs-lookup"><span data-stu-id="cedf9-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**FWP\_CONDITION\_FLAG\_IS\_REASSEMBLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-169">Comprueba si el paquete se ha reensamblado.</span><span class="sxs-lookup"><span data-stu-id="cedf9-169">Tests if the packet has been reassembled.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-170">Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-170">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

 

<span data-ttu-id="cedf9-171">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-171">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-172">FWPM \_ de \_ entrada \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-172">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**la \_ marca de condición de FWP \_ es la aplicación de \_ \_ nombre \_ \_ especificada**</span><span class="sxs-lookup"><span data-stu-id="cedf9-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**FWP\_CONDITION\_FLAG\_IS\_NAME\_APP\_SPECIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-174">Comprueba si el nombre del equipo del mismo nivel al que espera la aplicación se ha recibido a través de una API como [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) y no se ha obtenido a través de la heurística de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="cedf9-174">Tests if the name of the peer machine that the application is expecting to connect to has been received via an API such as [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) and not obtained via the caching heuristics.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-175">Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-175">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="cedf9-176">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-176">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-177">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-177">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**la \_ marca de condición de FWP \_ \_ es \_ promiscuo**</span><span class="sxs-lookup"><span data-stu-id="cedf9-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**FWP\_CONDITION\_FLAG\_IS\_PROMISCUOUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-179">Reservado.</span><span class="sxs-lookup"><span data-stu-id="cedf9-179">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**la \_ marca de condición de FWP \_ \_ es \_ auth \_ FW**</span><span class="sxs-lookup"><span data-stu-id="cedf9-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**FWP\_CONDITION\_FLAG\_IS\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-181">Comprueba si la conexión se ha autenticado de un extremo a otro, incluso si no se han comprobado los paquetes individuales.</span><span class="sxs-lookup"><span data-stu-id="cedf9-181">Tests if the connection is end-to-end authenticated, even if the individual packets have not been verified.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-182">Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-182">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="cedf9-183">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-183">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-184">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-184">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-185">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-185">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**la \_ marca de condición de FWP \_ \_ se está \_ reclasificando**</span><span class="sxs-lookup"><span data-stu-id="cedf9-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-187">Comprueba si el motor de filtrado está reclasificando una solicitud BIND o Listen anterior.</span><span class="sxs-lookup"><span data-stu-id="cedf9-187">Tests if the filtering engine is reclassifying a previous bind or listen request.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-188">Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-188">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="cedf9-189">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-189">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-190">\_Escucha de \_ autenticación Ale de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-190">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-191">\_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-191">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**la \_ marca de condición de FWP \_ es una \_ \_ conexión de proxy \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-193">Comprueba si la conexión usa un proxy.</span><span class="sxs-lookup"><span data-stu-id="cedf9-193">Tests if the connection uses a proxy.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-194">Solo está disponible en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="cedf9-194">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**la \_ marca de condición de FWP \_ es un \_ \_ \_ bucle invertido de APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="cedf9-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-196">Comprueba si el tráfico de red es el tráfico de bucle invertido del contenedor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cedf9-196">Tests if the network traffic is app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-197">Solo está disponible en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="cedf9-197">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**la \_ marca de condición de FWP \_ \_ no es un \_ \_ \_ bucle invertido de APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="cedf9-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-199">Comprueba si el tráfico de red es un tráfico de bucle invertido que no es de aplicación.</span><span class="sxs-lookup"><span data-stu-id="cedf9-199">Tests if the network traffic is non-app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-200">Solo está disponible en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="cedf9-200">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**la \_ marca de condición de FWP \_ \_ está \_ reservada**</span><span class="sxs-lookup"><span data-stu-id="cedf9-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**FWP\_CONDITION\_FLAG\_IS\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-202">Reservado.</span><span class="sxs-lookup"><span data-stu-id="cedf9-202">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**la \_ marca de condición de FWP \_ \_ está \_ respetando la \_ \_ autorización de la Directiva**</span><span class="sxs-lookup"><span data-stu-id="cedf9-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-204">Indica que se está realizando la clasificación actual para respetar la intención de que una aplicación de la tienda Windows redirigida se conecte a un host especificado.</span><span class="sxs-lookup"><span data-stu-id="cedf9-204">Indicates that the current classification is being performed to honor the intention of a redirected Windows Store app to connect to a specified host.</span></span> <span data-ttu-id="cedf9-205">Esta clasificación contendrá los mismos valores de campo clasificables que si la aplicación nunca se redirigió.</span><span class="sxs-lookup"><span data-stu-id="cedf9-205">Such a classification will contain the same classifiable field values as if the app were never redirected.</span></span> <span data-ttu-id="cedf9-206">La marca también indica que se invocará una clasificación futura para que coincida con el destino Redirigido efectivo.</span><span class="sxs-lookup"><span data-stu-id="cedf9-206">The flag also indicates that a future classification will be invoked to match the effective redirected destination.</span></span> <span data-ttu-id="cedf9-207">Si la aplicación se redirige a un servicio de proxy para su inspección, también significa que se invocará una clasificación futura en la conexión del proxy.</span><span class="sxs-lookup"><span data-stu-id="cedf9-207">If the app is redirected to a proxy service for inspection, it also means a future classification will be invoked on the proxy connection.</span></span> <span data-ttu-id="cedf9-208">Los controladores de llamadas normalmente deben permitir esta clasificación.</span><span class="sxs-lookup"><span data-stu-id="cedf9-208">Callout drivers should generally allow this classification.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-209">Solo está disponible en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="cedf9-209">Available only on Windows 8 and Windows Server 2012.</span></span>

 

<span data-ttu-id="cedf9-210">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-210">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-211">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-211">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="cedf9-212">Las marcas siguientes especifican el motivo por el que se va a autorizar una conexión previamente autorizada.</span><span class="sxs-lookup"><span data-stu-id="cedf9-212">The following flags specify the reason for reauthorizing a previously authorized connection.</span></span> <span data-ttu-id="cedf9-213">Estas marcas y las capas de filtrado donde se pueden usar se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="cedf9-213">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-214">Estas condiciones de filtrado solo están disponibles en Windows Server 2008 R2, Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-214">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="cedf9-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**cambio en la \_ \_ Directiva de motivo de reautorización de la condición de \_ \_ FWP \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-216">Indica que la conexión se ha reautorizado debido a que se han agregado o quitado filtros.</span><span class="sxs-lookup"><span data-stu-id="cedf9-216">Indicates that the connection was reauthorized due to filters being added or removed.</span></span>

<span data-ttu-id="cedf9-217">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-217">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-218">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-218">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-219">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-219">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**causa de reautor de la condición de FWP \_ \_ \_ \_ nueva \_ interfaz de llegada \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_ARRIVAL\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-221">Indica que el paquete llegó desde una interfaz desconocida.</span><span class="sxs-lookup"><span data-stu-id="cedf9-221">Indicates that the packet has arrived from an unknown interface.</span></span>

<span data-ttu-id="cedf9-222">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-222">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-223">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-223">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-224">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-224">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**condición de FWP reautor de la razón de la \_ \_ \_ \_ nueva \_ salto \_ de la interfaz**</span><span class="sxs-lookup"><span data-stu-id="cedf9-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_NEXTHOP\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-226">Indica que el paquete se va a deshacer de una interfaz desconocida.</span><span class="sxs-lookup"><span data-stu-id="cedf9-226">Indicates that the packet will be departing from an unknown interface.</span></span>

<span data-ttu-id="cedf9-227">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-227">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-228">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-228">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-229">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-229">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**\_paso de \_ creación de \_ Perfil de \_ motivo \_ de la condición de FWP**</span><span class="sxs-lookup"><span data-stu-id="cedf9-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_PROFILE\_CROSSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-231">Indica que el paquete ha pasado a través de interfaces de más de una categoría de red.</span><span class="sxs-lookup"><span data-stu-id="cedf9-231">Indicates that the packet has passed through interfaces of more than one network category.</span></span>

<span data-ttu-id="cedf9-232">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-232">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-233">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-233">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-234">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-234">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**\_conclusión de \_ reautorización de la condición de \_ \_ FWP \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_CLASSIFY\_COMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-236">Indica que ahora se permite completar una conexión retenida previamente.</span><span class="sxs-lookup"><span data-stu-id="cedf9-236">Indicates that a previously held connection is now being allowed to complete.</span></span>

<span data-ttu-id="cedf9-237">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-237">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-238">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-238">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-239">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-239">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**\_motivo de REautorización de la condición de FWP propiedades de \_ \_ \_ IPSec \_ \_ modificadas**</span><span class="sxs-lookup"><span data-stu-id="cedf9-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_IPSEC\_PROPERTIES\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-241">Indica que las propiedades de IPsec han cambiado o que la conexión ha cambiado de texto no cifrado a una conexión segura.</span><span class="sxs-lookup"><span data-stu-id="cedf9-241">Indicates that IPsec properties have changed, or that the connection has changed from clear text to a secure connection.</span></span>

<span data-ttu-id="cedf9-242">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-242">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-243">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-243">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-244">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-244">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**Estado de la \_ \_ inspección de \_ \_ flujo medio \_ \_ de la condición de FWP REAUTORICE**</span><span class="sxs-lookup"><span data-stu-id="cedf9-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_MID\_STREAM\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-246">Indica que ahora se está inspeccionando una conexión TCP establecida previamente.</span><span class="sxs-lookup"><span data-stu-id="cedf9-246">Indicates that a previously established TCP connection is now being inspected.</span></span>

<span data-ttu-id="cedf9-247">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-247">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-248">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-248">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-249">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-249">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**error de la \_ \_ propiedad de \_ socket de motivo de reautorización de la \_ \_ condición de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_SOCKET\_PROPERTY\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-251">Indica que se han establecido las propiedades de socket una vez que se ha autorizado y establecido una conexión.</span><span class="sxs-lookup"><span data-stu-id="cedf9-251">Indicates that socket properties have been set after a connection was authorized and established.</span></span>

<span data-ttu-id="cedf9-252">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-252">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-253">FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-253">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-254">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-254">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**condición de FWP \_ \_ reautor de la causa del \_ \_ nuevo \_ paquete de entrada de \_ MCAST \_ BCAST \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_INBOUND\_MCAST\_BCAST\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-256">Indica que se están volviendo a autorizar nuevos paquetes entrantes de multidifusión o difusión en las llamadas de aceptación de recepción de ALE \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cedf9-256">Indicates that new inbound multicast or broadcast packets are being re-authorized at ALE\_RECV\_ACCEPT callouts.</span></span>

<span data-ttu-id="cedf9-257">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-257">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-258">Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-258">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="cedf9-259">Las marcas siguientes especifican las propiedades de socket que están relacionadas con si una aplicación desea recibir tráfico de cruce seguro del perímetro.</span><span class="sxs-lookup"><span data-stu-id="cedf9-259">The following flags specify socket properties which are related to whether an application wants to receive Edge Traversal traffic.</span></span> <span data-ttu-id="cedf9-260">Estas marcas y las capas de filtrado donde se pueden usar se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="cedf9-260">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-261">Estas condiciones de filtrado solo están disponibles en Windows Server 2008 R2, Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cedf9-261">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="cedf9-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**la \_ marca de propiedad del socket de condición de FWP \_ \_ es el \_ \_ \_ \_ Puerto RPC del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_IS\_SYSTEM\_PORT\_RPC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-263">Indica que la aplicación se comunica con un puerto RPC dinámico.</span><span class="sxs-lookup"><span data-stu-id="cedf9-263">Indicates that the application is communicating with a dynamic RPC port.</span></span>

<span data-ttu-id="cedf9-264">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-264">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-265">\_Escucha de \_ autenticación Ale de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-265">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-266">\_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-266">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**identificador de propiedad de socket de condición de FWP \_ \_ \_ \_ \_ permitir \_ \_ tráfico perimetral**</span><span class="sxs-lookup"><span data-stu-id="cedf9-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_ALLOW\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-268">Indica que la aplicación desea recibir tráfico específico de cruce seguro del perímetro.</span><span class="sxs-lookup"><span data-stu-id="cedf9-268">Indicates that the application wants to receive edge traversal-specific traffic.</span></span>

<span data-ttu-id="cedf9-269">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-269">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-270">\_Escucha de \_ autenticación Ale de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-270">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-271">\_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-271">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**identificador de propiedad del socket de condición de FWP \_ \_ \_ \_ \_ denegar el \_ \_ tráfico perimetral**</span><span class="sxs-lookup"><span data-stu-id="cedf9-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_DENY\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-273">Indica que la aplicación no desea recibir o procesar el tráfico específico de cruce seguro del perímetro.</span><span class="sxs-lookup"><span data-stu-id="cedf9-273">Indicates that the application does not want to receive or process edge traversal-specific traffic.</span></span>

<span data-ttu-id="cedf9-274">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-274">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-275">\_Escucha de \_ autenticación Ale de capa FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-275">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="cedf9-276">\_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="cedf9-276">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="cedf9-277">Las marcas siguientes especifican los detalles de conexión relacionados con el filtrado L2.</span><span class="sxs-lookup"><span data-stu-id="cedf9-277">The following flags specify connection details related to L2 filtering.</span></span>

> [!Note]  
> <span data-ttu-id="cedf9-278">Estas condiciones de filtrado solo están disponibles en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="cedf9-278">These filtering conditions are available only on Windows 8 and Windows Server 2012.</span></span>

 

<dl> <dt>

<span data-ttu-id="cedf9-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**La \_ condición de FWP \_ L2 \_ es una \_ \_ Ethernet nativa**</span><span class="sxs-lookup"><span data-stu-id="cedf9-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-280">Indica que la conexión es un Ethernet nativo.</span><span class="sxs-lookup"><span data-stu-id="cedf9-280">Indicates that the connection is native Ethernet.</span></span>

<span data-ttu-id="cedf9-281">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-281">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-282">\_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-282">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-283">marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-283">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="cedf9-284">\_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-284">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-285">\_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-285">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**La \_ condición de FWP \_ L2 \_ es \_ Wi-Fi**</span><span class="sxs-lookup"><span data-stu-id="cedf9-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP\_CONDITION\_L2\_IS\_WIFI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-287">Indica que la conexión es Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="cedf9-287">Indicates that the connection is Wi-Fi.</span></span>

<span data-ttu-id="cedf9-288">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-288">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-289">\_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-289">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-290">marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-290">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="cedf9-291">\_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-291">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-292">\_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-292">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**La \_ condición de FWP \_ L2 \_ es \_ \_ banda ancha móvil**</span><span class="sxs-lookup"><span data-stu-id="cedf9-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-294">Indica que la conexión es banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="cedf9-294">Indicates that the connection is mobile broadband.</span></span>

<span data-ttu-id="cedf9-295">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-295">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-296">\_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-296">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-297">marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-297">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="cedf9-298">\_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-298">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-299">\_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-299">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**La \_ condición de FWP \_ L2 \_ es \_ Wi-Fi \_ Direct \_ Data**</span><span class="sxs-lookup"><span data-stu-id="cedf9-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-301">Indica que la conexión es Wi-Fi directa.</span><span class="sxs-lookup"><span data-stu-id="cedf9-301">Indicates that the connection is Wi-Fi Direct.</span></span>

<span data-ttu-id="cedf9-302">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-302">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-303">\_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-303">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-304">marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-304">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="cedf9-305">\_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-305">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-306">\_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-306">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**La \_ condición de FWP \_ L2 \_ es \_ VM2VM**</span><span class="sxs-lookup"><span data-stu-id="cedf9-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP\_CONDITION\_L2\_IS\_VM2VM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-308">Indica que la conexión se encuentra entre las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="cedf9-308">Indicates that the connection is between virtual machines.</span></span>

<span data-ttu-id="cedf9-309">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-309">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-310">\_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-310">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-311">marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-311">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="cedf9-312">\_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-312">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-313">\_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-313">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**La \_ condición de FWP \_ L2 \_ tiene un paquete con \_ formato incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-315">Indica que un paquete parece tener un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="cedf9-315">Indicates that a packet appears to be malformed.</span></span>

<span data-ttu-id="cedf9-316">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-316">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-317">\_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-317">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-318">marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-318">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="cedf9-319">\_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-319">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-320">\_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-320">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**La \_ condición de FWP \_ L2 \_ es \_ grupo de \_ fragmentos IP \_**</span><span class="sxs-lookup"><span data-stu-id="cedf9-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-322">Indica un grupo de fragmentos de paquetes IP.</span><span class="sxs-lookup"><span data-stu-id="cedf9-322">Indicates an IP packet fragment group.</span></span>

<span data-ttu-id="cedf9-323">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-323">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-324">\_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-324">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-325">marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-325">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="cedf9-326">\_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-326">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-327">\_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-327">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cedf9-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**Condición de FWP \_ \_ L2 \_ si el \_ conector \_ está presente**</span><span class="sxs-lookup"><span data-stu-id="cedf9-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cedf9-329">Indica que hay un conector presente.</span><span class="sxs-lookup"><span data-stu-id="cedf9-329">Indicates that a connector is present.</span></span>

<span data-ttu-id="cedf9-330">Nivel de filtrado:</span><span class="sxs-lookup"><span data-stu-id="cedf9-330">Filtering layer:</span></span>

-   <span data-ttu-id="cedf9-331">\_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-331">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-332">marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-332">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="cedf9-333">\_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM</span><span class="sxs-lookup"><span data-stu-id="cedf9-333">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="cedf9-334">\_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="cedf9-334">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cedf9-335">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cedf9-335">Requirements</span></span>



| <span data-ttu-id="cedf9-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="cedf9-336">Requirement</span></span> | <span data-ttu-id="cedf9-337">Value</span><span class="sxs-lookup"><span data-stu-id="cedf9-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cedf9-338">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cedf9-338">Minimum supported client</span></span><br/> | <span data-ttu-id="cedf9-339">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cedf9-339">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cedf9-340">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cedf9-340">Minimum supported server</span></span><br/> | <span data-ttu-id="cedf9-341">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cedf9-341">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cedf9-342">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cedf9-342">Header</span></span><br/>                   | <dl> <span data-ttu-id="cedf9-343"><dt>Fwptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="cedf9-343"><dt>Fwptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cedf9-344">Vea también</span><span class="sxs-lookup"><span data-stu-id="cedf9-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cedf9-345">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="cedf9-345">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

