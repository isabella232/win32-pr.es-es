---
description: Windows Management Infrastructure (WMI), instrumental de administración (MI) y Open Management Infrastructure (OMI) usan archivos de formato de objetos de administración (MOF) para describir la información que se pone a disposición de los proveedores respectivos.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: Proveedores de WMI/MI/OMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505a0853d9df7d9cf6f2371f6342b77f61f536b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669983"
---
# <a name="wmimiomi-providers"></a><span data-ttu-id="bc4d2-103">Proveedores de WMI/MI/OMI</span><span class="sxs-lookup"><span data-stu-id="bc4d2-103">WMI/MI/OMI Providers</span></span>

<span data-ttu-id="bc4d2-104">Windows Management Infrastructure (WMI), instrumental de administración (MI) y Open Management Infrastructure (OMI) usan archivos de formato de objetos de administración (MOF) para describir la información que se pone a disposición de los proveedores respectivos.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-104">Windows Management Infrastructure (WMI), Management Instrumentation (MI) and Open Management Infrastructure (OMI) all use Management Object Format (MOF) files to describe the information made available through their respective providers.</span></span>

<dl> <dt>

<span data-ttu-id="bc4d2-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-106">El proveedor de Active Directory, también conocido como proveedor de servicios de directorio (DS), asigna Active Directory objetos a WMI.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-106">The Active Directory provider, also known as the Directory Services (DS) provider, maps Active Directory objects to WMI.</span></span> <span data-ttu-id="bc4d2-107">Al tener acceso al espacio de nombres LDAP (Protocolo ligero de acceso a directorios) en WMI, puede hacer referencia a un objeto o convertirlo en un alias en el Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-107">By accessing the Lightweight Directory Access Protocol (LDAP) namespace in WMI, you can reference or make an object an alias in the Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Inventario de aplicaciones](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Application Inventory](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-109">Las clases WMI para el inventario de aplicaciones habilitan la detección de las aplicaciones Win32 instaladas y de las aplicaciones de la tienda Windows en un sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-109">The WMI classes for Application Inventory enable discovery of the installed Win32 applications and Windows store applications on a Windows system.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Proxy de aplicación](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Application Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-111">El proveedor de WMI del proxy de aplicación permite a los desarrolladores tener acceso al servicio de proxy de aplicación web para que los administradores puedan publicar aplicaciones para el acceso externo.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-111">Application Proxy WMI Provider enables developers to access the Web Application Proxy service so administrators can publish applications for external access.</span></span> <span data-ttu-id="bc4d2-112">Proxy de aplicación web es un proxy inverso para Servicios de federación de Active Directory (AD FS) (AD FS).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-112">Web Application Proxy is a reverse proxy for Active Directory Federation Services (AD FS).</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Cifrado de unidad BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker Drive Encryption (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-114">Proporciona configuración y administración para un área de almacenamiento en una unidad de disco duro, representada por una instancia de [**Win32 \_ EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), que se puede proteger mediante el cifrado.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-114">Provides configuration and management for an area of storage on a hard disk drive, represented by an instance of [**Win32\_EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), that can be protected by using encryption.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-115"><span id="BITS"></span><span id="bits"></span>[PARADA](/previous-versions/windows/desktop/bitsprov/bits-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-115"><span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-116">El servidor compacto de Servicio de transferencia inteligente en segundo plano (BITS) con administración remota de BITS permite a los administradores autenticados o las aplicaciones de controlador crear, modificar y administrar de forma remota los trabajos de transferencia de BITS sin utilizar el servicio Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-116">The Background Intelligent Transfer Service (BITS) Compact Server with BITS Remote Management allows authenticated administrators or controller applications to create, modify and manage BITS transfer jobs remotely without using the Internet Information Services (IIS) service.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[Doc](https://msdn.microsoft.com/library/ms941491.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-118">Proporciona acceso a los objetos de administración de BizTalk que representan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-118">Supplies access to the BizTalk administration objects represented by WMI classes.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[datos de la configuración de arranque (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Boot Configuration Data](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-120">El proveedor de datos de la configuración de arranque (BCD) (BCD) proporciona un almacén que se usa para describir las aplicaciones de arranque y la configuración de la aplicación de arranque.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-120">The Boot Configuration Data (BCD) provider provides a store that is used to describe boot applications and boot application settings.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Recopilador de eventos de arranque](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Boot Event Collector](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-122">El proveedor WMI del recopilador de eventos de arranque proporciona acceso a la información de conexión y configuración para la característica de recopilación de eventos de instalación y arranque en Windows Server.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-122">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, eventos de administración de energía](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, Power Management Events](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-124">Los proveedores de CIMWin32 admiten las clases implementadas en CimWin32.dll y constan de las clases CIM principales, la implementación de Win32 de esas clases y los eventos de administración de energía.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-124">The CIMWin32 providers support the classes implemented in CimWin32.dll, and consist of the core CIM classes, the Win32 implementation of those classes, and power management events.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-126">El proveedor CIMWin32a extiende las clases disponibles en [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-126">The CIMWin32a provider extends the classes available in the [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-128">El proveedor DcbQosCim admite clases que describen los datos de configuración de QOS de red, el control de los datos de configuración y los datos de configuración de clase de tráfico.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-128">The DcbQosCim provider supports classes that describe Network QOS setting data, control setting data, and traffic class setting data.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Sistema de archivos distribuido (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Distributed File System (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-130">El proveedor de DFS proporciona funciones DFS que admiten scripts a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-130">The DFS provider supplies scriptable DFS functions through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Replicación de Sistema de archivos distribuido (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-132">Crea herramientas para configurar y supervisar el servicio [sistema de archivos distribuido (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) .</span><span class="sxs-lookup"><span data-stu-id="bc4d2-132">Creates tools for configuring and monitoring the [Distributed File System (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) service.</span></span> <span data-ttu-id="bc4d2-133">Para obtener más información, vea [clases de WMI de DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-133">For more information, see [DFSR WMI Classes](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-135">El proveedor [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) admite clases que implementan el acceso al espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-135">The [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) provider supports classes that implement DFS namespace access.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-137">El proveedor [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) admite clases que interactúan con un servidor de protocolo de configuración dinámica de host (DHCP).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-137">The [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) provider supports classes that interact with a dynamic host configuration protocol (DHCP) server.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Cuota de disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Disk Quota](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-139">El proveedor de cuota de disco de Windows permite a los administradores controlar la cantidad de datos que almacena cada usuario en un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-139">The Windows Disk Quota provider allows administrators to control the amount of data that each user stores on an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Coordinador de transacciones distribuidas (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-141">El proveedor de DTC permite la administración de DTC.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-141">The DTC provider enables management of the DTC.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-142"><span id="DNS"></span><span id="dns"></span>[DN](/windows/desktop/DNS/dns-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-142"><span id="DNS"></span><span id="dns"></span>[DNS](/windows/desktop/DNS/dns-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-143">Permite a los administradores y programadores configurar registros de recursos (RR) de sistema de nombres de dominio (DNS) y servidores DNS mediante WMI.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-143">Enables administrators and programmers to configure Domain Name System (DNS) resource records (RRs) and DNS Servers using WMI.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Clases de proveedor Dnsclientcim](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim Provider Classes](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-145">El proveedor Dnsclientcim admite clases que interactúan con un cliente de sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-145">The Dnsclientcim provider supports classes that interact with a Domain Name System (DNS) client.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-147">El proveedor [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) admite clases WMI que interactúan con un cliente DNS.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-147">The [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) provider supports WMI classes that interact with a DNS client.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-149">El proveedor [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) admite clases WMI que interactúan con un servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-149">The [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) provider supports WMI classes that interact with a DNS server.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-151">El proveedor de [registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) proporciona acceso a los datos del servicio registro de eventos y a la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-151">The [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supplies access to data from the event log service, and notification of events.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Administración de seguimiento de eventos](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Event Tracing Management](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-153">El proveedor de administración de seguimiento de eventos proporciona acceso a las configuraciones de sesión y los eventos de seguimiento de seguimiento de eventos para Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-153">The Event Tracing Management provider provides access to Event Tracing for Windows (ETW) autologger session configurations and trace events.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Actualización de Cluster-Aware de conmutación por error](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Failover Cluster-Aware Updating](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-155">El proveedor de actualización de Cluster-Aware de conmutación por error (CAU) admite la coordinación con y la administración de CAU.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-155">The Failover Cluster-Aware Updating (CAU) provider supports coordination with and management of CAU.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Clústeres de conmutación por error de Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Failover Clustering Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-157">El proveedor de clústeres de conmutación por error de Hyper-V proporciona administración e informes de Hyper-V en un entorno de clústeres.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-157">The Failover Clustering Hyper-V provider provides management and reporting of Hyper-V in a clustering environment.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[QoS de almacenamiento de clústeres de conmutación por error](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Failover Clustering Storage QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-159">El proveedor de calidad de servicio (QoS) del almacenamiento de clústeres de conmutación por error proporciona administración e informes de las directivas QoS de almacenamiento de clústeres.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-159">The Failover Clustering Storage Quality of Service (QoS) provider provides management and reporting of the clustering storage QoS policies.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Proveedor de clústeres de conmutación por error v1](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failover Cluster V1 Provider](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-161">El proveedor de clústeres de conmutación por error v1 proporciona la administración de un clúster de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-161">The Failover Cluster V1 provider provides management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Extensiones V1 de clúster de conmutación por error](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Failover Cluster V1 Extensions](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-163">El proveedor de extensiones de clúster de conmutación por error proporciona administración adicional de un clúster de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-163">The Failover Cluster Extensions provider provides additional management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Monitor de estado de puerta de enlace](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gateway Health Monitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-165">El proveedor de supervisión de estado de puerta de enlace administra información y eventos de supervisión de estado de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-165">The Gateway Health Monitor provider manages gateway health monitoring events and information.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[API de directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Group Policy API](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-167">El proveedor de directiva de grupo habilita la administración basada en directivas mediante los servicios de directorio de Microsoft Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-167">The Group Policy provider enables policy-based administration using Microsoft Active Directory (AD) directory services.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Servicio de protección de host](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Host Guardian Service](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-169">El proveedor de servicios de protección de host proporciona administración del servicio de protección de host para las máquinas virtuales blindadas.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-169">The Host Guardian Service provider provides management of the Host Guardian Service for shielded VMs.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-171">El proveedor de Hyper-V permite administrar y recuperar información acerca de las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-171">The Hyper-V provider allows you to manage and retrieve information about virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-173">El proveedor de Hyper-V (V2) amplía el proveedor de [Hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) .</span><span class="sxs-lookup"><span data-stu-id="bc4d2-173">The Hyper-V (V2) provider extends the [Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) provider.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="bc4d2-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-175">Expone interfaces de programación que se pueden utilizar para consultar y configurar la metabase de IIS.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-175">Exposes programming interfaces that can be used to query and configure the IIS metabase.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Servidor de administración de direcciones de protocolo (IPAM) de Internet](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Internet Protocol Address Management (IPAM) Server](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-177">El proveedor de servidores IPAM permite a los desarrolladores administrar IPAM a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-177">The IPAM Server Provider enables developers to manage IPAM through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[Proveedor de rutas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-179">El proveedor de rutas IP preinstalado proporciona información de enrutamiento de red IPV4, incluida la información disponible a través del comando **Route Print** .</span><span class="sxs-lookup"><span data-stu-id="bc4d2-179">The preinstalled IP Route provider supplies IPV4 network routing information, including (but not limited to) the information available through the **route print** command.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Interfaz de administración de plataforma inteligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-181">Proporciona datos IPMI de las operaciones del controlador de administración de placa base (BMC).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-181">Supplies IPMI data from Baseboard Management Controller (BMC) operations.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI Target Server](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-183">El proveedor del servidor de destino iSCSI es compatible con una interfaz WMI para administrar el servidor de destino iSCSI de Microsoft, como la creación de discos virtuales y su presentación en el cliente.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-183">The iSCSI Target Server provider supports a WMI interface for managing the Microsoft iSCSI Target Server, such as creating virtual disks, and for presenting them to the client.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Objeto de trabajo](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Job Object](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-185">El proveedor de objetos de trabajo admite el acceso a datos sobre objetos de trabajo de kernel con nombre.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-185">The Job Object provider supports access to data about named kernel job objects.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Seguimiento de kernel](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Kernel Trace](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-187">El proveedor de eventos de seguimiento de kernel preinstalado permite ver eventos de seguimiento de kernel en la creación de procesos, la finalización de procesos, la creación de subprocesos, la terminación de subprocesos y la carga de módulos.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-187">The preinstalled Kernel Trace event provider allows you to see kernel trace events on Process creation, Process termination, Thread creation, Thread termination and module load.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span><span class="sxs-lookup"><span data-stu-id="bc4d2-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-189">Proporciona clases que crean, registran, configuran y administran aplicaciones de protocolo de inicio de sesión (SIP) personalizadas con [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-189">Provides classes that create, register, configure, manage custom Session Initiation Protocol (SIP) applications with the [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registro de herramientas de administración](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Management Tools Registry](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-191">El proveedor del registro de las herramientas de administración proporciona acceso remoto al registro.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-191">The Management Tools Registry provider provides remote access to the registry.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Administrador de tareas de herramientas de administración](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Management Tools Task Manager](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-193">El proveedor del administrador de tareas de las herramientas de administración proporciona acceso y administración de los datos del administrador de tareas.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-193">The Management Tools Task Manager provider provides access and management of the Task Manager data.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Aplicación MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM Application](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-195">El proveedor de aplicaciones de administración de dispositivos móviles (MDM) administra las aplicaciones en los dispositivos que están suscritos al servicio MDM.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-195">The Mobile Device Management (MDM) application provider manages applications on devices that are subscribed to the MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[Puente MDM](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM Bridge](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-197">El proveedor de puente de MDM habilita la administración de MDM de un puente de red.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-197">The MDM Bridge provider enables MDM management of a network bridge.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Configuración de MDM](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM Settings](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-199">El proveedor de configuración de MDM habilita la administración de la configuración de los dispositivos inscritos con un servicio MDM.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-199">The MDM Settings Provider enables management of settings on devices enrolled with a MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-201">El proveedor [msft \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) expone una clase que define una clase de vista para un sistema de equipo físico.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-201">The [MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) provider exposes a class that defines a view class for a physical computer system.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-203">La sección del proveedor [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) proporciona información de referencia para las clases de proveedor de MsNetImPlatform implementadas en NdisIMPlatCim.dll.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-203">The [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) provider section provides reference information for MsNetImPlatform provider classes implemented in NdisIMPlatCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-205">El proveedor [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) admite clases que tienen acceso a los adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-205">The [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) provider supports classes that access network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-207">En esta sección se proporciona información de referencia para las clases de proveedor [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) .</span><span class="sxs-lookup"><span data-stu-id="bc4d2-207">This section provides reference information for [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) Provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-209">Proporciona información de referencia para las clases de proveedor [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) .</span><span class="sxs-lookup"><span data-stu-id="bc4d2-209">Provides reference information for [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-211">El proveedor [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) admite clases que interactúan con la infraestructura de la caché de rama.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-211">The [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) provider supports classes that interact with the Branch Cache infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-213">El proveedor [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) proporciona datos para los datos de calidad de servicio (QoS) y de configuración de QoS de la red.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-213">The [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) provider supplies data for network quality of service (QoS) and QoS setting data.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-215">En esta sección se proporciona información de referencia para las clases de proveedor NetSwitchTeam declaradas en NetSwitchTeam. mof y se implementan en NetSwitchTeamCim.dll.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-215">This section provides reference information for NetSwitchTeam provider classes declared in NetSwitchTeam.mof and implemented in NetSwitchTeamCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-217">El proveedor NetTCPIP admite clases que interactúan con conexiones TCPIP.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-217">The NetTCPIP provider supports classes that interact with TCPIP connections.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-219">En esta sección se proporciona información de referencia para las clases de proveedor de NetTtCim definidas en NetTtCim. mof y se implementan en NetTtCim.dll.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-219">This section provides reference information for NetTtCim provider classes defined in NetTtCim.mof and implemented in NetTtCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-221">El proveedor NetWNV admite clases que interactúan con las tecnologías de virtualización de red.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-221">The NetWNV provider supports classes that interact with net virtualization technologies.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Protección de acceso a redes](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Network Access Protection](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-223">El proveedor de protección de acceso a redes expone una plataforma para el acceso protegido a redes privadas.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-223">The Network Access Protection provider exposes a platform for protected access to private networks.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Equilibrio de carga de red](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Network Load Balancing](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-225">El proveedor de equilibrio de carga de red (NLB) permite la administración de un clúster NLB.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-225">The Network Load Balancing (NLB) Provider enables management of a NLB cluster.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Servidor de NetworkController](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[NetworkController Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-227">El proveedor habilita la administración de un servidor de controladora de red.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-227">The provider enables management of a network controller server.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-229">El proveedor para NFS permite crear herramientas y scripts para configurar y supervisar el sistema de archivos de red de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-229">The provider for NFS allows you to create tools and scripts for configuring and monitoring the Windows Network File System.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Comandos](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-231">El proveedor de ping proporciona acceso a la información de estado proporcionada por el comando ping estándar.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-231">The Ping provider supplies access to the status information provided by the standard ping command.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Directivas](/previous-versions/windows/desktop/policmanprov/policy-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Policy](/previous-versions/windows/desktop/policmanprov/policy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-233">Proporciona extensiones a la Directiva de grupo y permite mejoras en la aplicación de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-233">Provides extensions to group policy, and permits refinements in the application of policy.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Medidor de energía](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Power Meter](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-235">El proveedor de medición de energía es compatible con la interfaz de medición y presupuesto (PMB).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-235">The Power Meter provider supports the Power Metering and Budgeting (PMB) interface.</span></span> <span data-ttu-id="bc4d2-236">Estas clases son la interfaz principal para la consulta de la información de la interfaz de medición de energía (PMI) de los medidores de energía subyacentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-236">These classes are the primary interface for the query of Power Meter Interface (PMI) information from underlying power meters on the system.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Directiva de energía](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Power Policy](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-238">El proveedor de directivas de energía proporciona a las clases la capacidad de administrar de forma remota toda la infraestructura de directivas de energía.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-238">The Power Policy provider provides classes the ability to remotely manage all the power policy infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-240">El proveedor [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) proporciona clases para administrar el acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-240">The [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) provider provides classes to manage Remote Access.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-242">El proveedor [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) proporciona clases para administrar el servidor de acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-242">The [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) provider provides classes to manage the Remote Access Server.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-244">El proveedor [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) expone las métricas de confiabilidad del registro de eventos de Windows y del sistema.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-244">The [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) provider exposes system and Windows Event Log reliability metrics.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Servicios de Escritorio remoto](/windows/desktop/TermServ/terminal-services-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Remote Desktop Services](/windows/desktop/TermServ/terminal-services-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-246">Habilita la administración coherente del servidor en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-246">Enables consistent server administration in a Remote Desktop Services environment.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-248">Define clases que permiten escribir scripts y código para modificar la configuración del servidor de informes y el Administrador de informes.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-248">Defines classes that allow you to write scripts and code to modify the settings of the report server and the Report Manager.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Conjunto resultante de directivas (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Resultant Set of Policy (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-250">Proporciona métodos para planear y depurar la configuración de directivas en una situación de si.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-250">Supplies methods to plan and debug policy settings in a what-if situation.</span></span> <span data-ttu-id="bc4d2-251">Estos métodos permiten a los administradores determinar fácilmente la combinación de opciones de directiva que se aplican o se aplican a un usuario o equipo.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-251">These methods allow administrators to determine easily the combination of policy settings that apply to, or will apply to, a user or computer.</span></span> <span data-ttu-id="bc4d2-252">Esto se conoce como el conjunto resultante de directivas (RSoP).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-252">This is known as the Resultant Set of Policy (RSoP).</span></span> <span data-ttu-id="bc4d2-253">Para obtener más información, consulte [About the RSoP WMI Method Provider](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) y [RSoP WMI classes](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-253">For more information, see [About the RSoP WMI Method Provider](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) and [RSoP WMI Classes](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Bursátil](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Security](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-255">Recupera o cambia la configuración de seguridad que controla la propiedad, la auditoría y los derechos de acceso a archivos, directorios y recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-255">Retrieves or changes security settings that control ownership, auditing, and access rights to files, directories, and shares.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-257">[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) expone la funcionalidad de implementación.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-257">The [ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) exposes deployment functionality.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Sesión](/previous-versions/windows/desktop/wmipsess/session-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Session](/previous-versions/windows/desktop/wmipsess/session-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-259">Administra sesiones y conexiones de red.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-259">Manages network sessions and connections.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Instantánea](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Shadow Copy](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-261">Proporciona funciones de administración para las instantáneas de la característica carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-261">Supplies management functions for the Shadow Copies of the Shared Folders feature.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Aprovisionamiento de máquinas virtuales blindadas](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Shielded VM Provisioning](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-263">El proveedor de aprovisionamiento de máquinas virtuales blindadas permite que un controlador de tejido inicie el aprovisionamiento seguro de una máquina virtual blindada en un host de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-263">The Shielded VM Provisioning provider enables a fabric controller to start the secure provisioning of a shielded VM on a Hyper-V host.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Servicio de aprovisionamiento de máquinas virtuales blindadas](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Shielded VM Provisioning Service](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-265">El proveedor habilita el aprovisionamiento de una máquina virtual blindada.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-265">The provider enables provisioning of a shielded virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Administración de SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB Management](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-267">La API de administración de SMB proporciona clases y métodos para administrar los recursos compartidos y el acceso compartido.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-267">The SMB Management API provides classes and methods to manage shares and share access.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-268"><span id="SNMP"></span><span id="snmp"></span>[Procese](/windows/desktop/WmiSdk/snmp-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-268"><span id="SNMP"></span><span id="snmp"></span>[SNMP](/windows/desktop/WmiSdk/snmp-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-269">Asigna objetos de Protocolo simple de administración de redes (SNMP) que se definen en objetos de esquema de base de información de administración (MIB) a clases.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-269">Maps Simple Network Management Protocol (SNMP) objects that are defined in Management Information Base (MIB) schema objects to classes.</span></span> <span data-ttu-id="bc4d2-270">Para obtener más información, consulte [configuración del entorno WMI SNMP](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-270">For more information, see [Setting up the WMI SNMP Environment](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Registro de inventario de software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Software Inventory Logging](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-272">El proveedor de registro de inventario de software recopila datos de licencias sobre el software instalado en un servidor de Windows y proporciona acceso remoto a los datos para que se puedan agregar fácilmente en un centro de datos.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-272">The Software Inventory Logging provider collects licensing data about software installed on a Windows Server, and provides remote access to the data so it can be aggregated easily by a datacenter.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Licencias de software para Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Software Licensing for Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-274">[Clases de licencias de software](/previous-versions/windows/desktop/sppwmi/software-license-provider-) utilizadas para Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-274">[Software Licensing Classes](/previous-versions/windows/desktop/sppwmi/software-license-provider-) used for Windows Vista.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Licencia de software](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Software License](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-276">El proveedor de licencias de software recupera datos de licencias de software.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-276">The Software Licensing provider retrieves software licensing data.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Volumen de almacenamiento](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Storage Volume](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-278">El proveedor de volumen de almacenamiento proporciona funciones de administración de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-278">The Storage Volume provider supplies volume management functions.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Réplica de almacenamiento](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Storage Replica](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-280">El proveedor habilita la administración de una réplica de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-280">The provider enables management of a storage replica.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-282">El proveedor del registro del sistema permite que las aplicaciones de administración recuperen y modifiquen los datos en el registro del sistema y reciban notificaciones cuando se produzcan cambios.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-282">The System Registry provider enables management applications to retrieve and modify data in the system registry, and receive notifications when changes occur.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Restaurar sistema](/windows/desktop/sr/system-restore-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[System Restore](/windows/desktop/sr/system-restore-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-284">Proporciona clases que configuran y usan la funcionalidad de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-284">Supplies classes that configure and use System Restore functionality.</span></span> <span data-ttu-id="bc4d2-285">Para obtener más información, consulte [configurar la restauración del sistema](/windows/desktop/sr/configuring-system-restore) y las [clases WMI de restaurar sistema](/windows/desktop/sr/system-restore-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-285">For more information, see [Configuring System Restore](/windows/desktop/sr/configuring-system-restore) and the [System Restore WMI Classes](/windows/desktop/sr/system-restore-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Módulo de plataforma segura](/windows/desktop/SecProv/trusted-platform-module-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-287">Proporciona acceso a los datos sobre un dispositivo de seguridad, representado por una instancia de [**\_ TPM de Win32**](/windows/desktop/SecProv/win32-tpm), que es la raíz de confianza para un sistema informático de plataforma segura de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-287">Provides access to data about a security device, represented by an instance of [**Win32\_TPM**](/windows/desktop/SecProv/win32-tpm), that is the root of trust for a Microsoft Windows trusted platform computer system.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-289">El proveedor [Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) es un proveedor de instancias que crea clases con información sobre las relaciones de confianza entre dominios.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-289">The [Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) provider is an instance provider that creates classes with information about the trust relationships between domains.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Registro de acceso de usuarios](/previous-versions/windows/desktop/ual/user-access-logging)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[User Access Logging](/previous-versions/windows/desktop/ual/user-access-logging)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-291">El registro de acceso de usuarios (UAL) es un marco común para que los roles de Windows Server informen de sus métricas de consumo respectivos.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-291">User Access Logging (UAL) is a common framework for Windows Server roles to report their respective consumption metrics.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-293">El proveedor [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) expone clases que proporcionan información sobre un perfil de usuario en un sistema Windows, así como el estado de mantenimiento de una carpeta de usuario redirigido.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-293">The [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) provider exposes classes that provide information about a user profile on a Windows system, as well as the health status of a redirected user folder.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Administración de estado de usuario](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[User State Management](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-295">El proveedor de administración de estado de usuario expone una API de administración y generación de informes para escenarios empresariales.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-295">The User State Management provider exposes a management and reporting API for enterprise scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[Visores](/windows/desktop/WmiSdk/view-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[View](/windows/desktop/WmiSdk/view-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-297">Crea nuevas instancias y métodos basados en instancias de otras clases.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-297">Creates new instances and methods based on instances of other classes.</span></span> <span data-ttu-id="bc4d2-298">Dos versiones del proveedor de vistas están disponibles en las plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-298">Two versions of the View provider are available on 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-300">El proveedor [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) expone una plataforma para automatizar la conectividad a un cliente de red privada virtual.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-300">The [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) provider exposes a platform for automating connectivity to a virtual private network client.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-301"><span id="WDM"></span><span id="wdm"></span>[TRANSMISIÓN](/windows/desktop/WmiCoreProv/wdm-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-301"><span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-302">Proporciona acceso a las clases, instancias, métodos y eventos de los controladores de hardware que cumplen con el Modelo de controlador de Windows (WDM).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-302">Provides access to the classes, instances, methods, and events of hardware drivers that conform to the Windows Driver Model (WDM).</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-304">El proveedor [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) expone características de filtrado y seguridad de la red.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-304">The [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) provider exposes network security and filtering features.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-306">El proveedor [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) expone información de firma digital sobre los controladores.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-306">The [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) provider exposes digital signature information about drivers.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-308">El proveedor [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) expone las marcas de tiempo actuales, locales y basadas en UTC en un sistema informático.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-308">The [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) provider exposes the current, local, and UTC-based timestamps on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Componentes de Windows Data Access (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-310">Proporciona la administración de WDAC.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-310">Provides management of WDAC.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-312">El proveedor de Windows Defender expone las características de seguridad de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-312">The Windows Defender provider exposes Windows Defender security features.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-314">El proveedor de Windows Installer, también conocido como proveedor MSI permite a las aplicaciones tener acceso a la información recopilada de las aplicaciones compatibles con Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-314">The Windows Installer provider, also known as the MSI provider allows applications to access information collected from Windows Installer compliant applications.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Activación de productos de Windows](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Product Activation](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-316">El proveedor de activación de productos de Windows (WPA) es una tecnología antipiratería destinada a reducir la copia casual del software.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-316">The Windows Product Activation (WPA) provider is an anti-piracy technology aimed at reducing the casual copying of software.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Administrador del servidor de Windows](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Server Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-318">El proveedor permite el acceso y la administración de la configuración controlada por la aplicación Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-318">The provider enables access to and management of the configuration controlled by the Server Manager application.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Administración de almacenamiento de Windows Server (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server Storage Management (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-320">El proveedor MsftStrgMan proporciona administración para los sistemas de almacenamiento en productos de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-320">The MsftStrgMan provider provides management for storage systems on Windows Server products.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Administración de almacenamiento de Windows (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows Storage Management (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-322">El proveedor StrgMgmt se puede usar para administrar una amplia gama de configuraciones de almacenamiento, desde tabletas hasta matrices de almacenamiento externo en servidores.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-322">The StrgMgmt provider can be used to manage a wide range of storage configurations, from tablets to external storage arrays on servers.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Herramienta de evaluación del sistema de Windows](/windows/desktop/WinSAT/winsat-mof-classes)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows System Assessment Tool](/windows/desktop/WinSAT/winsat-mof-classes)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-324">La herramienta de evaluación del sistema de Windows (WinSAT) expone una serie de clases que evalúa las características de rendimiento y las capacidades de un equipo.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-324">The Windows System Assessment Tool (WinSAT) exposes a number of classes that assesses the performance characteristics and capabilities of a computer.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[Núcleo de WMI](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI Core](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-326">El proveedor principal de WMI define las clases que componen la funcionalidad básica de WMI.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-326">The WMI Core provider defines classes that compose the core functionality of WMI.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-328">El proveedor [msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) admite proveedores.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-328">The [Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) provider supports providers.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Rendimiento de Win32 \_](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32\_Perf](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-330">La clase abstracta de rendimiento de [**\_ Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) es la clase base para las clases de contador de rendimiento [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) y [**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span><span class="sxs-lookup"><span data-stu-id="bc4d2-330">The [**Win32\_Perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) abstract class is the base class for the performance counter classes [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) and [**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span></span> <span data-ttu-id="bc4d2-331">Define las propiedades de frecuencia y marca de tiempo necesarias usadas en los algoritmos de tipo de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-331">It defines the required timestamp and frequency properties used in the CounterType algorithms for the performance counter classes.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-333">Una clase base abstracta para las clases de datos calculadas preinstaladas.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-333">An abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-335">La clase de contador de rendimiento [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) es la clase base abstracta para todas las clases de contador de rendimiento sin procesar concretas.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-335">The performance counter class [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) is the abstract base class for all concrete raw performance counter classes.</span></span> <span data-ttu-id="bc4d2-336">Para que aparezca en el monitor de sistema, las clases de contador de rendimiento se deben agregar al \\ espacio de nombres "root CIMv2" y derivarse de **Win32 \_ PerfRawData**.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-336">To appear in System Monitor, performance counter classes must be added to the "Root\\CIMv2" namespace and derived from **Win32\_PerfRawData**.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-338">Crea las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)de WMI.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-338">Creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="bc4d2-339">El proveedor WMIPerfInst proporciona los datos de forma dinámica a estas clases de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-339">Data is dynamically supplied to these performance classes by the WMIPerfInst provider.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-341">Proporciona datos del contador de rendimiento sin formato y con formato de forma dinámica desde las definiciones de [clase de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) .</span><span class="sxs-lookup"><span data-stu-id="bc4d2-341">Supplies raw and formatted performance counter data dynamically from [Performance Counter Class](/windows/desktop/CIMWin32Prov/performance-counter-classes) definitions.</span></span>

</dd> <dt>

<span data-ttu-id="bc4d2-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Carpetas de trabajo](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span><span class="sxs-lookup"><span data-stu-id="bc4d2-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Work Folders](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span></span>
</dt> <dd>

<span data-ttu-id="bc4d2-343">Carpetas de trabajo se usa para sincronizar archivos con varios equipos y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="bc4d2-343">Work Folders is used to synchronize files with multiple PCs and mobile devices.</span></span>

</dd> </dl>

 

 
