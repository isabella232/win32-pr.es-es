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
# <a name="whats-new-in-windowsvista"></a>Novedades de Windows Vista

A partir de Windows Vista, WMI contiene muchas características nuevas basadas en las solicitudes de los usuarios de WMI.

-   [Nueva herramienta de solución de problemas](#new-troubleshooting-tool)
-   [Nuevas características de seguridad de Windows Vista](#new-security-features-in-windows-vista)
-   [Otras características nuevas de Windows Vista](#other-new-features-in-windows-vista)
-   [Temas relacionados](#related-topics)

## <a name="new-troubleshooting-tool"></a>Nueva herramienta de solución de problemas

Hay disponible una nueva herramienta de solución de problemas para su descarga.

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>Utilidad de diagnóstico de WMI
</dt> <dd>

Esta utilidad examina el estado actual del servicio WMI y los componentes relacionados, la configuración de DCOM y la configuración del registro en el equipo local. La utilidad informa de los problemas y ofrece sugerencias para la reparación. Para obtener más información y descargar la utilidad, consulte [utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>Nuevas características de seguridad de Windows Vista

En la lista siguiente se enumeran las nuevas características de seguridad de WMI que están disponibles en Windows Vista.

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Seguimiento y registro de eventos
</dt> <dd>

El servicio WMI ya no usa la mayoría de los [archivos de registro de WMI](wmi-log-files.md). En su lugar, utiliza el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) y los eventos están disponibles a través de la interfaz de usuario de **visor de eventos** o la herramienta de línea de comandos wevtutil. Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Configuración de la seguridad del espacio de nombres WMI en el archivo MOF
</dt> <dd>

El calificador **NamespaceSecuritySDDL** se puede usar para proteger cualquier espacio de nombres. Para obtener más información, vea [establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Auditoría de seguridad de espacios de nombres de WMI
</dt> <dd>

WMI utiliza las listas de control de acceso (SACL) del sistema de espacio de nombres para auditar la actividad de los espacios de nombres y notificar eventos al registro de eventos de seguridad. Para obtener más información, consulte [acceso a espacios de nombres WMI](access-to-wmi-namespaces.md) y [configuración de descriptores de seguridad de espacios de nombres](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Obtener y establecer métodos de descriptor de seguridad para objetos protegibles
</dt> <dd>

Se han agregado nuevos métodos que admiten scripts para obtener y establecer descriptores de seguridad en la [**\_ impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer), el [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)y [**\_ \_ SystemSecurity**](--systemsecurity.md). Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipular descriptores de seguridad en scripts
</dt> <dd>

La [**clase \_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) tiene métodos que permiten que los scripts conviertan los descriptores de seguridad binarios en objetos protegibles en objetos descriptores [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) o cadenas del lenguaje de [definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Control de cuentas de usuario
</dt> <dd>

Control de cuentas de usuario (UAC) afecta a los datos de WMI que se devuelven, el acceso remoto y el modo en que se deben ejecutar los scripts. Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md). Para obtener más información acerca de UAC, vea [Introducción con control de cuentas de usuario en Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>Otras características nuevas de Windows Vista

En la lista siguiente se enumeran las nuevas características de WMI que están disponibles en Windows Vista.

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Nuevos proveedores de datos de contadores de rendimiento
</dt> <dd>

El proceso de detección automática/purga (ADAP) ya no transfiere objetos de contador de rendimiento a clases de rendimiento de WMI en el repositorio WMI. Para obtener más información, consulte [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md). El [proveedor WMIPerfClass](wmiperfclass-provider.md) crea las clases de contador de rendimiento de WMI. El [proveedor WMIPerfInst](wmiperfinst-provider.md)proporciona los datos de forma dinámica a estas clases de rendimiento de WMI.

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexador para colecciones
</dt> <dd>

El método [**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md) devuelve el objeto asociado a un índice especificado en una colección.

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Compatibilidad con IPv6 e IPv4
</dt> <dd>

Las clases de red y del [proveedor de rutas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) de WMI proporcionan datos para las direcciones IPv4. A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las capacidades de red IPv6. Para obtener más información, consulte [compatibilidad con IPv6 e IPv4 en WMI](ipv6-and-ipv4-support-in-wmi.md).

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Cambios en las conexiones remotas
</dt> <dd>

La conexión a un espacio de nombres WMI en un equipo remoto que ejecuta Windows Vista puede requerir cambios en la configuración del [firewall de Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), el control de [cuentas de usuario](/previous-versions/aa905108(v=msdn.10))o DCOM. Para obtener más información, vea [conectarse a WMI de forma remota a partir de vista](connecting-to-wmi-remotely-starting-with-vista.md).

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Cambios en [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

En el caso de los sistemas que se ejecutan en el sistema operativo Windows Vista y versiones posteriores, esta clase devuelve solo las actualizaciones proporcionadas por el servicio basado en componentes (CBS). Estas actualizaciones no aparecen en el registro. [**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)no devuelve las actualizaciones proporcionadas por Windows Installer (MSI) o el [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) .

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Habilitación y deshabilitación de una NIC
</dt> <dd>

[**Win32 \_ El adaptador de red tiene nuevos**](/windows/desktop/CIMWin32Prov/win32-networkadapter) métodos para habilitar y deshabilitar el adaptador de red.

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Cambios del proveedor de Windows Installer
</dt> <dd>

[**Win32 \_ El producto**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) tiene nuevas propiedades y métodos para proporcionar más datos sobre el producto.

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Nuevas clases de monitor de pantalla
</dt> <dd>

[Las clases de pantalla de monitor](/windows/desktop/WmiCoreProv/wmi-core-provider-) contienen datos proporcionados por el [proveedor de WDM](/windows/desktop/WmiCoreProv/wdm-provider) que proporciona datos sobre monitores de pantalla.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Proveedor de interfaz de administración de plataforma inteligente
</dt> <dd>

El proveedor de WMI [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) proporciona datos de las operaciones del controlador de administración de placa base (BMC) al sistema operativo. El proveedor proporciona información a las clases de información de administración de plataforma inteligente, que proporcionan datos de sensores y datos de mensajes del registro de eventos del sistema de BMC (SEL).

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detección de procesadores multithreading y multinúcleo
</dt> <dd>

[**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) El [**\_ procesador**](/windows/desktop/CIMWin32Prov/win32-processor) de ComputerSystem y Win32 tiene nuevas propiedades que le permiten escribir scripts para determinar si el sistema del equipo tiene procesadores multithreading o multiproceso.

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Mensajes de eventos
</dt> <dd>

Windows Vista tiene nuevos mensajes de eventos. Para obtener más información, vea [eventos de WMI](wmi-events.md).

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Mejoras en el inventario
</dt> <dd>

Muchas clases de hardware han tenido cambios para mejorar el inventario de hardware. Por ejemplo, se ha agregado una propiedad de número de serie a [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) y [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Nuevos modelos de hospedaje de proveedor
</dt> <dd>

Se han agregado nuevos modelos de hospedaje de proveedor para Windows Vista. Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 
