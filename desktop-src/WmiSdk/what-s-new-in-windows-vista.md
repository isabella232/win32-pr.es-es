---
description: A partir de Windows Vista, WMI contiene muchas características nuevas basadas en las solicitudes de los usuarios wmi.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Novedades de Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967028"
---
# <a name="whats-new-in-windowsvista"></a>Novedades de Windows Vista

A partir de Windows Vista, WMI contiene muchas características nuevas basadas en las solicitudes de los usuarios wmi.

-   [Nueva herramienta de solución de problemas](#new-troubleshooting-tool)
-   [Nuevas características de seguridad en Windows Vista](#new-security-features-in-windows-vista)
-   [Otras características nuevas de Windows Vista](#other-new-features-in-windows-vista)
-   [Temas relacionados](#related-topics)

## <a name="new-troubleshooting-tool"></a>Nueva herramienta de solución de problemas

Hay disponible una nueva herramienta de solución de problemas para su descarga.

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>Utilidad de diagnóstico de WMI
</dt> <dd>

Esta utilidad examina el estado actual del servicio WMI y los componentes relacionados, la configuración de DCOM y la configuración del Registro en el equipo local. La utilidad notifica problemas y ofrece sugerencias para la reparación. Para obtener más información y descargar la utilidad , [vea Utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>Nuevas características de seguridad en Windows Vista

En la lista siguiente se enumeran las nuevas características de seguridad wmi que están disponibles en Windows Vista.

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Seguimiento y registro de eventos
</dt> <dd>

El servicio WMI ya no usa la mayoría de los [archivos de registro wmi.](wmi-log-files.md) En su lugar, usa [Seguimiento](/windows/desktop/ETW/event-tracing-portal) de eventos  (ETW) y los eventos están disponibles a través de la interfaz de usuario Visor de eventos o la herramienta de línea de comandos Wevtutil. Para obtener más información, vea [Seguimiento de la actividad WMI.](tracing-wmi-activity.md)

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Establecer la seguridad del espacio de nombres WMI en el archivo MOF
</dt> <dd>

El **calificador NamespaceSecuritySDDL** se puede usar para proteger cualquier espacio de nombres. Para obtener más información, vea [Establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Auditoría de seguridad de espacios de nombres WMI
</dt> <dd>

WMI usa las listas de control de acceso del sistema de espacios de nombres (SACL) para auditar la actividad del espacio de nombres y notificar eventos al registro de eventos de seguridad. Para obtener más información, vea [Acceso a espacios de nombres WMI y](access-to-wmi-namespaces.md) Establecer [descriptores de seguridad de espacio de nombres](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Métodos de descriptor de seguridad Get y Set para objetos protegibles
</dt> <dd>

Se han agregado nuevos métodos que pueden incluirse en scripts para obtener y establecer descriptores de seguridad a Impresora [**Win32, \_**](/windows/desktop/CIMWin32Prov/win32-printer)Servicio [**\_ Win32,**](/windows/desktop/CIMWin32Prov/win32-service) [**StdRegProv,**](/previous-versions/windows/desktop/regprov/stdregprov) [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)y [**\_ \_ SystemSecurity**](--systemsecurity.md). Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](changing-access-security-on-securable-objects.md)

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipular descriptores de seguridad en scripts
</dt> <dd>

La clase [**\_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) tiene métodos que permiten a los scripts convertir descriptores [](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de seguridad binarios en objetos protegibles en objetos [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) o cadenas del lenguaje de definición de descriptor de seguridad. Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](changing-access-security-on-securable-objects.md)

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Control de cuentas de usuario
</dt> <dd>

El Control de cuentas de usuario (UAC) afecta a qué datos WMI se devuelven, al acceso remoto y a cómo se deben ejecutar los scripts. Para obtener más información, vea [Control de cuentas de usuario y WMI.](user-account-control-and-wmi.md) Para obtener más información sobre UAC, vea Tareas iniciales control de cuentas de [usuario en Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>Otras características nuevas de Windows Vista

En la lista siguiente se enumeran las nuevas características wmi que están disponibles en Windows Vista.

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Nuevos proveedores de datos de contadores de rendimiento
</dt> <dd>

El proceso AutoDiscovery/AutoPurge (ADAP) ya no transfiere objetos de contador de rendimiento a clases de rendimiento WMI en el repositorio WMI. Para obtener más información, vea [Bibliotecas de rendimiento y WMI.](performance-libraries-and-wmi.md) El [proveedor WMIPerfClass crea](wmiperfclass-provider.md) las clases de contador de rendimiento wmi. El proveedor [WMIPerfInst](wmiperfinst-provider.md)proporciona dinámicamente datos a estas clases de rendimiento WMI.

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexador para colecciones
</dt> <dd>

El [**método SWbemObject.ItemIndex**](swbemobjectset-itemindex.md) devuelve el objeto asociado a un índice especificado en una colección.

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Compatibilidad con IPv6 e IPv4
</dt> <dd>

El proveedor [de rutas IP WMI](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) y las clases de red suministran datos para las direcciones IPv4. A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las funcionalidades de red IPv6. Para obtener más información, vea [Compatibilidad con IPv6 e IPv4 en WMI.](ipv6-and-ipv4-support-in-wmi.md)

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Cambios en las conexiones remotas
</dt> <dd>

La conexión a un espacio de nombres WMI en un equipo remoto que ejecuta Windows Vista puede requerir cambios en la configuración de Windows [Firewall,](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx) [Control](/previous-versions/aa905108(v=msdn.10))de cuentas de usuario o DCOM. Para obtener más información, vea [Conectarse a WMI de forma remota a partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md).

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Cambios en [ **\_ QuickFixEngineering de Win32**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

Para los sistemas que se ejecutan en Windows Vista y en el sistema operativo posterior, esta clase devuelve solo las actualizaciones proporcionadas por el servicio basado en componentes (CBS). Estas actualizaciones no aparecen en el Registro. Las actualizaciones proporcionadas por Windows Installer (MSI) o [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) no se devuelven mediante [**\_ QuickFixEngineering de Win32.**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Habilitación y deshabilitación de una NIC
</dt> <dd>

[**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) tiene nuevos métodos para habilitar y deshabilitar el adaptador de red.

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Cambios en el proveedor del instalador
</dt> <dd>

[**Win32 \_ El**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) producto tiene nuevas propiedades y métodos para proporcionar más datos sobre el producto.

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Nuevas clases de monitor de pantalla
</dt> <dd>

[Las clases de visualización de](/windows/desktop/WmiCoreProv/wmi-core-provider-) monitor contienen datos proporcionados por el proveedor de [WDM](/windows/desktop/WmiCoreProv/wdm-provider) que proporciona datos sobre los monitores de pantalla.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Proveedor de interfaz de administración de plataforma inteligente
</dt> <dd>

El proveedor [DE IPMI wmi](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) proporciona datos de las operaciones del controlador de administración de placa base (BMC) al sistema operativo. El proveedor proporciona información a las clases de información de intelligent platform management, que proporcionan datos de sensores y datos de mensajes del registro de eventos del sistema BMC (SEL).

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detección de hyperthreading y procesadores de varios núcleos
</dt> <dd>

[**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) y el procesador [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-processor) tienen nuevas propiedades que permiten escribir scripts para determinar si el sistema del equipo tiene procesadores multinúcleo o hyperthreading.

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Mensajes de evento
</dt> <dd>

Windows Vista tiene nuevos mensajes de evento. Para obtener más información, vea [Eventos WMI](wmi-events.md).

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Mejoras en el inventario
</dt> <dd>

Muchas clases de hardware han tenido cambios para mejorar el inventario de hardware. Por ejemplo, se ha agregado una propiedad de número de serie a [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) y [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Nuevos modelos de hospedaje de proveedores
</dt> <dd>

Se han agregado nuevos modelos de hospedaje de proveedor para Windows Vista. Para obtener más información, vea [Provider Hosting and Security](provider-hosting-and-security.md).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 
