---
description: Novedades de Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: Novedades de Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682e4f125fcc11a1b6679af7df78fddba5a766ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967036"
---
# <a name="whats-new-in-windows-7"></a>Novedades de Windows 7

## <a name="new-security-feature-in-windows-7"></a>Nueva característica de seguridad en Windows 7

A continuación se muestra la nueva Windows de seguridad de Instrumental de administración de administración de recursos (WMI) que está disponible en Windows 7.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Control de la seguridad del proveedor
</dt> <dd>

Cambios para mejorar la seguridad del proceso de host del proveedor compartido wmi (wmiprvse.exe). Estos cambios introducen tres nuevas directivas de grupo y dos modos de ejecución para el host compartido wmi, que se denominan modos seguros y compatibles. Para obtener más información, vea [Claves del Registro para controlar la seguridad del proveedor.](registry-keys-for-controlling-provider-security-.md)

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Otras características nuevas o actualizadas de Windows 7

En la lista siguiente se enumeran las nuevas características de WMI que están disponibles en Windows 7.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>Compatibilidad de esquemas CIM
</dt> <dd>

A partir Windows 7, WMI es compatible con la versión 2.17.1 del esquema Modelo de información común (CIM). Para obtener más información, vea [Compatibilidad de esquemas CIM.](cim-schema-compatibility.md)

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Recorrido de asociación entre espacios de nombres
</dt> <dd>

WMI implementó un mecanismo estándar para detectar perfiles mediante el esquema CIM. Para obtener más información, vea [Cross Namespace Association Traversal](cross-namespace-association-traversal.md).

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Proveedores de asociación
</dt> <dd>

Información sobre cómo escribir y registrar un proveedor de asociación. Los proveedores de asociación se usan para exponer perfiles estándar, como un perfil de energía. Para obtener más información, vea [Escribir un proveedor de asociación para la interoperabilidad](writing-an-association-provider-for-interop.md).

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>Estado de característica opcional
</dt> <dd>

WMI implementó la [**clase \_ OptionalFeature de Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Esta clase consulta y devuelve el estado de las características opcionales que están presentes en un equipo. Para ver consultas de ejemplo Windows PowerShell, vea [Consulta del estado de características opcionales.](querying-the-status-of-optional-features.md)

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Cambio del comportamiento predeterminado de la característica de repositorio AutoRestore
</dt> <dd>

WMI tiene una nueva clave del Registro para habilitar o deshabilitar la característica de repositorio AutoRestore. Para obtener más información, vea [Clave del Registro para la configuración del repositorio.](registry-key-for-repository-configuration.md)

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>Nuevas Windows PowerShell clases de comandos
</dt> <dd>

Windows PowerShell cmdlets permiten a los usuarios completar las tareas de un extremo a otro necesarias para administrar equipos locales y remotos. Para obtener más información, vea [Referencia administrada para clases de comandos de PowerShell WMI.](managed-reference-for-wmi-powershell-command-classes.md)

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Nuevo mecanismo para conectarse a equipos remotos
</dt> <dd>

Windows PowerShell proporciona un mecanismo sencillo para conectarse a WMI en un equipo remoto. Para obtener más información, vea [Conectarse a WMI en un equipo remoto mediante PowerShell.](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Cambios en las clases de licencias de software
</dt> <dd>

Las [clases de licencias de software](/previous-versions/windows/desktop/sppwmi/software-license-provider-) tienen nuevos métodos y propiedades para proporcionar más datos de licencias de software. Además, se ha agregado la clase [**SoftwareLicensingTokenActivationLicense.**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense)

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Nuevas clases de medición de energía y presupuestación
</dt> <dd>

[Las clases de medición](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) de energía y presupuestación son la interfaz principal para la consulta de información de la interfaz de medidor de energía (PMI) de los medidores de energía subyacentes del sistema.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Nuevas clases de directiva de energía
</dt> <dd>

[Las clases de directivas de](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) energía permiten la administración remota de todas las infraestructuras de directivas de energía.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Cambios en la [**clase \_ ServerFeature de Win32**](win32-serverfeature.md)
</dt> <dd>

Se **actualizó** la propiedad ID de [**\_ Win32 ServerFeature.**](win32-serverfeature.md)

</dd> </dl>

Para obtener más información sobre las nuevas características de versiones anteriores del sistema operativo, vea [Novedades de Windows Vista](what-s-new-in-windows-vista.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 
