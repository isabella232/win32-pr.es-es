---
title: Filtrar identificadores de condición (Fwpmu.h)
description: Los Windows de condición de filtrado de la Plataforma de filtrado de filtros (WFP) se representan mediante un GUID.
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
ms.openlocfilehash: f5c3823ed750637d595924eb47acc714403751eb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467982"
---
# <a name="filtering-condition-identifiers"></a>Filtrar identificadores de condición

Los Windows de condición de filtrado de la Plataforma de filtrado de filtros (WFP) se representan mediante un **GUID.** El tipo de datos para el valor de condición para cada condición de filtrado se especifica como [**UN TIPO DE DATOS \_ \_ FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Estos identificadores y sus tipos de datos se definen aquí.

Las condiciones estándar se enumeran en primer lugar, seguidas de las condiciones específicas del modo de usuario. Las condiciones se agrupan por sistema operativo compatible, por lo que puede saber fácilmente qué condiciones se admiten para un sistema operativo determinado.

> [!Note]  
> Cada una de las siguientes condiciones de filtrado solo está disponible en un subconjunto de las capas de filtrado de WFP. Para obtener más información sobre la disponibilidad de cada condición en cualquier capa determinada, vea Condiciones de filtrado [**disponibles en cada capa de filtrado.**](filtering-conditions-available-at-each-filtering-layer.md)

 




| Condiciones disponibles para Windows 8 y Windows Server 2012 | Descripción | 
|------------------------------------------------------------|-------------|
| <span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt></dl> | Dirección MAC de una interfaz local determinada.<br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE <br /> | 
| <span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt></dl> | Dirección de destino de un marco de entrada o dirección de origen de un marco de salida.<br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE<br /> | 
| <span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt></dl> | Dirección de origen de un marco de entrada o dirección de destino de un marco de salida.<br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE<br /> | 
| <span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt></dl> | Tipo de datos de carga de red Ethernet V2. (Vea ETHERNET_TYPE_IPV4, etc. en netiodef.h).<br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt></dl> | Los 16 bits del encabezado VLAN, incluidos los campos VID, CFI y Priority según el estándar 802.1q (consulte VLAN_TAG en netiodef.h para ver las posiciones de los campos de bits).<br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt></dl> | Identificador único de la red vSwitch. No se puede usar junto con VLAN_IDs.<br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt></dl> | Número de puerto del puerto NDIS.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt></dl> | Tipo de medio del puerto NDIS.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /><strong>Valores posibles:</strong> Cualquiera de los valores <strong>NDIS_MEDIUM</strong> enumeración. (Vea ntddndis.h). <br /> | 
| <span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt></dl> | Tipo de medio físico del puerto NDIS.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /><strong>Valores posibles:</strong> Cualquiera de los valores <strong>NDIS_PHYSICAL_MEDIUM</strong> enumeración. (Vea ntddndis.h). <br /> | 
| <span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt></dl> | OR bit a bit de una combinación de marcas de condición de filtrado. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /><strong>Valores posibles:  </strong><ul><li>FWP_CONDITION_L2_IS_MOBILE_BROADBAND</li><li>FWP_CONDITION_L2_IS_NATIVE_ETHERNET</li><li>FWP_CONDITION_L2_IS_WIFI</li><li>FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</li></ul><br /> | 
| <span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt></dl> | Tipo de dirección de la dirección local física.<br /><strong>Tipo de datos:</strong> FWP_UINT8<br /><strong>Valores posibles:</strong> Cualquiera de los siguientes valores <strong>DL_ADDRESS_TYPE</strong> enumeración.<ul><li>DlUnicast</li><li>DlMulticast</li><li>DlBroadcast</li></ul><br /> | 
| <span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt></dl> | Tipo de dirección de la dirección remota física.<br /><strong>Tipo de datos:</strong> FWP_UINT8<br /><strong>Valores posibles:</strong> Cualquiera de los siguientes valores <strong>DL_ADDRESS_TYPE</strong> enumeración.<ul><li>DlUnicast</li><li>DlMulticast</li><li>DlBroadcast</li></ul><br /> | 
| <span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt></dl> | Dirección de origen física de un marco.<br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE<br /> | 
| <span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt></dl> | Dirección de destino física de un marco.<br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY6_TYPE<br /> | 
| <span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt></dl> | Tipo de dirección de la dirección de destino física.<br /><strong>Tipo de datos:</strong> FWP_UINT8<br /><strong>Valores posibles:</strong> Cualquiera de los siguientes valores <strong>DL_ADDRESS_TYPE</strong> enumeración.<ul><li>DlUnicast</li><li>DlMulticast</li><li>DlBroadcast</li></ul><br /> | 
| <span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt></dl> | Tipo de dirección de la dirección de destino física.<br /><strong>Tipo de datos:</strong> FWP_UINT8<br /><strong>Valores posibles:</strong> Cualquiera de los siguientes valores <strong>DL_ADDRESS_TYPE</strong> enumeración.<ul><li>DlUnicast</li><li>DlMulticast</li><li>DlBroadcast</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt></dl> | Puerto de origen del transporte del paquete.<br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt></dl> | Campo de tipo ICMP, tal como se especifica en RFC 792.<br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt></dl> | Puerto de destino del transporte del paquete.<br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt></dl> | Campo de código ICMP, tal como se especifica en RFC 792. <br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt></dl> | Identificador único de una instancia de vSwitch.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt></dl> | Especifica si la instancia de vSwitch forma parte de una red virtual externa, interna o privada.<br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt></dl> | Identificador único del origen del paquete actual. (Nombre de una VM-NIC, P-NIC o V-NIC).<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt></dl> | Identificador único del destino del paquete actual. (Nombre de una VM-NIC, P-NIC o V-NIC).<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt></dl> | Identificador único de la máquina virtual de origen de vSwitch.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt></dl> | Identificador único de la máquina virtual de destino de vSwitch.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt></dl> | Tipo de interfaz del origen del paquete actual.<br /><strong>Tipo de datos:</strong> FWP_UINT8<br /><strong>Valores posibles:  </strong><ul><li>SwitchNicSyntheticNic (cuando el tipo de interfaz es VM-NIC)</li><li>SwitchNicEmulatedNic (cuando el tipo de interfaz es VM-NIC)</li><li>SwitchNicPhysicalNic (cuando el tipo de interfaz es P-NIC)</li><li>SwitchNicVNic (cuando el tipo de interfaz es V-NIC, conectado a la partición del host)</li></ul><br /> | 
| <span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt></dl> | Tipo de interfaz del destino del paquete actual.<br /><strong>Tipo de datos:</strong> FWP_UINT8<br /><strong>Valores posibles:  </strong><ul><li>SwitchNicSyntheticNic (cuando el tipo de interfaz es VM-NIC)</li><li>SwitchNicEmulatedNic (cuando el tipo de interfaz es VM-NIC)</li><li>SwitchNicPhysicalNic (cuando el tipo de interfaz es P-NIC)</li><li>SwitchNicVNic (cuando el tipo de interfaz es V-NIC, conectado a la partición del host)</li></ul><br /> | 
| <span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt></dl> | LUID de la interfaz de red asociada a la dirección IP local. <br /><strong>Tipo de datos:</strong> FWP_UINT64<br /> | 
| <span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt></dl> | Identificador de seguridad (SID) de un contenedor de aplicaciones.<br /><strong>Tipo de datos:</strong> FWP_SID<br /> | 
| <span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt></dl> | La ruta de acceso completa del dispositivo de la aplicación, como "\device0\hardiskvolume1\Program Files\Application.exe". Cuando se ha redirigido una conexión, este será el identificador de la aplicación de origen. De lo contrario, será igual que <strong>FWPM_CONDITION_ALE_APP_ID</strong>.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 






| Condiciones disponibles para Windows 7, Windows Server 2008 R2 y versiones posteriores                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <dt>**FWPM \_ CONDITION \_ IP \_ NEXTHOP \_ ADDRESS**</dt> </dl>                                             | Dirección IP de la interfaz de próximo salto.<br/> **Tipo de datos:** FWP \_ V4 \_ ADDR \_ MASK<br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <dt>**INTERFAZ \_ \_ NEXTHOP DE IP DE CONDICIÓN \_ \_ FWPM**</dt> </dl>                                       | Interfaz de próximo salto desde la que partirá el paquete. <br/> **Tipo de datos:** FWP \_ UINT64<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <dt>**FWPM \_ CONDITION \_ NEXTHOP \_ INTERFACE \_ TYPE**</dt> </dl>                                 | Tipo de interfaz de la interfaz de próximo salto.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <dt>**FWPM \_ CONDITION \_ NEXTHOP \_ TUNNEL \_ TYPE**</dt> </dl>                                          | Tipo de túnel de la interfaz de próximo salto.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <dt>**FWPM \_ CONDITION \_ NEXTHOP \_ INTERFACE \_ INDEX**</dt> </dl>                              | Índice de interfaz de la interfaz de próximo salto.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <dt>**FWPM \_ CONDITION \_ NEXTHOP \_ SUB \_ INTERFACE \_ INDEX**</dt> </dl>                 | Índice de la sub interface de la interfaz de próximo salto.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <dt>**ID. DE PERFIL \_ ORIGINAL DE \_ CONDICIÓN \_ \_ FWPM**</dt> </dl>                                          | Categoría de red de la interfaz de llegada o próximo salto a través de la cual se crea el flujo de ALE (entrante o saliente). <br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <dt>**ID. DE PERFIL \_ \_ ACTUAL DE CONDICIÓN \_ \_ FWPM**</dt> </dl>                                             | Categoría de red de la interfaz de llegada o próximo salto a través de la que se crea el paquete actual (entrante o saliente). <br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <dt>**ID. DE PERFIL \_ DE INTERFAZ LOCAL DE CONDICIÓN \_ \_ \_ \_ FWPM**</dt> </dl>                    | Categoría de red de la interfaz de entrega.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <dt>**ID. DE PERFIL \_ DE INTERFAZ DE LLEGADA DE \_ \_ \_ CONDICIÓN \_ FWPM**</dt> </dl>              | Categoría de red de la interfaz de llegada.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <dt>**FWPM \_ CONDITION \_ NEXTHOP \_ INTERFACE \_ PROFILE \_ ID**</dt> </dl>              | Categoría de red de la interfaz de próximo salto.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <dt>**MOTIVO DE \_ \_ LA REAUTORIZACIÓN DE LA CONDICIÓN \_ FWPM**</dt> </dl>                                              | El motivo para volver a autorizar una conexión autorizada previamente.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <dt>**FWPM \_ CONDITION \_ ALE \_ REAUTH \_ REASON**</dt> </dl>                                                | El motivo para volver a autorizar una conexión autorizada previamente, como **FWP \_ CONDITION \_ REAUTHORIZE \_ REASON POLICY \_ \_ CHANGE** (o uno de los otros valores enumerados en Marcas de condición [**de filtrado).**](filtering-condition-flags-.md)<br/> **Tipo de datos:** FWP \_ UINT32<br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <dt>**TIPO ICMP \_ ORIGINAL DE CONDICIÓN \_ \_ FWPM \_**</dt> </dl>                                             | Tipo ICMP con el que se creó el flujo.<br/> **Tipo de datos:** FWP \_ UINT16<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <dt>**INTERFAZ DE LLEGADA \_ \_ FÍSICA DE IP \_ DE \_ CONDICIÓN FWPM \_**</dt> </dl>           | EL LUID de la interfaz física asociada a la dirección IP de llegada.<br/> **Tipo de datos:** FWP \_ UINT64<br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <dt>**FWPM \_ CONDITION \_ IP \_ PHYSICAL \_ NEXTHOP \_ INTERFACE**</dt> </dl>           | EL LUID de la interfaz física del próximo salto.<br/> **Tipo de datos:** FWP \_ UINT64<br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <dt>**FWPM \_ CONDITION \_ INTERFACE \_ QUARANTINE \_ EPOCH**</dt> </dl>                     | Recuento de épocas asociado a una interfaz. Reservado.<br/> **Tipo de datos:** FWP \_ UINT64<br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <dt>**CONDICIÓN FWPM \_ \_ ALE \_ SIO \_ FIREWALL SOCKET \_ \_ PROPERTY**</dt> </dl> | Reservado para uso interno. <br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                                              |





| Constantes disponibles para Windows Vista con SP1, Windows Server 2008 y versiones posteriores                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <dt>**INTERFAZ DE LLEGADA IP DE CONDICIÓN FWPM \_ \_ \_ \_**</dt> </dl>                       | LUID de la interfaz de red asociada a la dirección IP de llegada. <br/> **Tipo de datos:** FWP \_ UINT64<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <dt>**TIPO DE INTERFAZ \_ DE LLEGADA \_ DE CONDICIÓN \_ FWPM \_**</dt> </dl>                 | Tipo de la interfaz de red de llegada definida por la Autoridad de nombres asignados por Internet (IANA). Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valores posibles:** Los valores de tipo de interfaz enumerados en el archivo de encabezado Ipifcons.h.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <dt>**FWPM \_ TIPO \_ DE TÚNEL DE LLEGADA DE \_ \_ CONDICIÓN**</dt> </dl>                       | Método de encapsulación utilizado por un túnel asociado a la interfaz de red de llegada si el miembro Type es IF \_ TYPE \_ TUNNEL. La autoridad de nombres asignados a Internet (IANA) define el tipo de túnel. Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valores posibles:** Los valores de tipo de enumeración TUNNEL \_ TYPE enumerados en el archivo de encabezado Ifdef.h.<br/> **Tipo de datos:** FWP \_ UINT32<br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <dt>**FWPM \_ CONDITION \_ ARRIVAL \_ INTERFACE \_ INDEX**</dt> </dl>              | Índice de la interfaz de red de llegada, como enumera la pila de red.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <dt>**FWPM \_ CONDITION \_ ARRIVAL \_ SUB \_ INTERFACE \_ INDEX**</dt> </dl> | Índice de la interfaz de red de llegada, como enumera la pila de red. <br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <dt>**FWPM \_ CONDITION \_ LOCAL \_ INTERFACE \_ INDEX**</dt> </dl>                    | Índice de la interfaz de red, como enumera la pila de red. <br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <dt>**TIPO DE INTERFAZ \_ LOCAL DE \_ CONDICIÓN \_ \_ FWPM**</dt> </dl>                       | Tipo de interfaz tal como se define en Internet Assigned Names Authority (IANA). Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valores posibles:** Los valores de tipo de interfaz enumerados en el archivo de encabezado Ipifcons.h.<br/> **Tipo de datos:** FWP \_ UINT32<br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <dt>**TIPO DE TÚNEL \_ LOCAL DE \_ CONDICIÓN FWPM \_ \_**</dt> </dl>                                | Método de encapsulación utilizado por un túnel si el miembro Type es IF \_ TYPE \_ TUNNEL. La autoridad de nombres asignados a Internet (IANA) define el tipo de túnel. Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valores posibles:** Los valores de tipo de enumeración TUNNEL \_ TYPE enumerados en el archivo de encabezado Ifdef.h.<br/> **Tipo de datos:** FWP \_ UINT32 <br/>                                              |






| Constantes disponibles para Windows Vista y versiones posteriores | Descripción | 
|-------------------------------------------------|-------------|
| <span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt></dl> | Dirección IP local. <br /><strong>Tipo de datos:</strong> Para una dirección IPv4<ul><li>FWP_V4_ADDR_MASK, o</li><li>FWP_UINT32</li></ul><br /><strong>Tipo de datos:</strong> Para una dirección IPv6<ul><li>FWP_V6_ADDR_MASK, o</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt></dl> | Dirección IP remota. <br /><strong>Tipo de datos:</strong> Para una dirección IPv4<ul><li>FWP_V4_ADDR_MASK, o</li><li>FWP_UINT32</li></ul><br /><strong>Tipo de datos:</strong> Para una dirección IPv6<ul><li>FWP_V6_ADDR_MASK, o</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt></dl> | Dirección IP de origen para paquetes reenviados. <br /><strong>Tipo de datos:</strong> Para una dirección IPv4<ul><li>FWP_V4_ADDR_MASK, o</li><li>FWP_UINT32</li></ul><br /><strong>Tipo de datos:</strong> Para una dirección IPv6<ul><li>FWP_V6_ADDR_MASK, o</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt></dl> | Dirección IP de destino para paquetes reenviados. <br /><strong>Tipo de datos:</strong> Para una dirección IPv4<ul><li>FWP_V4_ADDR_MASK, o</li><li>FWP_UINT32</li></ul><br /><strong>Tipo de datos:</strong> Para una dirección IPv6<ul><li>FWP_V6_ADDR_MASK, o</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt></dl> | Tipo de dirección IP local. <br /><strong>Valores posibles:</strong> Cualquiera de los siguientes valores <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeración.<ul><li>NlatUnspecified</li><li>NlatUnicast</li><li>NlatAnycast</li><li>NlatMulticast</li><li>NlatBroadcast</li></ul><br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt></dl> | Tipo de dirección IP de destino para paquetes reenviados. <br /><strong>Valores posibles:</strong> Cualquiera de los siguientes valores <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeración.<ul><li>NlatUnspecified</li><li>NlatUnicast</li><li>NlatAnycast</li><li>NlatMulticast</li><li>NlatBroadcast</li></ul><br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt></dl> | LUID de la interfaz de red asociada a la dirección IP local. <br /><strong>Tipo de datos:</strong> FWP_UINT64<br /> | 
| <span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt></dl> | Tipo de interfaz tal como se define en Internet Assigned Names Authority (IANA). Para más información, consulte [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br /><strong>Valores posibles:</strong> Los valores de tipo de interfaz enumerados en el archivo de encabezado Ipifcons.h.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt></dl> | Método de encapsulación utilizado por un túnel si el miembro Type está IF_TYPE_TUNNEL. La autoridad de nombres asignados a Internet (IANA) define el tipo de túnel. Para más información, consulte <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>. <br /><strong>Valores posibles:</strong> Los TUNNEL_TYPE tipo de enumeración enumerados en el archivo de encabezado Ifdef.h.<br /><strong>Tipo de datos:</strong> FWP_UINT32 <br /> | 
| <span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt></dl> | El LUID de la interfaz de red en la que se va a enviar el paquete que se va a reenviar. <br /><strong>Tipo de datos:</strong> FWP_UINT64<br /> | 
| <span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt></dl> | Número de protocolo IP, tal como se especifica en RFC 1700. <br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt></dl> | Número de puerto del protocolo de transporte local.<br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt></dl> | Campo tipo ICMP, tal como se especifica en RFC 792. <br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt></dl> | Número de puerto del protocolo de transporte remoto. <br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt></dl> | Campo de código ICMP, como se especifica en RFC 792. <br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt></dl> | Tipo de dirección IP local que se inserta en el paquete ICMP.<br /><strong>Valores posibles:</strong> Cualquiera de los siguientes valores <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeración.<ul><li>NlatUnspecified</li><li>NlatUnicast</li><li>NlatAnycast</li><li>NlatMulticast</li><li>NlatBroadcast</li></ul><br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt></dl> | Dirección IP remota incrustada en el paquete ICMP. <br /><strong>Tipo de datos:</strong> Para una dirección IPv4<ul><li>FWP_V4_ADDR_MASK, o</li><li>FWP_UINT32</li></ul><br /><strong>Tipo de datos:</strong> Para una dirección IPv6<ul><li>FWP_V6_ADDR_MASK, o</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt></dl> | Número de protocolo IP insertado en el paquete ICMP, tal como se especifica en RFC 1700. <br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt></dl> | Número de puerto del protocolo de transporte local que se inserta en el paquete ICMP. <br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt></dl> | Número de puerto del protocolo de transporte remoto que se inserta en el paquete ICMP. <br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl><dt><strong>FWPM_CONDITION_FLAGS</strong></dt></dl> | OR bit a bit de una combinación de marcas de condición de filtrado. <br /><strong>Valores posibles:</strong> Consulte <a href="filtering-condition-flags-.md"> <strong>Filtrado de marcas de condición</strong></a><br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt></dl> | Dirección del tráfico o flujo de datos. <br /><strong>Valores posibles:  </strong><ul><li>FWP_DIRECTION_INBOUND</li><li>FWP_DIRECTION_OUTBOUND</li></ul><br /> Para las capas de datagramas (FWPM_LAYER_DATAGRAM_DATA_ ) y las capas de paquetes de flujo *(FWPM_LAYER_STREAM_PACKET_*), el valor será el mismo que la dirección del paquete. <br /> Para las capas de flujo (FWPM_LAYER_STREAM_ ) y las capas establecidas de flujo *(FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), el valor será el mismo que la dirección de la conexión. (Por ejemplo, cuando una aplicación local inicia la conexión, un paquete de entrada FWPM_CONDITION_DIRECTION <strong>establecido</strong> <strong>en FWP_DIRECTION_OUTBOUND</strong>). <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt></dl> | Índice de la interfaz de red, como enumera la pila de red. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt></dl> | Índice de la interfaz de red lógica, como enumera la pila de red. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt></dl> | Índice de la interfaz de red de origen para los paquetes reenviados, como se enumera en la pila de red.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt></dl> | Índice de la interfaz de red lógica de origen para paquetes reenviados, como enumera la pila de red. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt></dl> | Índice de la interfaz de red de destino para los paquetes reenviados, como se enumera en la pila de red. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt></dl> | Índice de la interfaz de red lógica de destino para paquetes reenviados, tal y como enumera la pila de red. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt></dl> | Ruta de acceso completa del dispositivo de la aplicación, tal y como devuelve la función <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0.</strong></a> <br /> (Por ejemplo, "\device0\hardiskvolume1\Program Files\Application.exe").<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt></dl> | Identificación del usuario local. <br /><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt></dl> | Identificación del usuario remoto. <br /><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt></dl> | Identificación de la máquina remota. <br /><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt></dl> | Modo de socket sin formato que se permite o se deniega.<br /><strong>Valores posibles:  </strong><ul><li>SIO_RCVALL</li><li>SIO_RCVALL_IGMPMCAST</li><li>SIO_RCVALL_MCAST</li></ul>Para obtener una descripción de estos modos de socket sin formato, vea la <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>función WSAIoctl.</strong></a><br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt></dl> | Reservado para uso interno. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt></dl> | Reservado para uso interno. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 




Las siguientes constantes solo están disponibles para el modo de usuario.



| Condiciones de modo de usuario disponibles para Windows 8 y Windows Server 2012                                                                                                                       | Descripción                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <dt>**MODO \_ QM DE CONDICIÓN \_ \_ FWPM**</dt> </dl> | El modo del filtro de modo rápido (QM). Consulte [**IPSEC \_ TRAFFIC TYPE \_ (TIPO DE TRÁFICO de IPSEC)**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) para ver los valores posibles.<br/> **Tipo de datos:** FWP \_ UINT32<br/> |






| Condiciones de modo de usuario disponibles para Windows 7, Windows Server 2008 R2 y versiones posteriores | Descripción | 
|---------------------------------------------------------------------------------|-------------|
| <span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt></dl> | Reservado para uso interno.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt></dl> | Nombre del mismo nivel. Por ejemplo, el nombre DNS del mismo nivel.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt></dl> | Identidad de la entidad de seguridad de autenticación remota. <br /><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt></dl> | El tipo de método de autenticación IKE, IKEv2 o AuthIP. <br /><strong>Tipo de datos:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE<br /> | 
| <span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt></dl> | El tipo de módulo de claves.<br /><strong>Tipo de datos:</strong> IKEEXT_KEY_MODULE_TYPE<br /> | 
| <span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt></dl> | Modo IPsec en el que se puede obtener un token.<br /><strong>Tipo de datos:</strong> IPSEC_TOKEN_MODE<br /> | 
| <span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt></dl> | Clave de contexto del proveedor de directivas de modo principal (MM) o modo rápido (QM) del SA que se está autorizando. Resulta útil para restringir el ámbito de la regla de autorización a LAS formadas mediante una clave de directiva MM o QM de IPsec especificada.<br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY16_TYPE<br /> | 
| <span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt></dl> | Método utilizado para autenticar la asociación de seguridad.<br /><blockquote>[!Note]<br />Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.</blockquote><br /><strong>Tipo de datos:</strong> FWP_UINT32 <br /> | 







| Constantes disponibles para Windows Vista y versiones posteriores | Descripción | 
|-------------------------------------------------|-------------|
| <span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt></dl> | Identificación del usuario remoto.<br /><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt></dl> | UUID de la interfaz RPC. <br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY16_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt></dl> | Versión de la interfaz RPC. <br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt></dl> | Reservado para uso interno. <br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt></dl> | Identificación de la aplicación COM.<br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY16_TYPE<br /> | 
| <span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt></dl> | Nombre de la aplicación.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt></dl> | Protocolo RPC. <br /><strong>Valores posibles:  </strong><ul><li>RPC_PROTSEQ_TCP</li><li>RPC_PROTSEQ_NMP</li><li>RPC_PROTSEQ_LRPC</li><li>RPC_PROTSEQ_HTTP</li></ul><br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt></dl> | Tipo de servicio de autenticación. Para obtener más información sobre los tipos de servicio de autenticación, vea <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service Constants</strong></a>. <br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt></dl> | Nivel de servicio de autenticación. Para obtener más información sobre los niveles de servicio de autenticación, vea <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Constantes de nivel de autenticación</strong></a>. <br /><strong>Tipo de datos:</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt></dl> | Algoritmo de cifrado de la interfaz de proveedor de servicios de seguridad (SSPI) basado en certificados.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt></dl> | Tamaño de la clave de cifrado SSPI basada en certificado.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt></dl> | Dirección IPv4 local. <br /><strong>Tipo de datos:  </strong><ul><li>FWP_V4_ADDR_MASK, o</li><li>FWP_UINT32</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt></dl> | Dirección IPv6 local. <br /><strong>Tipo de datos:  </strong><ul><li>FWP_V6_ADDR_MASK, o</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt></dl> | Dirección IPv4 remota. <br /><strong>Tipo de datos:  </strong><ul><li>FWP_V4_ADDR_MASK, o</li><li>FWP_UINT32</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt></dl> | Dirección IPv6 remota. <br /><strong>Tipo de datos:  </strong><ul><li>FWP_V6_ADDR_MASK, o</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl><dt><strong>FWPM_CONDITION_PIPE</strong></dt></dl> | Nombre de la canalización con nombre remoto.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt></dl> | UUID del proceso con la interfaz RPC.<br /><strong>Tipo de datos:</strong> FWP_BYTE_ARRAY16_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt></dl> | Reservado para uso interno.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt></dl> | Reservado para uso interno.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt></dl> | Identificación del cliente cuando se usa RpcProxy.<br /><strong>Tipo de datos:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt></dl> | Nombre del servidor RPC cuando se usa RpcProxy.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt></dl> | Puerto en el servidor RPC cuando se usa RpcProxy.<br /><strong>Tipo de datos:</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt></dl> | Tipo de servicio de autenticación de proxy RPC.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt></dl> | Longitud de clave de Capa de sockets seguros (SSL) en el certificado de cliente.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt></dl> | Identificador de objeto en el certificado de cliente.<br /><strong>Tipo de datos:</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt></dl> | Tipo de evento net.<br /><strong>Tipo de datos:</strong> FWP_UINT32<br /> | 




## <a name="remarks"></a>Comentarios

Cuando las direcciones IP se almacenan en formato FWP UINT32 o cuando un puerto IP se almacena en formato \_ FWP UINT16, se almacenan en orden de host, no en orden \_ de red.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |
