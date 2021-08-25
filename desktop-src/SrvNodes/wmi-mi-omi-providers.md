---
description: Windows La infraestructura de administración (WMI), la instrumentación de administración (MI) y la infraestructura de administración abierta (OMI) usan archivos de formato de objeto de administración (MOF) para describir la información que está disponible a través de sus proveedores respectivos.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: Proveedores de WMI/MI/OMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682629f72da94cd2210fb781284a7cb4cf7f85868ff405f22727e619d128ae65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992425"
---
# <a name="wmimiomi-providers"></a>Proveedores de WMI/MI/OMI

Windows La infraestructura de administración (WMI), la instrumentación de administración (MI) y la infraestructura de administración abierta (OMI) usan archivos de formato de objeto de administración (MOF) para describir la información que está disponible a través de sus proveedores respectivos.

<dl> <dt>

<span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)
</dt> <dd>

El Active Directory, también conocido como proveedor de servicios de directorio (DS), asigna objetos Active Directory a WMI. Al acceder al espacio de nombres Ldap (Protocolo ligero de acceso a directorios) en WMI, puede hacer referencia a un objeto o convertirlo en un alias en el Active Directory.

</dd> <dt>

<span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Inventario de aplicaciones](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)
</dt> <dd>

Las clases WMI de Inventario de aplicaciones permiten la detección de las aplicaciones Win32 instaladas y Windows almacenar aplicaciones en un Windows instalado.

</dd> <dt>

<span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Application Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)
</dt> <dd>

Application Proxy WMI permite a los desarrolladores acceder al servicio web Application Proxy para que los administradores puedan publicar aplicaciones para el acceso externo. Web Application Proxy es un proxy inverso para Servicios de federación de Active Directory (AD FS) (AD FS).

</dd> <dt>

<span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Cifrado de unidad BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)
</dt> <dd>

Proporciona configuración y administración para un área de almacenamiento en una unidad de disco duro, representada por una instancia de [**\_ Win32 EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), que se puede proteger mediante cifrado.

</dd> <dt>

<span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dd>

El servidor compacto de Servicio de transferencia inteligente en segundo plano (BITS) con administración remota de BITS permite a los administradores autenticados o a las aplicaciones de controlador crear, modificar y administrar trabajos de transferencia de BITS de forma remota sin usar el servicio Internet Information Services (IIS).

</dd> <dt>

<span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[Biztalk](https://msdn.microsoft.com/library/ms941491.aspx)
</dt> <dd>

Proporciona acceso a los objetos de administración de BizTalk representados por clases WMI.

</dd> <dt>

<span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[datos de la configuración de arranque (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)
</dt> <dd>

El datos de la configuración de arranque (BCD) (BCD) proporciona un almacén que se usa para describir las aplicaciones de arranque y la configuración de la aplicación de arranque.

</dd> <dt>

<span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Recopilador de eventos de arranque](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)
</dt> <dd>

El proveedor WMI del recopilador de eventos de arranque proporciona acceso a la información de conexión y configuración de la característica De instalación y recopilación de eventos de arranque en Windows Server.

</dd> <dt>

<span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, Eventos de administración de energía](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)
</dt> <dd>

Los proveedores CIMWin32 admiten las clases implementadas en CimWin32.dll y constan de las clases CIM principales, la implementación win32 de esas clases y los eventos de administración de energía.

</dd> <dt>

<span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)
</dt> <dd>

El proveedor CIMWin32a amplía las clases disponibles en [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).

</dd> <dt>

<span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)
</dt> <dd>

El proveedor DcbQosCim admite clases que describen datos de configuración de QOS de red, datos de configuración de control y datos de configuración de clases de tráfico.

</dd> <dt>

<span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Sistema de archivos distribuido (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)
</dt> <dd>

El proveedor DFS proporciona funciones DFS que admiten scripts a través de WMI.

</dd> <dt>

<span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Sistema de archivos distribuido replicación de datos (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)
</dt> <dd>

Crea herramientas para configurar y supervisar el [servicio Sistema de archivos distribuido (DFS).](/previous-versions/windows/desktop/dfs/distributed-file-system) Para obtener más información, vea [Clases WMI DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).

</dd> <dt>

<span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)
</dt> <dd>

El [proveedor Dfsncimprov admite](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) clases que implementan el acceso al espacio de nombres DFS.

</dd> <dt>

<span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)
</dt> <dd>

El [proveedor DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) admite clases que interactúan con un servidor de protocolo de configuración dinámica de host (DHCP).

</dd> <dt>

<span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Cuota de disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)
</dt> <dd>

El Windows de cuota de disco permite a los administradores controlar la cantidad de datos que cada usuario almacena en un sistema de archivos NTFS.

</dd> <dt>

<span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Coordinador de transacciones distribuidas (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)
</dt> <dd>

El proveedor de DTC permite la administración del DTC.

</dd> <dt>

<span id="DNS"></span><span id="dns"></span>[Dns](/windows/desktop/DNS/dns-wmi-provider)
</dt> <dd>

Permite a los administradores y programadores configurar registros de recursos (RR) del Sistema de nombres de dominio (DNS) y servidores DNS mediante WMI.

</dd> <dt>

<span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Clases de proveedor dnsclientcim](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)
</dt> <dd>

El proveedor Dnsclientcim admite clases que interactúan con un cliente del Sistema de nombres de dominio (DNS).

</dd> <dt>

<span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)
</dt> <dd>

El [proveedor DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) admite clases WMI que interactúan con un cliente DNS.

</dd> <dt>

<span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)
</dt> <dd>

El [proveedor DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) admite clases WMI que interactúan con un servidor DNS.

</dd> <dt>

<span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider)
</dt> <dd>

El [proveedor de registro de](/previous-versions/windows/desktop/eventlogprov/event-log-provider) eventos proporciona acceso a los datos del servicio de registro de eventos y notificación de eventos.

</dd> <dt>

<span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Administración de seguimiento de eventos](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)
</dt> <dd>

El proveedor de administración de seguimiento de eventos proporciona acceso al seguimiento de eventos para las configuraciones de sesión del registrador automático de Windows (ETW) y los eventos de seguimiento.

</dd> <dt>

<span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Actualización de Cluster-Aware conmutación por error](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)
</dt> <dd>

El proveedor de actualización Cluster-Aware conmutación por error (CAU) admite la coordinación y la administración de cau.

</dd> <dt>

<span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Clústeres de conmutación por error de Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)
</dt> <dd>

El proveedor de Hyper-V de clústeres de conmutación por error proporciona administración e informes de Hyper-V en un entorno de agrupación en clústeres.

</dd> <dt>

<span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Clústeres de conmutación por error Storage QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)
</dt> <dd>

El proveedor de calidad de servicio (QoS) Storage clústeres de conmutación por error proporciona administración e informes de las directivas qoS de almacenamiento en clústeres.

</dd> <dt>

<span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Proveedor de clúster de conmutación por error V1](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)
</dt> <dd>

El proveedor de clúster de conmutación por error V1 proporciona administración de un clúster de conmutación por error.

</dd> <dt>

<span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Extensiones de clúster de conmutación por error V1](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)
</dt> <dd>

El proveedor de extensiones de clúster de conmutación por error proporciona administración adicional de un clúster de conmutación por error.

</dd> <dt>

<span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Puerta de enlace Health Monitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)
</dt> <dd>

El proveedor de Health Monitor de puerta de enlace administra información y eventos de supervisión del estado de la puerta de enlace.

</dd> <dt>

<span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[directiva de grupo API](/previous-versions/windows/desktop/Policy/group-policy-start-page)
</dt> <dd>

El directiva de grupo permite la administración basada en directivas mediante los servicios de directorio de Microsoft Active Directory (AD).

</dd> <dt>

<span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Servicio de protección de host](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)
</dt> <dd>

El proveedor del Servicio de protección de host proporciona administración del Servicio de protección de host para máquinas virtuales blindadas.

</dd> <dt>

<span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)
</dt> <dd>

El proveedor de Hyper-V permite administrar y recuperar información sobre las máquinas virtuales.

</dd> <dt>

<span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)
</dt> <dd>

El proveedor de Hyper-V (V2) amplía el [proveedor de Hyper-V.](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)

</dd> <dt>

<span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))
</dt> <dd>

Expone interfaces de programación que se pueden usar para consultar y configurar la metabase de IIS.

</dd> <dt>

<span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Servidor de administración de direcciones de protocolo de Internet (IPAM)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)
</dt> <dd>

El proveedor IPAM server permite a los desarrolladores administrar IPAM a través de WMI.

</dd> <dt>

<span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[Proveedor de rutas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)
</dt> <dd>

El proveedor de rutas IP preinstalado proporciona información de enrutamiento de red IPV4, incluida (entre otras) la información disponible a través del comando **route print.**

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)
</dt> <dd>

Proporciona datos IPMI de las operaciones del controlador de administración de placa base (BMC).

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)
</dt> <dd>

El Servidor de destino iSCSI admite una interfaz WMI para administrar microsoft Servidor de destino iSCSI, como crear discos virtuales y presentarlos al cliente.

</dd> <dt>

<span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Objeto Job](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)
</dt> <dd>

El proveedor de objetos de trabajo admite el acceso a los datos sobre objetos de trabajo de kernel con nombre.

</dd> <dt>

<span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Seguimiento del kernel](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)
</dt> <dd>

El proveedor de eventos kernel Trace preinstalado permite ver eventos de seguimiento de kernel en creación de procesos, terminación de procesos, creación de subprocesos, terminación de subprocesos y carga de módulos.

</dd> <dt>

<span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))
</dt> <dd>

Proporciona clases que crean, registran, configuran y administran aplicaciones personalizadas del Protocolo de iniciación de sesión (SIP) con [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).

</dd> <dt>

<span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registro de herramientas de administración](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)
</dt> <dd>

El proveedor del Registro de herramientas de administración proporciona acceso remoto al Registro.

</dd> <dt>

<span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Herramientas de administración Administrador de tareas](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)
</dt> <dd>

El proveedor de Administrador de tareas herramientas de administración proporciona acceso y administración de los Administrador de tareas datos.

</dd> <dt>

<span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Aplicación MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)
</dt> <dd>

El proveedor de Administración de dispositivos móviles (MDM) administra las aplicaciones en dispositivos que están suscritos al servicio MDM.

</dd> <dt>

<span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[Puente MDM](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)
</dt> <dd>

El proveedor de puente de MDM permite la administración de MDM de un puente de red.

</dd> <dt>

<span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Mdm Configuración](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)
</dt> <dd>

El proveedor de Configuración MDM permite la administración de la configuración en dispositivos inscritos con un servicio MDM.

</dd> <dt>

<span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)
</dt> <dd>

El [proveedor MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) expone una clase que define una clase de vista para un sistema de equipo físico.

</dd> <dt>

<span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)
</dt> <dd>

La [sección proveedor MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) proporciona información de referencia para las clases de proveedor de MsNetImPlatform implementadas en NdisIMPlatCim.dll.

</dd> <dt>

<span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)
</dt> <dd>

El [proveedor NetAdapterCim admite](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) clases que tienen acceso a adaptadores de red.

</dd> <dt>

<span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)
</dt> <dd>

En esta sección se proporciona información de referencia para las clases de proveedor de [NetDaCim.](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)

</dd> <dt>

<span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)
</dt> <dd>

Proporciona información de referencia para las clases de proveedor de [NetNcCim.](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)

</dd> <dt>

<span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)
</dt> <dd>

El [proveedor NetPeerDist admite](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) clases que interactúan con la infraestructura de caché de rama.

</dd> <dt>

<span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)
</dt> <dd>

El [proveedor NetQosCim proporciona](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) datos para la calidad de servicio de red (QoS) y los datos de configuración de QoS.

</dd> <dt>

<span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)
</dt> <dd>

En esta sección se proporciona información de referencia para las clases de proveedor NetSwitchTeam declaradas en NetSwitchTeam.mof e implementadas en NetSwitchTeamCim.dll.

</dd> <dt>

<span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)
</dt> <dd>

El proveedor NetTCPIP admite clases que interactúan con conexiones TCPIP.

</dd> <dt>

<span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)
</dt> <dd>

En esta sección se proporciona información de referencia para las clases de proveedor de NetTtCim definidas en NetTtCim.mof e implementadas en NetTtCim.dll.

</dd> <dt>

<span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)
</dt> <dd>

El proveedor netWNV admite clases que interactúan con las tecnologías de virtualización de red.

</dd> <dt>

<span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Protección de acceso a la red](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)
</dt> <dd>

El proveedor de protección de acceso a redes expone una plataforma para el acceso protegido a redes privadas.

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Equilibrio de carga de red](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)
</dt> <dd>

El proveedor de equilibrio de carga de red (NLB) permite la administración de un clúster NLB.

</dd> <dt>

<span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Servidor NetworkController](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)
</dt> <dd>

El proveedor permite la administración de un servidor de controladora de red.

</dd> <dt>

<span id="NFS"></span><span id="nfs"></span>[Nfs](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)
</dt> <dd>

El proveedor de NFS permite crear herramientas y scripts para configurar y supervisar el Windows de archivos de red.

</dd> <dt>

<span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Señal](/previous-versions/windows/desktop/wmipicmp/ping-provider)
</dt> <dd>

El proveedor Ping proporciona acceso a la información de estado proporcionada por el comando ping estándar.

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Política](/previous-versions/windows/desktop/policmanprov/policy-provider)
</dt> <dd>

Proporciona extensiones a la directiva de grupo y permite refinamientos en la aplicación de la directiva.

</dd> <dt>

<span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Medidor de energía](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)
</dt> <dd>

El proveedor de medidores de energía admite la interfaz de medición y presupuestos de energía (PMB). Estas clases son la interfaz principal para la consulta de información de la interfaz de medidor de energía (PMI) de los medidores de energía subyacentes en el sistema.

</dd> <dt>

<span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Directiva de energía](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)
</dt> <dd>

El proveedor de Power Policy proporciona a las clases la capacidad de administrar de forma remota toda la infraestructura de directivas de energía.

</dd> <dt>

<span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)
</dt> <dd>

El [proveedor RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) proporciona clases para administrar el acceso remoto.

</dd> <dt>

<span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)
</dt> <dd>

El [proveedor RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) proporciona clases para administrar el servidor de acceso remoto.

</dd> <dt>

<span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)
</dt> <dd>

El [proveedor ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) expone las métricas de confiabilidad del sistema Windows del registro de eventos.

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Servicios de Escritorio remoto](/windows/desktop/TermServ/terminal-services-wmi-provider)
</dt> <dd>

Permite una administración coherente del servidor en Servicios de Escritorio remoto entorno.

</dd> <dt>

<span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)
</dt> <dd>

Define clases que permiten escribir scripts y código para modificar la configuración del servidor de informes y el Administrador de informes.

</dd> <dt>

<span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Conjunto resultante de directivas (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)
</dt> <dd>

Proporciona métodos para planear y depurar la configuración de directivas en una situación de "what-if". Estos métodos permiten a los administradores determinar fácilmente la combinación de la configuración de directiva que se aplica o se aplicará a un usuario o equipo. Esto se conoce como conjunto resultante de directivas (RSoP). Para obtener más información, vea [Acerca del proveedor de métodos WMI de RSoP](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) y Clases WMI de [RSoP](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).

</dd> <dt>

<span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Seguridad](/previous-versions/windows/desktop/secrcw32prov/security-provider)
</dt> <dd>

Recupera o cambia la configuración de seguridad que controla la propiedad, la auditoría y los derechos de acceso a archivos, directorios y recursos compartidos.

</dd> <dt>

<span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)
</dt> <dd>

[ServerManager.DeploymentProvider expone](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) la funcionalidad de implementación.

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Sesión](/previous-versions/windows/desktop/wmipsess/session-provider)
</dt> <dd>

Administra las sesiones de red y las conexiones.

</dd> <dt>

<span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Instantánea](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)
</dt> <dd>

Proporciona funciones de administración para la característica Instantáneas de carpetas compartidas.

</dd> <dt>

<span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Aprovisionamiento de máquinas virtuales blindadas](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)
</dt> <dd>

El proveedor de aprovisionamiento de máquinas virtuales blindadas permite que un controlador de tejido inicie el aprovisionamiento seguro de una máquina virtual blindada en un host de Hyper-V.

</dd> <dt>

<span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Servicio de aprovisionamiento de máquinas virtuales blindadas](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)
</dt> <dd>

El proveedor habilita el aprovisionamiento de una máquina virtual blindada.

</dd> <dt>

<span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Administración de SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
</dt> <dd>

El servicio SMB API de Administración clases y métodos para administrar recursos compartidos y el acceso compartido.

</dd> <dt>

<span id="SNMP"></span><span id="snmp"></span>[Snmp](/windows/desktop/WmiSdk/snmp-provider)
</dt> <dd>

Mapas Objetos de Protocolo simple de administración de redes (SNMP) que se definen en objetos de esquema de Base de información de administración (MIB) para clases. Para obtener más información, vea [Configuración del entorno SNMP de WMI.](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment)

</dd> <dt>

<span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Registro de inventario de software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
</dt> <dd>

El proveedor de registro de inventario de software recopila datos de licencias sobre el software instalado en un servidor de Windows y proporciona acceso remoto a los datos para que un centro de datos pueda agregarlo fácilmente.

</dd> <dt>

<span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Licencias de software para Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)
</dt> <dd>

[Clases de licencias de](/previous-versions/windows/desktop/sppwmi/software-license-provider-) software usadas para Windows Vista.

</dd> <dt>

<span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Licencia de software](/previous-versions/windows/desktop/sppwmi/software-license-provider-)
</dt> <dd>

El proveedor de licencias de software recupera los datos de licencias de software.

</dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Storage Volumen](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)
</dt> <dd>

El proveedor Storage volumen proporciona funciones de administración de volúmenes.

</dd> <dt>

<span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Storage Réplica](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)
</dt> <dd>

El proveedor habilita la administración de una réplica de almacenamiento.

</dd> <dt>

<span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider)
</dt> <dd>

El proveedor del Registro del sistema permite a las aplicaciones de administración recuperar y modificar datos en el registro del sistema y recibir notificaciones cuando se producen cambios.

</dd> <dt>

<span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Restaurar sistema](/windows/desktop/sr/system-restore-portal)
</dt> <dd>

Proporciona clases que configuran y usan Restaurar sistema funcionalidad. Para obtener más información, vea [Configuring Restaurar sistema](/windows/desktop/sr/configuring-system-restore) and the [Restaurar sistema WMI Classes](/windows/desktop/sr/system-restore-wmi-classes).

</dd> <dt>

<span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Módulo de plataforma segura](/windows/desktop/SecProv/trusted-platform-module-provider)
</dt> <dd>

Proporciona acceso a los datos sobre un dispositivo de seguridad, representado por una instancia de [**\_ TPM de Win32,**](/windows/desktop/SecProv/win32-tpm)que es la raíz de confianza de un sistema informático de la plataforma de confianza de Microsoft Windows.

</dd> <dt>

<span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)
</dt> <dd>

El [proveedor Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) es un proveedor de instancias que crea clases con información sobre las relaciones de confianza entre dominios.

</dd> <dt>

<span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Registro de acceso de usuario](/previous-versions/windows/desktop/ual/user-access-logging)
</dt> <dd>

El registro de acceso de usuario (UAL) es un marco común para que los roles Windows Server informen de sus respectivas métricas de consumo.

</dd> <dt>

<span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)
</dt> <dd>

El [proveedor UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) expone clases que proporcionan información sobre un perfil de usuario en un sistema Windows, así como el estado de mantenimiento de una carpeta de usuario redirigida.

</dd> <dt>

<span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Administración de estado de usuario](/previous-versions/windows/desktop/usm/user-state-management-api-portal)
</dt> <dd>

El proveedor de administración de estado de usuario expone una API de administración e informes para escenarios empresariales.

</dd> <dt>

<span id="View"></span><span id="view"></span><span id="VIEW"></span>[Vista](/windows/desktop/WmiSdk/view-provider)
</dt> <dd>

Crea nuevas instancias y métodos basados en instancias de otras clases. Hay dos versiones del proveedor de vistas disponibles en plataformas de 64 bits.

</dd> <dt>

<span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)
</dt> <dd>

El [proveedor VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) expone una plataforma para automatizar la conectividad con un cliente de red privada virtual.

</dd> <dt>

<span id="WDM"></span><span id="wdm"></span>[Wdm](/windows/desktop/WmiCoreProv/wdm-provider)
</dt> <dd>

Proporciona acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan a Windows Driver Model (WDM).

</dd> <dt>

<span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)
</dt> <dd>

El [proveedor WFasCim expone](/previous-versions/windows/desktop/wfascimprov/network-security-classes) características de filtrado y seguridad de red.

</dd> <dt>

<span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)
</dt> <dd>

El [proveedor WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) expone información de firma digital sobre los controladores.

</dd> <dt>

<span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)
</dt> <dd>

El [proveedor Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) expone las marcas de tiempo actuales, locales y basadas en UTC en un sistema informático.

</dd> <dt>

<span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Componentes de acceso a datos (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)
</dt> <dd>

Proporciona administración de WDAC.

</dd> <dt>

<span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
</dt> <dd>

El Windows Defender de seguridad expone Windows Defender de seguridad.

</dd> <dt>

<span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Instalador](/previous-versions/windows/desktop/msiprov/windows-installer-provider)
</dt> <dd>

El Windows installer, también conocido como proveedor MSI, permite a las aplicaciones acceder a la información recopilada de Windows aplicaciones compatibles con installer.

</dd> <dt>

<span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Activación del producto](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)
</dt> <dd>

El Windows de activación de productos (WPA) es una tecnología antisecuidad destinada a reducir la copia informal de software.

</dd> <dt>

<span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Administrador del servidor](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)
</dt> <dd>

El proveedor permite el acceso y la administración de la configuración controlada por la Administrador del servidor aplicación.

</dd> <dt>

<span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server Storage Management (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)
</dt> <dd>

El proveedor MsftStrgMan proporciona administración de sistemas de almacenamiento en Windows Server.

</dd> <dt>

<span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows Storage Management (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
</dt> <dd>

El proveedor StrgMgmt se puede usar para administrar una amplia gama de configuraciones de almacenamiento, desde tabletas hasta matrices de almacenamiento externas en servidores.

</dd> <dt>

<span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows Herramienta de evaluación del sistema](/windows/desktop/WinSAT/winsat-mof-classes)
</dt> <dd>

La Windows System Assessment Tool (WinSAT) expone una serie de clases que evalúan las características y funcionalidades de rendimiento de un equipo.

</dd> <dt>

<span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI Core](/windows/desktop/WmiCoreProv/wmi-core-provider-)
</dt> <dd>

El proveedor WMI Core define clases que componen la funcionalidad principal de WMI.

</dd> <dt>

<span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)
</dt> <dd>

El [proveedor Msft \_ ProviderSubSystem admite](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) proveedores.

</dd> <dt>

<span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32 \_ Perf](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)
</dt> <dd>

La [**clase abstracta \_ Win32 Perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) es la clase base para las clases de contador de rendimiento [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) y [**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov). Define las propiedades de marca de tiempo y frecuencia necesarias usadas en los algoritmos CounterType para las clases de contador de rendimiento.

</dd> <dt>

<span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)
</dt> <dd>

Clase base abstracta para las clases de datos calculadas preinstaladas.

</dd> <dt>

<span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)
</dt> <dd>

La clase de contador de [**rendimiento Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) es la clase base abstracta para todas las clases de contadores de rendimiento sin procesar concretas. Para aparecer en el Monitor de sistema, las clases de contador de rendimiento deben agregarse al espacio de nombres \\ "ROOT CIMv2" y derivarse de **Win32 \_ PerfRawData**.

</dd> <dt>

<span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)
</dt> <dd>

Crea las clases [de contador de rendimiento wmi](/windows/desktop/CIMWin32Prov/performance-counter-classes). El proveedor WMIPerfInst proporciona dinámicamente datos a estas clases de rendimiento.

</dd> <dt>

<span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)
</dt> <dd>

Proporciona datos de contadores de rendimiento sin formato y con formato de forma dinámica a partir de [definiciones de clase de contador](/windows/desktop/CIMWin32Prov/performance-counter-classes) de rendimiento.

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Carpetas de trabajo](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)
</dt> <dd>

Carpetas de trabajo se usa para sincronizar archivos con varios equipos y dispositivos móviles.

</dd> </dl>

 

 
