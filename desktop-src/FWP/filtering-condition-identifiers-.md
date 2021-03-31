---
title: Filtrar los identificadores de condición (Fwpmu. h)
description: Los identificadores de condición de filtrado de la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.
ms.assetid: 4f0b970a-e511-4107-8023-22a8775905b9
topic_type:
- apiref
api_name:
- FWPM_CONDITION_INTERFACE_MAC_ADDRESS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS
- FWPM_CONDITION_MAC_REMOTE_ADDRESS
- FWPM_CONDITION_ETHER_TYPE
- FWPM_CONDITION_VLAN_ID
- FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID
- FWPM_CONDITION_NDIS_PORT
- FWPM_CONDITION_NDIS_MEDIA_TYPE
- FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE
- FWPM_CONDITION_L2_FLAGS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_SOURCE_ADDRESS
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS
- FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_SOURCE_PORT
- FWPM_CONDITION_VSWITCH_ICMP_TYPE
- FWPM_CONDITION_IP_DESTINATION_PORT
- FWPM_CONDITION_VSWITCH_ICMP_CODE
- FWPM_CONDITION_VSWITCH_ID
- FWPM_CONDITION_VSWITCH_NETWORK_TYPE
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_SOURCE_VM_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE
- FWPM_CONDITION_INTERFACE
- FWPM_CONDITION_ALE_PACKAGE_ID
- FWPM_CONDITION_ALE_ORIGINAL_APP_ID
- FWPM_CONDITION_IP_NEXTHOP_ADDRESS
- FWPM_CONDITION_IP_NEXTHOP_INTERFACE
- FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE
- FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE
- FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX
- FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ORIGINAL_PROFILE_ID
- FWPM_CONDITION_CURRENT_PROFILE_ID
- FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID
- FWPM_CONDITION_REAUTHORIZE_REASON
- FWPM_CONDITION_ALE_REAUTH_REASON
- FWPM_CONDITION_ORIGINAL_ICMP_TYPE
- FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE
- FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE
- FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH
- FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY
- FWPM_CONDITION_IP_ARRIVAL_INTERFACE
- FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE
- FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE
- FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX
- FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_TYPE
- FWPM_CONDITION_LOCAL_TUNNEL_TYPE
- FWPM_CONDITION_IP_LOCAL_ADDRESS
- FWPM_CONDITION_IP_REMOTE_ADDRESS
- FWPM_CONDITION_IP_SOURCE_ADDRESS
- FWPM_CONDITION_IP_DESTINATION_ADDRESS
- FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_LOCAL_INTERFACE
- FWPM_CONDITION_INTERFACE_TYPE
- FWPM_CONDITION_TUNNEL_TYPE
- FWPM_CONDITION_IP_FORWARD_INTERFACE
- FWPM_CONDITION_IP_PROTOCOL
- FWPM_CONDITION_IP_LOCAL_PORT
- FWPM_CONDITION_ICMP_TYPE
- FWPM_CONDITION_IP_REMOTE_PORT
- FWPM_CONDITION_ICMP_CODE
- FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS
- FWPM_CONDITION_EMBEDDED_PROTOCOL
- FWPM_CONDITION_EMBEDDED_LOCAL_PORT
- FWPM_CONDITION_EMBEDDED_REMOTE_PORT
- FWPM_CONDITION_FLAGS
- FWPM_CONDITION_DIRECTION
- FWPM_CONDITION_INTERFACE_INDEX
- FWPM_CONDITION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ALE_APP_ID
- FWPM_CONDITION_ALE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_MACHINE_ID
- FWPM_CONDITION_ALE_PROMISCUOUS_MODE
- FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT
- FWPM_CONDITION_ALE_NAP_CONTEXT
- FWPM_CONDITION_QM_MODE
- FWPM_CONDITION_KM_AUTH_NAP_CONTEXT
- FWPM_CONDITION_PEER_NAME
- FWPM_CONDITION_REMOTE_ID
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_KM_TYPE
- FWPM_CONDITION_KM_MODE
- FWPM_CONDITION_IPSEC_POLICY_KEY
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_REMOTE_USER_TOKEN
- FWPM_CONDITION_RPC_IF_UUID
- FWPM_CONDITION_RPC_IF_VERSION
- FWPM_CONDITION_RPC_IF_FLAG
- FWPM_CONDITION_DCOM_APP_ID
- FWPM_CONDITION_IMAGE_NAME
- FWPM_CONDITION_RPC_PROTOCOL
- FWPM_CONDITION_RPC_AUTH_TYPE
- FWPM_CONDITION_RPC_AUTH_LEVEL
- FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM
- FWPM_CONDITION_SEC_KEY_SIZE
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V4
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V6
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V4
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V6
- FWPM_CONDITION_PIPE
- FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID
- FWPM_CONDITION_RPC_EP_VALUE
- FWPM_CONDITION_RPC_EP_FLAGS
- FWPM_CONDITION_CLIENT_TOKEN
- FWPM_CONDITION_RPC_SERVER_NAME
- FWPM_CONDITION_RPC_SERVER_PORT
- FWPM_CONDITION_RPC_PROXY_AUTH_TYPE
- FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH
- FWPM_CONDITION_CLIENT_CERT_OID
- FWPM_CONDITION_NET_EVENT_TYPE
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617946e5708bb982f96edcad155bcbf2509596dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801034"
---
# <a name="filtering-condition-identifiers"></a><span data-ttu-id="82005-103">Filtrado de identificadores de condición</span><span class="sxs-lookup"><span data-stu-id="82005-103">Filtering Condition Identifiers</span></span>

<span data-ttu-id="82005-104">Los identificadores de condición de filtrado de la plataforma de filtrado de Windows (WFP) se representan mediante un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="82005-104">The Windows Filtering Platform (WFP) filtering condition identifiers are each represented by a **GUID**.</span></span> <span data-ttu-id="82005-105">El tipo de datos para el valor de la condición para cada condición de filtrado se especifica como un [**\_ \_ tipo de datos de FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="82005-105">The data type for the condition value for each filtering condition is specified as an [**FWP\_DATA\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="82005-106">Estos identificadores y sus tipos de datos se definen aquí.</span><span class="sxs-lookup"><span data-stu-id="82005-106">These identifiers and their data types are defined here.</span></span>

<span data-ttu-id="82005-107">Las condiciones estándar se enumeran en primer lugar, seguidas de las condiciones específicas del modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="82005-107">The standard conditions are listed first, followed by the conditions specific to user mode.</span></span> <span data-ttu-id="82005-108">Las condiciones se agrupan por sistema operativo compatible, por lo que puede saber fácilmente qué condiciones se admiten para un sistema operativo determinado.</span><span class="sxs-lookup"><span data-stu-id="82005-108">Conditions are grouped by supported operating system, so that you can easily tell which conditions are supported for a given OS.</span></span>

> [!Note]  
> <span data-ttu-id="82005-109">Cada una de las siguientes condiciones de filtrado solo está disponible en un subconjunto de las capas de filtrado de WFP.</span><span class="sxs-lookup"><span data-stu-id="82005-109">Each of the following filtering conditions is available only at a subset of the WFP filtering layers.</span></span> <span data-ttu-id="82005-110">Para obtener más información sobre la disponibilidad de cada condición en un nivel determinado, consulte [**condiciones de filtrado disponibles en cada capa de filtrado**](filtering-conditions-available-at-each-filtering-layer.md).</span><span class="sxs-lookup"><span data-stu-id="82005-110">For more information on each condition's availability at any given layer, see [**Filtering Conditions Available at Each Filtering Layer**](filtering-conditions-available-at-each-filtering-layer.md).</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="82005-111">Condiciones disponibles para Windows 8 y Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="82005-111">Conditions available for Windows 8 and Windows Server 2012</span></span></th>
<th style="text-align: left;"><span data-ttu-id="82005-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="82005-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <span data-ttu-id="82005-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-114">Dirección MAC de una interfaz local determinada.</span><span class="sxs-lookup"><span data-stu-id="82005-114">The MAC address of a particular local interface.</span></span><br/> <span data-ttu-id="82005-115"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-115"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <span data-ttu-id="82005-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-117">Dirección de destino de un marco entrante o de una dirección de origen de un marco saliente.</span><span class="sxs-lookup"><span data-stu-id="82005-117">Destination address of an inbound frame, or source address of an outbound frame.</span></span><br/> <span data-ttu-id="82005-118"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-118"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <span data-ttu-id="82005-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-120">Dirección de origen de un marco de entrada o dirección de destino de un marco de salida.</span><span class="sxs-lookup"><span data-stu-id="82005-120">Source address of an inbound frame, or destination address of an outbound frame.</span></span><br/> <span data-ttu-id="82005-121"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-121"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <span data-ttu-id="82005-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-123">El tipo de datos de la carga de red Ethernet V2.</span><span class="sxs-lookup"><span data-stu-id="82005-123">The Ethernet V2 network payload data type.</span></span> <span data-ttu-id="82005-124">(Vea ETHERNET_TYPE_IPV4, etc. en netiodef. h).</span><span class="sxs-lookup"><span data-stu-id="82005-124">(See ETHERNET_TYPE_IPV4, etc. in netiodef.h.)</span></span><br/> <span data-ttu-id="82005-125"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-125"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <span data-ttu-id="82005-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-127">El encabezado de 16 bits de VLAN, incluidos los campos VID, CFI y Priority según el estándar 802.1 q (consulte VLAN_TAG en netiodef. h para las posiciones de los campos de bits).</span><span class="sxs-lookup"><span data-stu-id="82005-127">The 16-bits of VLAN header including the VID, CFI, and Priority fields as per the 802.1q standard (see VLAN_TAG in netiodef.h for the positions of the bitfields).</span></span><br/> <span data-ttu-id="82005-128"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-128"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <span data-ttu-id="82005-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-130">Identificador único de la red vSwitch.</span><span class="sxs-lookup"><span data-stu-id="82005-130">Unique identifier for the vSwitch network.</span></span> <span data-ttu-id="82005-131">No se puede usar junto con VLAN_IDs.</span><span class="sxs-lookup"><span data-stu-id="82005-131">Cannot be used in conjunction with VLAN_IDs.</span></span><br/> <span data-ttu-id="82005-132"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-132"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <span data-ttu-id="82005-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-134">El número de puerto del puerto NDIS.</span><span class="sxs-lookup"><span data-stu-id="82005-134">The port number of the NDIS port.</span></span><br/> <span data-ttu-id="82005-135"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-135"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <span data-ttu-id="82005-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-137">El tipo de medio del puerto NDIS.</span><span class="sxs-lookup"><span data-stu-id="82005-137">The media type of the NDIS port.</span></span><br/> <span data-ttu-id="82005-138"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-138"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="82005-139"><strong>Valores posibles:</strong> Cualquiera de los valores de enumeración de <strong>NDIS_MEDIUM</strong> .</span><span class="sxs-lookup"><span data-stu-id="82005-139"><strong>Possible values:</strong> Any of the <strong>NDIS_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="82005-140">(Vea ntddndis. h).</span><span class="sxs-lookup"><span data-stu-id="82005-140">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <span data-ttu-id="82005-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-142">El tipo de medio físico del puerto NDIS.</span><span class="sxs-lookup"><span data-stu-id="82005-142">The physical media type of the NDIS port.</span></span><br/> <span data-ttu-id="82005-143"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-143"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="82005-144"><strong>Valores posibles:</strong> Cualquiera de los valores de enumeración de <strong>NDIS_PHYSICAL_MEDIUM</strong> .</span><span class="sxs-lookup"><span data-stu-id="82005-144"><strong>Possible values:</strong> Any of the <strong>NDIS_PHYSICAL_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="82005-145">(Vea ntddndis. h).</span><span class="sxs-lookup"><span data-stu-id="82005-145">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <span data-ttu-id="82005-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-147">Una operación OR bit a bit de una combinación de marcas de condición de filtrado.</span><span class="sxs-lookup"><span data-stu-id="82005-147">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="82005-148"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-148"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="82005-149"><strong>Valores posibles:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-149"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span><span class="sxs-lookup"><span data-stu-id="82005-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span></span></li>
<li><span data-ttu-id="82005-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="82005-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span></span></li>
<li><span data-ttu-id="82005-152">FWP_CONDITION_L2_IS_WIFI</span><span class="sxs-lookup"><span data-stu-id="82005-152">FWP_CONDITION_L2_IS_WIFI</span></span></li>
<li><span data-ttu-id="82005-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span><span class="sxs-lookup"><span data-stu-id="82005-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <span data-ttu-id="82005-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-155">Tipo de dirección de la dirección local física.</span><span class="sxs-lookup"><span data-stu-id="82005-155">The address type of the physical local address.</span></span><br/> <span data-ttu-id="82005-156"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-156"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="82005-157"><strong>Valores posibles:</strong> Cualquiera de los siguientes valores de enumeración de <strong>DL_ADDRESS_TYPE</strong> .</span><span class="sxs-lookup"><span data-stu-id="82005-157"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="82005-158">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="82005-158">DlUnicast</span></span></li>
<li><span data-ttu-id="82005-159">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="82005-159">DlMulticast</span></span></li>
<li><span data-ttu-id="82005-160">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="82005-160">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <span data-ttu-id="82005-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-162">Tipo de dirección de la dirección remota física.</span><span class="sxs-lookup"><span data-stu-id="82005-162">The address type of the physical remote address.</span></span><br/> <span data-ttu-id="82005-163"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-163"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="82005-164"><strong>Valores posibles:</strong> Cualquiera de los siguientes valores de enumeración de <strong>DL_ADDRESS_TYPE</strong> .</span><span class="sxs-lookup"><span data-stu-id="82005-164"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="82005-165">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="82005-165">DlUnicast</span></span></li>
<li><span data-ttu-id="82005-166">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="82005-166">DlMulticast</span></span></li>
<li><span data-ttu-id="82005-167">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="82005-167">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <span data-ttu-id="82005-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-169">Dirección de origen física de un marco.</span><span class="sxs-lookup"><span data-stu-id="82005-169">The physical source address of a frame.</span></span><br/> <span data-ttu-id="82005-170"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-170"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <span data-ttu-id="82005-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-172">Dirección de destino física de un marco.</span><span class="sxs-lookup"><span data-stu-id="82005-172">The physical destination address of a frame.</span></span><br/> <span data-ttu-id="82005-173"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-173"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <span data-ttu-id="82005-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-175">Tipo de dirección de la dirección de destino física.</span><span class="sxs-lookup"><span data-stu-id="82005-175">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="82005-176"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-176"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="82005-177"><strong>Valores posibles:</strong> Cualquiera de los siguientes valores de enumeración de <strong>DL_ADDRESS_TYPE</strong> .</span><span class="sxs-lookup"><span data-stu-id="82005-177"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="82005-178">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="82005-178">DlUnicast</span></span></li>
<li><span data-ttu-id="82005-179">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="82005-179">DlMulticast</span></span></li>
<li><span data-ttu-id="82005-180">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="82005-180">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <span data-ttu-id="82005-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-182">Tipo de dirección de la dirección de destino física.</span><span class="sxs-lookup"><span data-stu-id="82005-182">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="82005-183"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-183"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="82005-184"><strong>Valores posibles:</strong> Cualquiera de los siguientes valores de enumeración de <strong>DL_ADDRESS_TYPE</strong> .</span><span class="sxs-lookup"><span data-stu-id="82005-184"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="82005-185">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="82005-185">DlUnicast</span></span></li>
<li><span data-ttu-id="82005-186">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="82005-186">DlMulticast</span></span></li>
<li><span data-ttu-id="82005-187">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="82005-187">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <span data-ttu-id="82005-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-189">Puerto de origen del transporte del paquete.</span><span class="sxs-lookup"><span data-stu-id="82005-189">The source port of the packet's transport.</span></span><br/> <span data-ttu-id="82005-190"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-190"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <span data-ttu-id="82005-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-192">Campo de tipo ICMP, tal y como se especifica en RFC 792.</span><span class="sxs-lookup"><span data-stu-id="82005-192">The ICMP type field, as specified in RFC 792.</span></span><br/> <span data-ttu-id="82005-193"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-193"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <span data-ttu-id="82005-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-195">Puerto de destino del transporte del paquete.</span><span class="sxs-lookup"><span data-stu-id="82005-195">The destination port of the packet's transport.</span></span><br/> <span data-ttu-id="82005-196"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-196"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <span data-ttu-id="82005-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-198">El campo de Código ICMP, tal como se especifica en RFC 792.</span><span class="sxs-lookup"><span data-stu-id="82005-198">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="82005-199"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-199"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <span data-ttu-id="82005-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-201">Identificador único de una instancia de vSwitch.</span><span class="sxs-lookup"><span data-stu-id="82005-201">Unique identifier of an vSwitch instance.</span></span><br/> <span data-ttu-id="82005-202"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-202"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <span data-ttu-id="82005-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-204">Especifica si la instancia de vSwitch es parte de una red virtual externa, interna o privada.</span><span class="sxs-lookup"><span data-stu-id="82005-204">Specifies whether the vSwitch instance is part of an external, internal, or private virtual network.</span></span><br/> <span data-ttu-id="82005-205"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-205"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <span data-ttu-id="82005-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-207">Identificador único del origen del paquete actual.</span><span class="sxs-lookup"><span data-stu-id="82005-207">Unique identifier of the source of the current packet.</span></span> <span data-ttu-id="82005-208">(El nombre de una máquina virtual NIC, P-NIC o V-NIC).</span><span class="sxs-lookup"><span data-stu-id="82005-208">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="82005-209"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-209"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <span data-ttu-id="82005-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-211">Identificador único del destino del paquete actual.</span><span class="sxs-lookup"><span data-stu-id="82005-211">Unique identifier of the destination of the current packet.</span></span> <span data-ttu-id="82005-212">(El nombre de una máquina virtual NIC, P-NIC o V-NIC).</span><span class="sxs-lookup"><span data-stu-id="82005-212">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="82005-213"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-213"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <span data-ttu-id="82005-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-215">Identificador único de la máquina virtual de origen vSwitch.</span><span class="sxs-lookup"><span data-stu-id="82005-215">Unique identifier of the vSwitch source virtual machine.</span></span><br/> <span data-ttu-id="82005-216"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-216"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <span data-ttu-id="82005-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-218">Identificador único de la máquina virtual de destino vSwitch.</span><span class="sxs-lookup"><span data-stu-id="82005-218">Unique identifier of the vSwitch destination virtual machine.</span></span><br/> <span data-ttu-id="82005-219"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-219"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <span data-ttu-id="82005-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-221">Tipo de interfaz del origen del paquete actual.</span><span class="sxs-lookup"><span data-stu-id="82005-221">Interface type of the source of the current packet.</span></span><br/> <span data-ttu-id="82005-222"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-222"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="82005-223"><strong>Valores posibles:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-223"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-224">SwitchNicSyntheticNic (cuando el tipo de interfaz es VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="82005-224">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="82005-225">SwitchNicEmulatedNic (cuando el tipo de interfaz es VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="82005-225">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="82005-226">SwitchNicPhysicalNic (cuando el tipo de interfaz es P-NIC)</span><span class="sxs-lookup"><span data-stu-id="82005-226">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="82005-227">SwitchNicVNic (cuando el tipo de interfaz es V-NIC, conectado a la partición del host)</span><span class="sxs-lookup"><span data-stu-id="82005-227">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <span data-ttu-id="82005-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-229">Tipo de interfaz del destino del paquete actual.</span><span class="sxs-lookup"><span data-stu-id="82005-229">Interface type of the destination of the current packet.</span></span><br/> <span data-ttu-id="82005-230"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-230"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="82005-231"><strong>Valores posibles:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-231"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-232">SwitchNicSyntheticNic (cuando el tipo de interfaz es VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="82005-232">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="82005-233">SwitchNicEmulatedNic (cuando el tipo de interfaz es VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="82005-233">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="82005-234">SwitchNicPhysicalNic (cuando el tipo de interfaz es P-NIC)</span><span class="sxs-lookup"><span data-stu-id="82005-234">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="82005-235">SwitchNicVNic (cuando el tipo de interfaz es V-NIC, conectado a la partición del host)</span><span class="sxs-lookup"><span data-stu-id="82005-235">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <span data-ttu-id="82005-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-237">LUID para la interfaz de red asociada con la dirección IP local.</span><span class="sxs-lookup"><span data-stu-id="82005-237">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="82005-238"><strong>Tipo de datos:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="82005-238"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <span data-ttu-id="82005-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-240">El identificador de seguridad (SID) de un contenedor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82005-240">The security identifier (SID) of an app container.</span></span><br/> <span data-ttu-id="82005-241"><strong>Tipo de datos:</strong> FWP_SID</span><span class="sxs-lookup"><span data-stu-id="82005-241"><strong>Data type:</strong> FWP_SID</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <span data-ttu-id="82005-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-243">La ruta de acceso completa del dispositivo de la aplicación, como &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .</span><span class="sxs-lookup"><span data-stu-id="82005-243">The fully qualified device path of the application, such as &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.</span></span> <span data-ttu-id="82005-244">Cuando se haya Redirigido una conexión, será el identificador de la aplicación de origen; de lo contrario, será igual que <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span><span class="sxs-lookup"><span data-stu-id="82005-244">When a connection has been redirected, this will be the identifier of the originating app; otherwise this will be the same as <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span></span><br/> <span data-ttu-id="82005-245"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-245"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
</tbody>
</table>





| <span data-ttu-id="82005-246">Condiciones disponibles para Windows 7, Windows Server 2008 R2 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="82005-246">Conditions available for Windows 7, Windows Server 2008 R2, and later</span></span>                                                                                                                                                                                                    | <span data-ttu-id="82005-247">Descripción</span><span class="sxs-lookup"><span data-stu-id="82005-247">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <span data-ttu-id="82005-248"><dt>**\_dirección de \_ \_ NEXTHOP IP de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-248"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_ADDRESS**</dt></span></span> </dl>                                             | <span data-ttu-id="82005-249">Dirección IP de la interfaz de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="82005-249">The IP address of the next-hop interface.</span></span><br/> <span data-ttu-id="82005-250">**Tipo de datos:** Máscara de dirección de FWP \_ V4 \_ \_</span><span class="sxs-lookup"><span data-stu-id="82005-250">**Data type:** FWP\_V4\_ADDR\_MASK</span></span><br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <span data-ttu-id="82005-251"><dt>**\_ \_ interfaz NEXTHOP de IP de condición FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-251"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>                                       | <span data-ttu-id="82005-252">La interfaz de próximo salto desde la que se va a deshacer el paquete.</span><span class="sxs-lookup"><span data-stu-id="82005-252">The next-hop interface from which the packet will be departing.</span></span> <br/> <span data-ttu-id="82005-253">**Tipo de datos:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="82005-253">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <span data-ttu-id="82005-254"><dt>**\_tipo de \_ \_ interfaz NEXTHOP de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-254"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_TYPE**</dt></span></span> </dl>                                 | <span data-ttu-id="82005-255">Tipo de interfaz de la interfaz de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="82005-255">The interface type of the next-hop interface.</span></span><br/> <span data-ttu-id="82005-256">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-256">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <span data-ttu-id="82005-257"><dt>**\_tipo de túnel FWPM Condition \_ NEXTHOP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-257"><dt>**FWPM\_CONDITION\_NEXTHOP\_TUNNEL\_TYPE**</dt></span></span> </dl>                                          | <span data-ttu-id="82005-258">El tipo de túnel de la interfaz de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="82005-258">The tunnel type of the next-hop interface.</span></span><br/> <span data-ttu-id="82005-259">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-259">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <span data-ttu-id="82005-260"><dt>**\_Índice de \_ \_ interfaz NEXTHOP de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-260"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_INDEX**</dt></span></span> </dl>                              | <span data-ttu-id="82005-261">Índice de interfaz de la interfaz de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="82005-261">The interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="82005-262">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-262">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <span data-ttu-id="82005-263"><dt>**\_Índice de \_ la \_ \_ subinterfaz de FWPM Condition NEXTHOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-263"><dt>**FWPM\_CONDITION\_NEXTHOP\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl>                 | <span data-ttu-id="82005-264">Índice de la subinterfaz de la interfaz de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="82005-264">The sub-interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="82005-265">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-265">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <span data-ttu-id="82005-266"><dt>**\_identificador de \_ \_ perfil original de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-266"><dt>**FWPM\_CONDITION\_ORIGINAL\_PROFILE\_ID**</dt></span></span> </dl>                                          | <span data-ttu-id="82005-267">Categoría de red de la interfaz de llegada o de próximo salto a través de la cual se crea el flujo de ALE (entrante o saliente).</span><span class="sxs-lookup"><span data-stu-id="82005-267">The network category of the arrival or next-hop interface through which the ALE flow (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="82005-268">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-268">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <span data-ttu-id="82005-269"><dt>**\_identificador de \_ \_ perfil actual de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-269"><dt>**FWPM\_CONDITION\_CURRENT\_PROFILE\_ID**</dt></span></span> </dl>                                             | <span data-ttu-id="82005-270">Categoría de red de la interfaz de llegada o de próximo salto a través de la cual se crea el paquete actual (entrante o saliente).</span><span class="sxs-lookup"><span data-stu-id="82005-270">The network category of the arrival or next-hop interface through which the current packet (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="82005-271">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-271">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <span data-ttu-id="82005-272"><dt>**condición FWPM identificador de Perfil de la \_ \_ \_ interfaz local \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-272"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>                    | <span data-ttu-id="82005-273">Categoría de red de la interfaz de entrega.</span><span class="sxs-lookup"><span data-stu-id="82005-273">The network category of the delivery interface.</span></span><br/> <span data-ttu-id="82005-274">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-274">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <span data-ttu-id="82005-275"><dt>**\_identificador de \_ Perfil de interfaz de llegada de condición de \_ \_ FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-275"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="82005-276">Categoría de red de la interfaz de llegada.</span><span class="sxs-lookup"><span data-stu-id="82005-276">The network category of the arrival interface.</span></span><br/> <span data-ttu-id="82005-277">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-277">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <span data-ttu-id="82005-278"><dt>**identificador de Perfil de la \_ \_ interfaz NEXTHOP Condition \_ \_ FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-278"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="82005-279">Categoría de red de la interfaz de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="82005-279">The network category of the next-hop interface.</span></span><br/> <span data-ttu-id="82005-280">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-280">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <span data-ttu-id="82005-281"><dt>**\_motivo de \_ reautorización de la condición FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-281"><dt>**FWPM\_CONDITION\_REAUTHORIZE\_REASON**</dt></span></span> </dl>                                              | <span data-ttu-id="82005-282">Motivo por el que se va a autorizar a una conexión previamente autorizada.</span><span class="sxs-lookup"><span data-stu-id="82005-282">The reason for reauthorizing a previously authorized connection.</span></span><br/> <span data-ttu-id="82005-283">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-283">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <span data-ttu-id="82005-284"><dt>**\_motivo de \_ \_ reautenticación de \_ Ale de FWPM condicional**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-284"><dt>**FWPM\_CONDITION\_ALE\_REAUTH\_REASON**</dt></span></span> </dl>                                                | <span data-ttu-id="82005-285">La razón para reautorizar una conexión previamente autorizada, como **FWP \_ Condition \_ reautorice el \_ \_ \_ cambio** de la Directiva de motivo (o uno de los otros valores enumerados en [**marcas de condición de filtrado**](filtering-condition-flags-.md)).</span><span class="sxs-lookup"><span data-stu-id="82005-285">The reason for reauthorizing a previously authorized connection, such as **FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE** (or one of the other values listed in [**Filtering Condition Flags**](filtering-condition-flags-.md)).</span></span><br/> <span data-ttu-id="82005-286">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-286">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <span data-ttu-id="82005-287"><dt>**\_tipo de \_ \_ ICMP original de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-287"><dt>**FWPM\_CONDITION\_ORIGINAL\_ICMP\_TYPE**</dt></span></span> </dl>                                             | <span data-ttu-id="82005-288">Tipo de ICMP con el que se creó el flujo.</span><span class="sxs-lookup"><span data-stu-id="82005-288">The ICMP type with which the flow was created.</span></span><br/> <span data-ttu-id="82005-289">**Tipo de datos:** FWP \_ UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-289">**Data type:** FWP\_UINT16</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <span data-ttu-id="82005-290"><dt>**\_interfaz de \_ \_ llegada física \_ IP \_ de condición FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-290"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="82005-291">LUID de la interfaz física asociada a la dirección IP de llegada.</span><span class="sxs-lookup"><span data-stu-id="82005-291">The LUID of the physical interface associated with the arrival IP address.</span></span><br/> <span data-ttu-id="82005-292">**Tipo de datos:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="82005-292">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <span data-ttu-id="82005-293"><dt>**\_interfaz de \_ \_ NEXTHOP física \_ IP \_ de condición FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-293"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="82005-294">LUID de la interfaz física del próximo salto.</span><span class="sxs-lookup"><span data-stu-id="82005-294">The LUID of the physical interface of the next hop.</span></span><br/> <span data-ttu-id="82005-295">**Tipo de datos:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="82005-295">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <span data-ttu-id="82005-296"><dt>**\_tiempo de \_ cuarentena de interfaz de condición FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-296"><dt>**FWPM\_CONDITION\_INTERFACE\_QUARANTINE\_EPOCH**</dt></span></span> </dl>                     | <span data-ttu-id="82005-297">El número de tiempo asociado a una interfaz.</span><span class="sxs-lookup"><span data-stu-id="82005-297">The epoch count associated with an interface.</span></span> <span data-ttu-id="82005-298">Reservado.</span><span class="sxs-lookup"><span data-stu-id="82005-298">Reserved.</span></span><br/> <span data-ttu-id="82005-299">**Tipo de datos:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="82005-299">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <span data-ttu-id="82005-300"><dt>**\_propiedad de \_ \_ socket de \_ Firewall \_ de la condición Ale FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-300"><dt>**FWPM\_CONDITION\_ALE\_SIO\_FIREWALL\_SOCKET\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="82005-301">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="82005-301">Reserved for internal use.</span></span> <br/> <span data-ttu-id="82005-302">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-302">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                              |





| <span data-ttu-id="82005-303">Constantes disponibles para Windows Vista con SP1, Windows Server 2008 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="82005-303">Constants available for Windows Vista with SP1, Windows Server 2008, and later</span></span>                                                                                                                                                                           | <span data-ttu-id="82005-304">Descripción</span><span class="sxs-lookup"><span data-stu-id="82005-304">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <span data-ttu-id="82005-305"><dt>**\_interfaz de \_ llegada de IP de condición FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-305"><dt>**FWPM\_CONDITION\_IP\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>                       | <span data-ttu-id="82005-306">LUID para la interfaz de red asociada con la dirección IP de llegada.</span><span class="sxs-lookup"><span data-stu-id="82005-306">The LUID for the network interface associated with the arrival IP address.</span></span> <br/> <span data-ttu-id="82005-307">**Tipo de datos:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="82005-307">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <span data-ttu-id="82005-308"><dt>**\_tipo de \_ interfaz de llegada de condición de FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-308"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                 | <span data-ttu-id="82005-309">El tipo de la interfaz de red de llegada tal y como se define en la autoridad de nombres asignados (IANA) de Internet.</span><span class="sxs-lookup"><span data-stu-id="82005-309">The type of the arrival network interface as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="82005-310">Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="82005-310">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="82005-311">**Valores posibles:** Los valores de tipo de interfaz enumerados en el archivo de encabezado Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="82005-311">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="82005-312">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-312">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <span data-ttu-id="82005-313"><dt>**FWPM \_ \_tipo de \_ túnel \_ de llegada de condición**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-313"><dt> **FWPM\_CONDITION\_ARRIVAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="82005-314">Método de encapsulación utilizado por un túnel asociado a la interfaz de red de llegada si el miembro de tipo es si es un \_ túnel de tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="82005-314">The encapsulation method used by a tunnel associated with the arrival network interface if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="82005-315">La autoridad de nombres asignados de Internet (IANA) define el tipo de túnel.</span><span class="sxs-lookup"><span data-stu-id="82005-315">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="82005-316">Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="82005-316">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="82005-317">**Valores posibles:** Los \_ valores de tipo de la enumeración de tipo de túnel enumerados en el archivo de encabezado ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="82005-317">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="82005-318">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-318">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <span data-ttu-id="82005-319"><dt>**\_Índice de \_ interfaz de llegada de condición de FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-319"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_INDEX**</dt></span></span> </dl>              | <span data-ttu-id="82005-320">Índice de la interfaz de red de llegada, tal y como se enumera en la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-320">The index of the arrival network interface, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="82005-321">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-321">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <span data-ttu-id="82005-322"><dt>**\_Índice de \_ \_ \_ subinterfaz de llegada de condición \_ de FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-322"><dt>**FWPM\_CONDITION\_ARRIVAL\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl> | <span data-ttu-id="82005-323">Índice de la interfaz de red de llegada, tal y como se enumera en la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-323">The index of the arrival network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="82005-324">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-324">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <span data-ttu-id="82005-325"><dt>**\_Índice de \_ \_ interfaz local de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-325"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_INDEX**</dt></span></span> </dl>                    | <span data-ttu-id="82005-326">Índice de la interfaz de red, tal y como lo enumera la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-326">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="82005-327">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-327">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <span data-ttu-id="82005-328"><dt>**\_tipo de \_ \_ interfaz local de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-328"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="82005-329">El tipo de interfaz definido por la autoridad de nombres asignados (IANA) de Internet.</span><span class="sxs-lookup"><span data-stu-id="82005-329">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="82005-330">Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="82005-330">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="82005-331">**Valores posibles:** Los valores de tipo de interfaz enumerados en el archivo de encabezado Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="82005-331">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="82005-332">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-332">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <span data-ttu-id="82005-333"><dt>**\_tipo de \_ \_ túnel local de condición \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-333"><dt>**FWPM\_CONDITION\_LOCAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                                | <span data-ttu-id="82005-334">Método de encapsulación utilizado por un túnel si el miembro de tipo es si es un \_ túnel de tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="82005-334">The encapsulation method used by a tunnel if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="82005-335">La autoridad de nombres asignados de Internet (IANA) define el tipo de túnel.</span><span class="sxs-lookup"><span data-stu-id="82005-335">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="82005-336">Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="82005-336">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="82005-337">**Valores posibles:** Los \_ valores de tipo de la enumeración de tipo de túnel enumerados en el archivo de encabezado ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="82005-337">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="82005-338">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-338">**Data type:** FWP\_UINT32</span></span> <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="82005-339">Constantes disponibles para Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="82005-339">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="82005-340">Descripción</span><span class="sxs-lookup"><span data-stu-id="82005-340">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <span data-ttu-id="82005-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-342">Dirección IP local.</span><span class="sxs-lookup"><span data-stu-id="82005-342">The local IP address.</span></span> <br/> <span data-ttu-id="82005-343"><strong>Tipo de datos:</strong> Para una dirección IPv4</span><span class="sxs-lookup"><span data-stu-id="82005-343"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="82005-344">FWP_V4_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-344">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-345">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-345">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-346"><strong>Tipo de datos:</strong> Para una dirección IPv6</span><span class="sxs-lookup"><span data-stu-id="82005-346"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="82005-347">FWP_V6_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-347">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-348">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-348">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <span data-ttu-id="82005-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-350">Dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="82005-350">The remote IP address.</span></span> <br/> <span data-ttu-id="82005-351"><strong>Tipo de datos:</strong> Para una dirección IPv4</span><span class="sxs-lookup"><span data-stu-id="82005-351"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="82005-352">FWP_V4_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-352">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-353">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-353">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-354"><strong>Tipo de datos:</strong> Para una dirección IPv6</span><span class="sxs-lookup"><span data-stu-id="82005-354"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="82005-355">FWP_V6_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-355">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-356">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-356">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <span data-ttu-id="82005-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-358">La dirección IP de origen para los paquetes reenviados.</span><span class="sxs-lookup"><span data-stu-id="82005-358">The source IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="82005-359"><strong>Tipo de datos:</strong> Para una dirección IPv4</span><span class="sxs-lookup"><span data-stu-id="82005-359"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="82005-360">FWP_V4_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-360">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-361">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-361">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-362"><strong>Tipo de datos:</strong> Para una dirección IPv6</span><span class="sxs-lookup"><span data-stu-id="82005-362"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="82005-363">FWP_V6_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-363">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-364">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-364">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <span data-ttu-id="82005-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-366">La dirección IP de destino para los paquetes reenviados.</span><span class="sxs-lookup"><span data-stu-id="82005-366">The destination IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="82005-367"><strong>Tipo de datos:</strong> Para una dirección IPv4</span><span class="sxs-lookup"><span data-stu-id="82005-367"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="82005-368">FWP_V4_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-368">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-369">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-369">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-370"><strong>Tipo de datos:</strong> Para una dirección IPv6</span><span class="sxs-lookup"><span data-stu-id="82005-370"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="82005-371">FWP_V6_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-371">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-372">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-372">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <span data-ttu-id="82005-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-374">Tipo de dirección IP local.</span><span class="sxs-lookup"><span data-stu-id="82005-374">The local IP address type.</span></span> <br/> <span data-ttu-id="82005-375"><strong>Valores posibles:</strong> Cualquiera de los siguientes valores de enumeración de <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> .</span><span class="sxs-lookup"><span data-stu-id="82005-375"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="82005-376">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="82005-376">NlatUnspecified</span></span></li>
<li><span data-ttu-id="82005-377">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="82005-377">NlatUnicast</span></span></li>
<li><span data-ttu-id="82005-378">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="82005-378">NlatAnycast</span></span></li>
<li><span data-ttu-id="82005-379">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="82005-379">NlatMulticast</span></span></li>
<li><span data-ttu-id="82005-380">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="82005-380">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-381"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-381"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <span data-ttu-id="82005-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-383">El tipo de dirección IP de destino para los paquetes reenviados.</span><span class="sxs-lookup"><span data-stu-id="82005-383">The destination IP address type for forwarded packets.</span></span> <br/> <span data-ttu-id="82005-384"><strong>Valores posibles:</strong> Cualquiera de los siguientes valores de enumeración de <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> .</span><span class="sxs-lookup"><span data-stu-id="82005-384"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="82005-385">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="82005-385">NlatUnspecified</span></span></li>
<li><span data-ttu-id="82005-386">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="82005-386">NlatUnicast</span></span></li>
<li><span data-ttu-id="82005-387">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="82005-387">NlatAnycast</span></span></li>
<li><span data-ttu-id="82005-388">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="82005-388">NlatMulticast</span></span></li>
<li><span data-ttu-id="82005-389">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="82005-389">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-390"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-390"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <span data-ttu-id="82005-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-392">LUID para la interfaz de red asociada con la dirección IP local.</span><span class="sxs-lookup"><span data-stu-id="82005-392">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="82005-393"><strong>Tipo de datos:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="82005-393"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <span data-ttu-id="82005-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-395">El tipo de interfaz definido por la autoridad de nombres asignados (IANA) de Internet.</span><span class="sxs-lookup"><span data-stu-id="82005-395">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="82005-396">Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="82005-396">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="82005-397"><strong>Valores posibles:</strong> Los valores de tipo de interfaz enumerados en el archivo de encabezado Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="82005-397"><strong>Possible values:</strong> The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="82005-398"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-398"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <span data-ttu-id="82005-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-400">Método de encapsulación utilizado por un túnel si el miembro de tipo es IF_TYPE_TUNNEL.</span><span class="sxs-lookup"><span data-stu-id="82005-400">The encapsulation method used by a tunnel if the Type member is IF_TYPE_TUNNEL.</span></span> <span data-ttu-id="82005-401">La autoridad de nombres asignados de Internet (IANA) define el tipo de túnel.</span><span class="sxs-lookup"><span data-stu-id="82005-401">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="82005-402">Para más información, consulte <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span><span class="sxs-lookup"><span data-stu-id="82005-402">For more information, see <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span></span> <br/> <span data-ttu-id="82005-403"><strong>Valores posibles:</strong> Los valores de tipo de enumeración TUNNEL_TYPE enumerados en el archivo de encabezado ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="82005-403"><strong>Possible values:</strong> The TUNNEL_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="82005-404"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-404"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <span data-ttu-id="82005-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-406">El LUID de la interfaz de red en la que se va a enviar el paquete que se va a reenviar.</span><span class="sxs-lookup"><span data-stu-id="82005-406">The LUID for the network interface on which the packet being forwarded is to be sent out.</span></span> <br/> <span data-ttu-id="82005-407"><strong>Tipo de datos:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="82005-407"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <span data-ttu-id="82005-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-409">Número de protocolo IP, tal y como se especifica en RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="82005-409">The IP protocol number, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="82005-410"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-410"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <span data-ttu-id="82005-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-412">El número de puerto del Protocolo de transporte local.</span><span class="sxs-lookup"><span data-stu-id="82005-412">The local transport protocol port number.</span></span><br/> <span data-ttu-id="82005-413"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-413"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <span data-ttu-id="82005-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-415">Campo de tipo ICMP, tal y como se especifica en RFC 792.</span><span class="sxs-lookup"><span data-stu-id="82005-415">The ICMP type field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="82005-416"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-416"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <span data-ttu-id="82005-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-418">Número de puerto del Protocolo de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="82005-418">The remote transport protocol port number.</span></span> <br/> <span data-ttu-id="82005-419"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-419"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <span data-ttu-id="82005-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-421">El campo de Código ICMP, tal como se especifica en RFC 792.</span><span class="sxs-lookup"><span data-stu-id="82005-421">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="82005-422"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-422"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <span data-ttu-id="82005-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-424">Tipo de dirección IP local que está incrustado en el paquete ICMP.</span><span class="sxs-lookup"><span data-stu-id="82005-424">The local IP address type that is embedded in the ICMP packet.</span></span><br/> <span data-ttu-id="82005-425"><strong>Valores posibles:</strong> Cualquiera de los siguientes valores de enumeración de <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> .</span><span class="sxs-lookup"><span data-stu-id="82005-425"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="82005-426">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="82005-426">NlatUnspecified</span></span></li>
<li><span data-ttu-id="82005-427">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="82005-427">NlatUnicast</span></span></li>
<li><span data-ttu-id="82005-428">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="82005-428">NlatAnycast</span></span></li>
<li><span data-ttu-id="82005-429">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="82005-429">NlatMulticast</span></span></li>
<li><span data-ttu-id="82005-430">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="82005-430">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-431"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-431"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <span data-ttu-id="82005-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-433">La dirección IP remota que está incrustada en el paquete ICMP.</span><span class="sxs-lookup"><span data-stu-id="82005-433">The remote IP address that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="82005-434"><strong>Tipo de datos:</strong> Para una dirección IPv4</span><span class="sxs-lookup"><span data-stu-id="82005-434"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="82005-435">FWP_V4_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-435">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-436">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-436">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-437"><strong>Tipo de datos:</strong> Para una dirección IPv6</span><span class="sxs-lookup"><span data-stu-id="82005-437"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="82005-438">FWP_V6_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-438">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-439">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-439">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <span data-ttu-id="82005-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-441">Número de protocolo IP que se inserta en el paquete ICMP, tal como se especifica en RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="82005-441">The IP protocol number that is embedded in the ICMP packet, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="82005-442"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-442"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <span data-ttu-id="82005-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-444">El número de puerto del Protocolo de transporte local que está incrustado en el paquete ICMP.</span><span class="sxs-lookup"><span data-stu-id="82005-444">The local transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="82005-445"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-445"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <span data-ttu-id="82005-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-447">Número de puerto del Protocolo de transporte remoto que está incrustado en el paquete ICMP.</span><span class="sxs-lookup"><span data-stu-id="82005-447">The remote transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="82005-448"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-448"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <span data-ttu-id="82005-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-450">Una operación OR bit a bit de una combinación de marcas de condición de filtrado.</span><span class="sxs-lookup"><span data-stu-id="82005-450">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="82005-451"><strong>Valores posibles:</strong> Consulte <a href="filtering-condition-flags-.md"> <strong>marcas de condición de filtrado</strong></a></span><span class="sxs-lookup"><span data-stu-id="82005-451"><strong>Possible values:</strong> See <a href="filtering-condition-flags-.md"><strong>Filtering Condition Flags</strong></a></span></span><br/> <span data-ttu-id="82005-452"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-452"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <span data-ttu-id="82005-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-454">Dirección del flujo de datos o tráfico.</span><span class="sxs-lookup"><span data-stu-id="82005-454">The direction of the traffic or data flow.</span></span> <br/> <span data-ttu-id="82005-455"><strong>Valores posibles:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-455"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-456">FWP_DIRECTION_INBOUND</span><span class="sxs-lookup"><span data-stu-id="82005-456">FWP_DIRECTION_INBOUND</span></span></li>
<li><span data-ttu-id="82005-457">FWP_DIRECTION_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="82005-457">FWP_DIRECTION_OUTBOUND</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-458">En el caso de las capas de datagrama (FWPM_LAYER_DATAGRAM_DATA_ *) y las capas de paquetes de secuencias (FWPM_LAYER_STREAM_PACKET_*), el valor será el mismo que el de la dirección del paquete.</span><span class="sxs-lookup"><span data-stu-id="82005-458">For datagram layers (FWPM_LAYER_DATAGRAM_DATA_ *) and stream packet layers (FWPM_LAYER_STREAM_PACKET_*), the value will be the same as the direction of the packet.</span></span> <br/> <span data-ttu-id="82005-459">En el caso de los niveles de secuencia (FWPM_LAYER_STREAM_ *) y los niveles establecidos de Flow (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), el valor será el mismo que la dirección de la conexión.</span><span class="sxs-lookup"><span data-stu-id="82005-459">For stream layers (FWPM_LAYER_STREAM_ *) and flow established layers (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), the value will be the same as direction of the connection.</span></span> <span data-ttu-id="82005-460">(Por ejemplo, cuando una aplicación local inicia la conexión, un paquete entrante tiene <strong>FWPM_CONDITION_DIRECTION</strong> establecido en <strong>FWP_DIRECTION_OUTBOUND</strong>).</span><span class="sxs-lookup"><span data-stu-id="82005-460">(For example, when a local application initiates the connection, an inbound packet has <strong>FWPM_CONDITION_DIRECTION</strong> set to <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span></span> <br/> <span data-ttu-id="82005-461"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-461"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <span data-ttu-id="82005-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-463">Índice de la interfaz de red, tal y como lo enumera la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-463">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="82005-464"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-464"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <span data-ttu-id="82005-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-466">Índice de la interfaz de red lógica, tal y como se enumera en la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-466">The index of the logical network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="82005-467"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-467"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <span data-ttu-id="82005-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-469">Índice de la interfaz de red de origen para los paquetes reenviados, tal y como se enumera en la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-469">The index of the source network interface for forwarded packets, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="82005-470"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-470"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <span data-ttu-id="82005-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-472">Índice de la interfaz de red lógica de origen para los paquetes reenviados, tal y como se enumera en la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-472">The index of the source logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="82005-473"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-473"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <span data-ttu-id="82005-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-475">Índice de la interfaz de red de destino para los paquetes reenviados, tal y como se enumera en la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-475">The index of the destination network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="82005-476"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-476"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <span data-ttu-id="82005-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-478">Índice de la interfaz de red lógica de destino para los paquetes reenviados, tal y como se enumera en la pila de red.</span><span class="sxs-lookup"><span data-stu-id="82005-478">The index of the destination logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="82005-479"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-479"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <span data-ttu-id="82005-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-481">La ruta de acceso completa del dispositivo de la aplicación, tal como la devuelve la función <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="82005-481">The fully qualified device path of the application, as returned by the <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> function.</span></span> <br/> <span data-ttu-id="82005-482">(Por ejemplo, &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; ).</span><span class="sxs-lookup"><span data-stu-id="82005-482">(For example, &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.)</span></span><br/> <span data-ttu-id="82005-483"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-483"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <span data-ttu-id="82005-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-485">La identificación del usuario local.</span><span class="sxs-lookup"><span data-stu-id="82005-485">The identification of the local user.</span></span> <br/> <span data-ttu-id="82005-486"><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-486"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <span data-ttu-id="82005-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-488">La identificación del usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="82005-488">The identification of the remote user.</span></span> <br/> <span data-ttu-id="82005-489"><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-489"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <span data-ttu-id="82005-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-491">La identificación de la máquina remota.</span><span class="sxs-lookup"><span data-stu-id="82005-491">The identification of the remote machine.</span></span> <br/> <span data-ttu-id="82005-492"><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-492"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <span data-ttu-id="82005-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-494">Modo de socket sin formato permitido o denegado.</span><span class="sxs-lookup"><span data-stu-id="82005-494">The raw socket mode that is allowed or denied.</span></span><br/> <span data-ttu-id="82005-495"><strong>Valores posibles:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-495"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-496">SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="82005-496">SIO_RCVALL</span></span></li>
<li><span data-ttu-id="82005-497">SIO_RCVALL_IGMPMCAST</span><span class="sxs-lookup"><span data-stu-id="82005-497">SIO_RCVALL_IGMPMCAST</span></span></li>
<li><span data-ttu-id="82005-498">SIO_RCVALL_MCAST</span><span class="sxs-lookup"><span data-stu-id="82005-498">SIO_RCVALL_MCAST</span></span></li>
</ul>
<span data-ttu-id="82005-499">Para obtener una descripción de estos modos de socket sin formato, vea la función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="82005-499">For a description of these raw socket modes, see the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> function.</span></span><br/> <span data-ttu-id="82005-500"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-500"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <span data-ttu-id="82005-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-502">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="82005-502">Reserved for internal use.</span></span> <br/> <span data-ttu-id="82005-503"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-503"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <span data-ttu-id="82005-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-505">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="82005-505">Reserved for internal use.</span></span> <br/> <span data-ttu-id="82005-506"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-506"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="82005-507">Las constantes siguientes solo están disponibles para el modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="82005-507">The following constants are available for user mode only.</span></span>



| <span data-ttu-id="82005-508">Condiciones de modo de usuario disponibles para Windows 8 y Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="82005-508">User-mode conditions available for Windows 8 and Windows Server 2012</span></span>                                                                                                                       | <span data-ttu-id="82005-509">Descripción</span><span class="sxs-lookup"><span data-stu-id="82005-509">Description</span></span>                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <span data-ttu-id="82005-510"><dt>**modo de FWPM \_ condición de \_ QM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82005-510"><dt>**FWPM\_CONDITION\_QM\_MODE**</dt></span></span> </dl> | <span data-ttu-id="82005-511">El modo del filtro de modo rápido (QM).</span><span class="sxs-lookup"><span data-stu-id="82005-511">The mode of the quick mode (QM) filter.</span></span> <span data-ttu-id="82005-512">Consulte [**\_ \_ tipo de tráfico de IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) para ver los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="82005-512">See [**IPSEC\_TRAFFIC\_TYPE**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) for possible values.</span></span><br/> <span data-ttu-id="82005-513">**Tipo de datos:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-513">**Data type:** FWP\_UINT32</span></span><br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="82005-514">Condiciones de modo de usuario disponibles para Windows 7, Windows Server 2008 R2 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="82005-514">User-mode conditions available for Windows 7, Windows Server 2008 R2, and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="82005-515">Descripción</span><span class="sxs-lookup"><span data-stu-id="82005-515">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <span data-ttu-id="82005-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-517">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="82005-517">Reserved for internal use.</span></span><br/> <span data-ttu-id="82005-518"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-518"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <span data-ttu-id="82005-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-520">Nombre del elemento del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="82005-520">The name of the peer.</span></span> <span data-ttu-id="82005-521">Por ejemplo, el nombre DNS del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="82005-521">For example, the peer's DNS name.</span></span><br/> <span data-ttu-id="82005-522"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-522"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <span data-ttu-id="82005-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-524">Identidad de la entidad de seguridad de autenticación remota.</span><span class="sxs-lookup"><span data-stu-id="82005-524">The identity of the remote authentication principal.</span></span> <br/> <span data-ttu-id="82005-525"><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-525"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="82005-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-527">El tipo de método de autenticación IKE, IKEv2 o AuthIP.</span><span class="sxs-lookup"><span data-stu-id="82005-527">The type of IKE, IKEv2, or AuthIP authentication method.</span></span> <br/> <span data-ttu-id="82005-528"><strong>Tipo de datos:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-528"><strong>Data type:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <span data-ttu-id="82005-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-530">El tipo de módulo de creación de claves.</span><span class="sxs-lookup"><span data-stu-id="82005-530">The type of keying module.</span></span><br/> <span data-ttu-id="82005-531"><strong>Tipo de datos:</strong> IKEEXT_KEY_MODULE_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-531"><strong>Data type:</strong> IKEEXT_KEY_MODULE_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <span data-ttu-id="82005-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-533">Modo IPsec en el que se puede obtener un token.</span><span class="sxs-lookup"><span data-stu-id="82005-533">The IPsec mode in which a token can be obtained.</span></span><br/> <span data-ttu-id="82005-534"><strong>Tipo de datos:</strong> IPSEC_TOKEN_MODE</span><span class="sxs-lookup"><span data-stu-id="82005-534"><strong>Data type:</strong> IPSEC_TOKEN_MODE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <span data-ttu-id="82005-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-536">La clave de contexto del proveedor de directivas de modo principal (MM) o modo rápido (QM) de la SA que se está autorizando.</span><span class="sxs-lookup"><span data-stu-id="82005-536">The main mode (MM) or quick mode (QM) policy provider context key of the SA being authorized.</span></span> <span data-ttu-id="82005-537">Resulta útil para restringir el ámbito de la regla de autorización a una SAs formada mediante una clave de directiva IPsec MM o QM especificada.</span><span class="sxs-lookup"><span data-stu-id="82005-537">Useful for restricting the scope of the authorization rule to SAs formed using a specified IPsec MM or QM policy key.</span></span><br/> <span data-ttu-id="82005-538"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-538"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="82005-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-540">Método utilizado para autenticar la Asociación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="82005-540">The method used to authenticate the security association.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="82005-541">Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="82005-541">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="82005-542"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-542"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
</tbody>
</table>





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="82005-543">Constantes disponibles para Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="82005-543">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="82005-544">Descripción</span><span class="sxs-lookup"><span data-stu-id="82005-544">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <span data-ttu-id="82005-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-546">La identificación del usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="82005-546">The identification of the remote user.</span></span><br/> <span data-ttu-id="82005-547"><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-547"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <span data-ttu-id="82005-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-549">UUID de la interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="82005-549">The UUID of the RPC interface.</span></span> <br/> <span data-ttu-id="82005-550"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-550"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <span data-ttu-id="82005-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-552">Versión de la interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="82005-552">The version of the RPC interface.</span></span> <br/> <span data-ttu-id="82005-553"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-553"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <span data-ttu-id="82005-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-555">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="82005-555">Reserved for internal use.</span></span> <br/> <span data-ttu-id="82005-556"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-556"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <span data-ttu-id="82005-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-558">La identificación de la aplicación COM.</span><span class="sxs-lookup"><span data-stu-id="82005-558">The identification of the COM application.</span></span><br/> <span data-ttu-id="82005-559"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-559"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <span data-ttu-id="82005-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-561">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82005-561">The name of the application.</span></span><br/> <span data-ttu-id="82005-562"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-562"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <span data-ttu-id="82005-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-564">El protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="82005-564">The RPC protocol.</span></span> <br/> <span data-ttu-id="82005-565"><strong>Valores posibles:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-565"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-566">RPC_PROTSEQ_TCP</span><span class="sxs-lookup"><span data-stu-id="82005-566">RPC_PROTSEQ_TCP</span></span></li>
<li><span data-ttu-id="82005-567">RPC_PROTSEQ_NMP</span><span class="sxs-lookup"><span data-stu-id="82005-567">RPC_PROTSEQ_NMP</span></span></li>
<li><span data-ttu-id="82005-568">RPC_PROTSEQ_LRPC</span><span class="sxs-lookup"><span data-stu-id="82005-568">RPC_PROTSEQ_LRPC</span></span></li>
<li><span data-ttu-id="82005-569">RPC_PROTSEQ_HTTP</span><span class="sxs-lookup"><span data-stu-id="82005-569">RPC_PROTSEQ_HTTP</span></span></li>
</ul>
<br/> <span data-ttu-id="82005-570"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-570"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <span data-ttu-id="82005-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-572">El tipo de servicio de autenticación.</span><span class="sxs-lookup"><span data-stu-id="82005-572">The authentication service type.</span></span> <span data-ttu-id="82005-573">Para obtener más información sobre los tipos de servicio de autenticación, vea <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service constantes</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="82005-573">For more information about authentication service types, see <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service Constants</strong></a>.</span></span> <br/> <span data-ttu-id="82005-574"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-574"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <span data-ttu-id="82005-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-576">Nivel de servicio de autenticación.</span><span class="sxs-lookup"><span data-stu-id="82005-576">The authentication service level.</span></span> <span data-ttu-id="82005-577">Para obtener más información sobre los niveles de servicio de autenticación, consulte <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>constantes de nivel de autenticación</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="82005-577">For more information about authentication service levels, see <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Authentication-Level Constants</strong></a>.</span></span> <br/> <span data-ttu-id="82005-578"><strong>Tipo de datos:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="82005-578"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <span data-ttu-id="82005-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-580">Algoritmo de cifrado de la interfaz del proveedor de servicios de seguridad (SSPI) basado en certificados.</span><span class="sxs-lookup"><span data-stu-id="82005-580">The certificate based Security Service Provider Interface (SSPI) encryption algorithm.</span></span><br/> <span data-ttu-id="82005-581"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-581"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <span data-ttu-id="82005-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-583">Tamaño de la clave de cifrado SSPI basada en el certificado.</span><span class="sxs-lookup"><span data-stu-id="82005-583">The certificate based SSPI encryption key size.</span></span><br/> <span data-ttu-id="82005-584"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-584"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <span data-ttu-id="82005-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-586">Dirección IPv4 local.</span><span class="sxs-lookup"><span data-stu-id="82005-586">The local IPv4 address.</span></span> <br/> <span data-ttu-id="82005-587"><strong>Tipo de datos:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-587"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-588">FWP_V4_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-588">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-589">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-589">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <span data-ttu-id="82005-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-591">Dirección IPv6 local.</span><span class="sxs-lookup"><span data-stu-id="82005-591">The local IPv6 address.</span></span> <br/> <span data-ttu-id="82005-592"><strong>Tipo de datos:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-592"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-593">FWP_V6_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-593">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-594">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-594">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <span data-ttu-id="82005-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-596">Dirección IPv4 remota.</span><span class="sxs-lookup"><span data-stu-id="82005-596">The remote IPv4 address.</span></span> <br/> <span data-ttu-id="82005-597"><strong>Tipo de datos:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-597"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-598">FWP_V4_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-598">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-599">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-599">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <span data-ttu-id="82005-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-601">Dirección IPv6 remota.</span><span class="sxs-lookup"><span data-stu-id="82005-601">The remote IPv6 address.</span></span> <br/> <span data-ttu-id="82005-602"><strong>Tipo de datos:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="82005-602"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="82005-603">FWP_V6_ADDR_MASK, o</span><span class="sxs-lookup"><span data-stu-id="82005-603">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="82005-604">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-604">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <span data-ttu-id="82005-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-606">Nombre de la canalización con nombre remota.</span><span class="sxs-lookup"><span data-stu-id="82005-606">The name of the remote named pipe.</span></span><br/> <span data-ttu-id="82005-607"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-607"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <span data-ttu-id="82005-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-609">UUID del proceso con la interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="82005-609">The UUID of the process with the RPC interface.</span></span><br/> <span data-ttu-id="82005-610"><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-610"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <span data-ttu-id="82005-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-612">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="82005-612">Reserved for internal use.</span></span><br/> <span data-ttu-id="82005-613"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-613"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <span data-ttu-id="82005-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-615">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="82005-615">Reserved for internal use.</span></span><br/> <span data-ttu-id="82005-616"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-616"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <span data-ttu-id="82005-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-618">La identificación del cliente al usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="82005-618">The identification of the client when using RpcProxy.</span></span><br/> <span data-ttu-id="82005-619"><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-619"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <span data-ttu-id="82005-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-621">Nombre del servidor RPC al usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="82005-621">The name of the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="82005-622"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-622"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <span data-ttu-id="82005-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-624">El puerto en el servidor RPC al usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="82005-624">The port on the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="82005-625"><strong>Tipo de datos:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="82005-625"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <span data-ttu-id="82005-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-627">El tipo de servicio de autenticación del proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="82005-627">The RPC proxy authentication service type.</span></span><br/> <span data-ttu-id="82005-628"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-628"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <span data-ttu-id="82005-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-630">La longitud de la clave de capa de sockets seguros (SSL) en el certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="82005-630">The Secure Socket Layer (SSL) key length in the client certificate.</span></span><br/> <span data-ttu-id="82005-631"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-631"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <span data-ttu-id="82005-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-633">Identificador de objeto en el certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="82005-633">The object identifier in the client certificate.</span></span><br/> <span data-ttu-id="82005-634"><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="82005-634"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <span data-ttu-id="82005-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82005-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="82005-636">El tipo de evento de net.</span><span class="sxs-lookup"><span data-stu-id="82005-636">The type of net event.</span></span><br/> <span data-ttu-id="82005-637"><strong>Tipo de datos:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="82005-637"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="82005-638">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82005-638">Remarks</span></span>

<span data-ttu-id="82005-639">Cuando las direcciones IP se almacenan en \_ formato FWP UINT32 o cuando un puerto IP se almacena en \_ formato FWP UINT16, se almacenan en el orden del host, no en el orden de red.</span><span class="sxs-lookup"><span data-stu-id="82005-639">When IP addresses are stored in FWP\_UINT32 format or when an IP port is stored in FWP\_UINT16 format, they are stored in host-order, not network-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="82005-640">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82005-640">Requirements</span></span>



| <span data-ttu-id="82005-641">Requisito</span><span class="sxs-lookup"><span data-stu-id="82005-641">Requirement</span></span> | <span data-ttu-id="82005-642">Value</span><span class="sxs-lookup"><span data-stu-id="82005-642">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82005-643">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82005-643">Minimum supported client</span></span><br/> | <span data-ttu-id="82005-644">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="82005-644">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="82005-645">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82005-645">Minimum supported server</span></span><br/> | <span data-ttu-id="82005-646">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="82005-646">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="82005-647">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82005-647">Header</span></span><br/>                   | <dl> <span data-ttu-id="82005-648"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="82005-648"><dt>Fwpmu.h</dt></span></span> </dl> |
