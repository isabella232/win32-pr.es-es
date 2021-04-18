---
description: A partir de Windows Vista, WMI contiene muchas características nuevas basadas en las solicitudes de los usuarios de WMI.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Novedades de Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717113"
---
# <a name="whats-new-in-windowsvista"></a><span data-ttu-id="11d99-103">Novedades de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11d99-103">Whats New in Windows�Vista</span></span>

<span data-ttu-id="11d99-104">A partir de Windows Vista, WMI contiene muchas características nuevas basadas en las solicitudes de los usuarios de WMI.</span><span class="sxs-lookup"><span data-stu-id="11d99-104">Starting with Windows Vista, WMI contains many new features based upon requests by WMI users.</span></span>

-   [<span data-ttu-id="11d99-105">Nueva herramienta de solución de problemas</span><span class="sxs-lookup"><span data-stu-id="11d99-105">New Troubleshooting Tool</span></span>](#new-troubleshooting-tool)
-   [<span data-ttu-id="11d99-106">Nuevas características de seguridad de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11d99-106">New Security Features in Windows Vista</span></span>](#new-security-features-in-windows-vista)
-   [<span data-ttu-id="11d99-107">Otras características nuevas de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11d99-107">Other New Features in Windows Vista</span></span>](#other-new-features-in-windows-vista)
-   [<span data-ttu-id="11d99-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11d99-108">Related topics</span></span>](#related-topics)

## <a name="new-troubleshooting-tool"></a><span data-ttu-id="11d99-109">Nueva herramienta de solución de problemas</span><span class="sxs-lookup"><span data-stu-id="11d99-109">New Troubleshooting Tool</span></span>

<span data-ttu-id="11d99-110">Hay disponible una nueva herramienta de solución de problemas para su descarga.</span><span class="sxs-lookup"><span data-stu-id="11d99-110">A new troubleshooting tool is available for download.</span></span>

<dl> <dt>

<span data-ttu-id="11d99-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>Utilidad de diagnóstico de WMI</span><span class="sxs-lookup"><span data-stu-id="11d99-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span></span>
</dt> <dd>

<span data-ttu-id="11d99-112">Esta utilidad examina el estado actual del servicio WMI y los componentes relacionados, la configuración de DCOM y la configuración del registro en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="11d99-112">This utility examines the current state of the WMI service and related components, DCOM settings, and registry settings on the local computer.</span></span> <span data-ttu-id="11d99-113">La utilidad informa de los problemas y ofrece sugerencias para la reparación.</span><span class="sxs-lookup"><span data-stu-id="11d99-113">The utility reports problems and offers suggestions for repair.</span></span> <span data-ttu-id="11d99-114">Para obtener más información y descargar la utilidad, consulte [utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span><span class="sxs-lookup"><span data-stu-id="11d99-114">For more information and to download the utility, see [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span></span>

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a><span data-ttu-id="11d99-115">Nuevas características de seguridad de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11d99-115">New Security Features in Windows Vista</span></span>

<span data-ttu-id="11d99-116">En la lista siguiente se enumeran las nuevas características de seguridad de WMI que están disponibles en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11d99-116">The following list lists the new WMI security features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="11d99-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Seguimiento y registro de eventos</span><span class="sxs-lookup"><span data-stu-id="11d99-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Tracing and logging events</span></span>
</dt> <dd>

<span data-ttu-id="11d99-118">El servicio WMI ya no usa la mayoría de los [archivos de registro de WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-118">WMI service no longer uses most of the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="11d99-119">En su lugar, utiliza el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) y los eventos están disponibles a través de la interfaz de usuario de **visor de eventos** o la herramienta de línea de comandos wevtutil.</span><span class="sxs-lookup"><span data-stu-id="11d99-119">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="11d99-120">Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-120">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Configuración de la seguridad del espacio de nombres WMI en el archivo MOF</span><span class="sxs-lookup"><span data-stu-id="11d99-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Setting WMI namespace security in the MOF file</span></span>
</dt> <dd>

<span data-ttu-id="11d99-122">El calificador **NamespaceSecuritySDDL** se puede usar para proteger cualquier espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="11d99-122">The **NamespaceSecuritySDDL** qualifier can be used to secure any namespace.</span></span> <span data-ttu-id="11d99-123">Para obtener más información, vea [establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-123">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Auditoría de seguridad de espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="11d99-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Security Auditing of WMI namespaces</span></span>
</dt> <dd>

<span data-ttu-id="11d99-125">WMI utiliza las listas de control de acceso (SACL) del sistema de espacio de nombres para auditar la actividad de los espacios de nombres y notificar eventos al registro de eventos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="11d99-125">WMI uses the namespace system access control lists (SACL) to audit namespace activity and report events to the Security event log.</span></span> <span data-ttu-id="11d99-126">Para obtener más información, consulte [acceso a espacios de nombres WMI](access-to-wmi-namespaces.md) y [configuración de descriptores de seguridad de espacios de nombres](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-126">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Obtener y establecer métodos de descriptor de seguridad para objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="11d99-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get and Set security descriptor methods for securable objects</span></span>
</dt> <dd>

<span data-ttu-id="11d99-128">Se han agregado nuevos métodos que admiten scripts para obtener y establecer descriptores de seguridad en la [**\_ impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer), el [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)y [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-128">New scriptable methods to get and set security descriptors have been added to [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32\_DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting), and [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="11d99-129">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-129">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipular descriptores de seguridad en scripts</span><span class="sxs-lookup"><span data-stu-id="11d99-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulate Security Descriptors in scripts</span></span>
</dt> <dd>

<span data-ttu-id="11d99-131">La [**clase \_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) tiene métodos que permiten que los scripts conviertan los descriptores de seguridad binarios en objetos protegibles en objetos descriptores [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) o cadenas del lenguaje de [definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="11d99-131">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class has methods that allow scripts to convert binary security descriptors on securable objects to [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) objects or [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) strings.</span></span> <span data-ttu-id="11d99-132">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-132">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="11d99-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>User Account Control</span></span>
</dt> <dd>

<span data-ttu-id="11d99-134">Control de cuentas de usuario (UAC) afecta a los datos de WMI que se devuelven, el acceso remoto y el modo en que se deben ejecutar los scripts.</span><span class="sxs-lookup"><span data-stu-id="11d99-134">User Account Control (UAC) affects what WMI data is returned, remote access, and how scripts must be run.</span></span> <span data-ttu-id="11d99-135">Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-135">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span> <span data-ttu-id="11d99-136">Para obtener más información acerca de UAC, vea [Introducción con control de cuentas de usuario en Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span><span class="sxs-lookup"><span data-stu-id="11d99-136">For more information about UAC, see [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span></span>

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a><span data-ttu-id="11d99-137">Otras características nuevas de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11d99-137">Other New Features in Windows Vista</span></span>

<span data-ttu-id="11d99-138">En la lista siguiente se enumeran las nuevas características de WMI que están disponibles en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11d99-138">The following list lists new WMI features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="11d99-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Nuevos proveedores de datos de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="11d99-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>New performance counter data providers</span></span>
</dt> <dd>

<span data-ttu-id="11d99-140">El proceso de detección automática/purga (ADAP) ya no transfiere objetos de contador de rendimiento a clases de rendimiento de WMI en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="11d99-140">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="11d99-141">Para obtener más información, consulte [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-141">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span> <span data-ttu-id="11d99-142">El [proveedor WMIPerfClass](wmiperfclass-provider.md) crea las clases de contador de rendimiento de WMI.</span><span class="sxs-lookup"><span data-stu-id="11d99-142">The [WMIPerfClass Provider](wmiperfclass-provider.md) creates the WMI Performance Counter Classes.</span></span> <span data-ttu-id="11d99-143">El [proveedor WMIPerfInst](wmiperfinst-provider.md)proporciona los datos de forma dinámica a estas clases de rendimiento de WMI.</span><span class="sxs-lookup"><span data-stu-id="11d99-143">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst Provider](wmiperfinst-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexador para colecciones</span><span class="sxs-lookup"><span data-stu-id="11d99-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer for collections</span></span>
</dt> <dd>

<span data-ttu-id="11d99-145">El método [**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md) devuelve el objeto asociado a un índice especificado en una colección.</span><span class="sxs-lookup"><span data-stu-id="11d99-145">The [**SWbemObject.ItemIndex**](swbemobjectset-itemindex.md) method returns the object associated with a specified index into a collection.</span></span>

</dd> <dt>

<span data-ttu-id="11d99-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Compatibilidad con IPv6 e IPv4</span><span class="sxs-lookup"><span data-stu-id="11d99-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Support for IPv6 and IPv4</span></span>
</dt> <dd>

<span data-ttu-id="11d99-147">Las clases de red y del [proveedor de rutas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) de WMI proporcionan datos para las direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="11d99-147">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="11d99-148">A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las capacidades de red IPv6.</span><span class="sxs-lookup"><span data-stu-id="11d99-148">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span> <span data-ttu-id="11d99-149">Para obtener más información, consulte [compatibilidad con IPv6 e IPv4 en WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-149">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Cambios en las conexiones remotas</span><span class="sxs-lookup"><span data-stu-id="11d99-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Changes to remote connections</span></span>
</dt> <dd>

<span data-ttu-id="11d99-151">La conexión a un espacio de nombres WMI en un equipo remoto que ejecuta Windows Vista puede requerir cambios en la configuración del [firewall de Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), el control de [cuentas de usuario](/previous-versions/aa905108(v=msdn.10))o DCOM.</span><span class="sxs-lookup"><span data-stu-id="11d99-151">Connecting to a WMI namespace on a remote computer running Windows Vista may require changes to settings for [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [User Account Control](/previous-versions/aa905108(v=msdn.10)), or DCOM.</span></span> <span data-ttu-id="11d99-152">Para obtener más información, vea [conectarse a WMI de forma remota a partir de vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-152">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Cambios en [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span><span class="sxs-lookup"><span data-stu-id="11d99-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Changes to [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span></span>
</dt> <dd>

<span data-ttu-id="11d99-154">En el caso de los sistemas que se ejecutan en el sistema operativo Windows Vista y versiones posteriores, esta clase devuelve solo las actualizaciones proporcionadas por el servicio basado en componentes (CBS).</span><span class="sxs-lookup"><span data-stu-id="11d99-154">For systems running on the Windows Vista and later operating system, this class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="11d99-155">Estas actualizaciones no aparecen en el registro.</span><span class="sxs-lookup"><span data-stu-id="11d99-155">These updates are not listed in the registry.</span></span> <span data-ttu-id="11d99-156">[**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)no devuelve las actualizaciones proporcionadas por Windows Installer (MSI) o el [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) .</span><span class="sxs-lookup"><span data-stu-id="11d99-156">Updates supplied by Windows Installer (MSI) or the [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) are not returned by [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Habilitación y deshabilitación de una NIC</span><span class="sxs-lookup"><span data-stu-id="11d99-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Enabling and disabling a NIC</span></span>
</dt> <dd>

<span data-ttu-id="11d99-158">[**Win32 \_ El adaptador de red tiene nuevos**](/windows/desktop/CIMWin32Prov/win32-networkadapter) métodos para habilitar y deshabilitar el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="11d99-158">[**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) has new methods to enable and disable the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="11d99-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Cambios del proveedor de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="11d99-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Provider changes</span></span>
</dt> <dd>

<span data-ttu-id="11d99-160">[**Win32 \_ El producto**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) tiene nuevas propiedades y métodos para proporcionar más datos sobre el producto.</span><span class="sxs-lookup"><span data-stu-id="11d99-160">[**Win32\_Product**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) has new properties and methods to provide more data about the product.</span></span>

</dd> <dt>

<span data-ttu-id="11d99-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Nuevas clases de monitor de pantalla</span><span class="sxs-lookup"><span data-stu-id="11d99-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>New display monitor classes</span></span>
</dt> <dd>

<span data-ttu-id="11d99-162">[Las clases de pantalla de monitor](/windows/desktop/WmiCoreProv/wmi-core-provider-) contienen datos proporcionados por el [proveedor de WDM](/windows/desktop/WmiCoreProv/wdm-provider) que proporciona datos sobre monitores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="11d99-162">[Monitor Display Classes](/windows/desktop/WmiCoreProv/wmi-core-provider-) contain data supplied by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) that provides data about display monitors.</span></span>

</dd> <dt>

<span data-ttu-id="11d99-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Proveedor de interfaz de administración de plataforma inteligente</span><span class="sxs-lookup"><span data-stu-id="11d99-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider</span></span>
</dt> <dd>

<span data-ttu-id="11d99-164">El proveedor de WMI [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) proporciona datos de las operaciones del controlador de administración de placa base (BMC) al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="11d99-164">The WMI [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) supplies data from baseboard management controller (BMC) operations to the operating system.</span></span> <span data-ttu-id="11d99-165">El proveedor proporciona información a las clases de información de administración de plataforma inteligente, que proporcionan datos de sensores y datos de mensajes del registro de eventos del sistema de BMC (SEL).</span><span class="sxs-lookup"><span data-stu-id="11d99-165">The provider supplies information to the Intelligent Platform Management Information Classes, which provide sensors data and BMC System Event Log (SEL) message data.</span></span>

</dd> <dt>

<span data-ttu-id="11d99-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detección de procesadores multithreading y multinúcleo</span><span class="sxs-lookup"><span data-stu-id="11d99-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detecting hyperthreading and multicore processors</span></span>
</dt> <dd>

<span data-ttu-id="11d99-167">[**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) El [**\_ procesador**](/windows/desktop/CIMWin32Prov/win32-processor) de ComputerSystem y Win32 tiene nuevas propiedades que le permiten escribir scripts para determinar si el sistema del equipo tiene procesadores multithreading o multiproceso.</span><span class="sxs-lookup"><span data-stu-id="11d99-167">[**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) and [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor) have new properties that enable you to write scripts to determine whether the computer system has multicore or hyperthreading processors.</span></span>

</dd> <dt>

<span data-ttu-id="11d99-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Mensajes de eventos</span><span class="sxs-lookup"><span data-stu-id="11d99-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Event messages</span></span>
</dt> <dd>

<span data-ttu-id="11d99-169">Windows Vista tiene nuevos mensajes de eventos.</span><span class="sxs-lookup"><span data-stu-id="11d99-169">Windows Vista has new event messages.</span></span> <span data-ttu-id="11d99-170">Para obtener más información, vea [eventos de WMI](wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-170">For more information, see [WMI Events](wmi-events.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Mejoras en el inventario</span><span class="sxs-lookup"><span data-stu-id="11d99-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Inventory improvements</span></span>
</dt> <dd>

<span data-ttu-id="11d99-172">Muchas clases de hardware han tenido cambios para mejorar el inventario de hardware.</span><span class="sxs-lookup"><span data-stu-id="11d99-172">Many hardware classes have had changes to improve hardware inventory.</span></span> <span data-ttu-id="11d99-173">Por ejemplo, se ha agregado una propiedad de número de serie a [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) y [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span><span class="sxs-lookup"><span data-stu-id="11d99-173">For example, a serial number property was added to [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) and [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span></span>

</dd> <dt>

<span data-ttu-id="11d99-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Nuevos modelos de hospedaje de proveedor</span><span class="sxs-lookup"><span data-stu-id="11d99-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>New provider hosting models</span></span>
</dt> <dd>

<span data-ttu-id="11d99-175">Se han agregado nuevos modelos de hospedaje de proveedor para Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11d99-175">New provider hosting models have been added for Windows Vista.</span></span> <span data-ttu-id="11d99-176">Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="11d99-176">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="11d99-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11d99-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11d99-178">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="11d99-178">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
