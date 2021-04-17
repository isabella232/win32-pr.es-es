---
description: Las tablas siguientes son necesarias en un módulo de combinación estándar.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Tablas de base de datos de módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678251"
---
# <a name="merge-module-database-tables"></a>Tablas de base de datos de módulos de combinación

Las tablas siguientes son necesarias en un módulo de combinación estándar.



| Nombre de la tabla                                       | Comentario                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Componente](component-table.md)                 | DESEE                                                                                       |
| [Directorio](directory-table.md)                 | DESEE                                                                                       |
| [FeatureComponents](featurecomponents-table.md) | DESEE                                                                                       |
| [Archivo](file-table.md)                           | DESEE                                                                                       |
| [ModuleSignature](modulesignature-table.md)     | DESEE Combinados en la base de datos del instalador. Muestra la información que identifica un módulo de combinación. |
| [ModuleComponents](modulecomponents-table.md)   | DESEE Combinados en la base de datos del instalador. Enumera todos los componentes del módulo de combinación.     |



 

Las tablas siguientes solo se producen en módulos de combinación u otras bases de datos de instalador que ya se han combinado con un módulo de combinación.



| Nombre de la tabla                                     | Comentario                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ModuleDependency](moduledependency-table.md) | Combinados en la base de datos del instalador. Enumera otros módulos de combinación requeridos por este módulo de combinación.                |
| [ModuleExclusion](moduleexclusion-table.md)   | Combinados en la base de datos del instalador. Enumera otros módulos de combinación que no son compatibles con este módulo de combinación. |



 

Las siguientes tablas ModuleSequence solo se producen en los módulos de combinación.



| Nombre de la tabla                                                             | Comentario                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)               | Combina acciones en la [tabla AdminUISequence](adminuisequence-table.md).               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)     | Combina acciones en la [tabla AdminExecuteSequence](adminexecutesequence-table.md).     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                 | No use esta tabla. Para obtener más información, consulte [tabla AdvtUISequence](advtuisequence-table.md). |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)       | Combina acciones en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).       |
| [ModuleIgnoreTable](moduleignoretable-table.md)                       | Muestra las tablas del módulo que no se combinan en el archivo. msi.                        |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)           | Combina acciones en la [tabla InstallUISequence](installuisequence-table.md).           |
| [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | Combina acciones en la [tabla InstallExecuteSequence](installexecutesequence-table.md). |



 

Las tablas siguientes son necesarias en cada módulo de combinación configurable. Se requiere Mergemod.dll 2,0 o una versión posterior para crear un módulo de combinación configurable. Para obtener más información, consulte [módulos de combinación configurables](configurable-merge-modules.md).



| Nombre de la tabla                                                 | Comentario                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tabla ModuleSubstitution](modulesubstitution-table.md)   | DESEE Esta tabla no se combina en la base de datos de instalación de destino. Especifica los campos configurables en la base de datos de destino y proporciona una plantilla para la configuración de cada campo. |
| [Tabla ModuleConfiguration](moduleconfiguration-table.md) | DESEE Esta tabla no se combina en la base de datos de instalación de destino. Identifica los atributos configurables del módulo.                                                                 |



 

Las siguientes tablas de instalador no se pueden producir en un módulo de combinación estándar.

-   [BBControl](bbcontrol-table.md)
-   [Valla](billboard-table.md)
-   [CCPSearch](ccpsearch-table.md)
-   [Error](error-table.md)
-   [Característica](feature-table.md)
-   [Tabla LaunchCondition](launchcondition-table.md)
-   [Elementos multimedia](media-table.md)
-   [Revisión](patch-table.md)
-   [Actualización](upgrade-table.md)

Las siguientes tablas de instalador son opcionales en los módulos de combinación.

-   [ActionText](actiontext-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdvtUISequence](advtuisequence-table.md)
-   [AppId](appid-table.md)
-   [AppSearch](appsearch-table.md)
-   [BindImage](bindimage-table.md)
-   [CheckBox](checkbox-table.md)
-   [Clase](class-table.md)
-   [ComboBox](combobox-table.md)
-   [CompLocator](complocator-table.md)
-   [Control](control-table.md)
-   [ControlCondition](controlcondition-table.md)
-   [CreateFolder](createfolder-table.md)
-   [CustomAction](customaction-table.md)
-   [Diálogo](dialog-table.md)
-   [DrLocator](drlocator-table.md)
-   [DuplicateFile](duplicatefile-table.md)
-   [Entorno](environment-table.md)
-   [EventMapping](eventmapping-table.md)
-   [Extensión](extension-table.md)
-   [Fuente](font-table.md)
-   [Icono](icon-table.md)
-   [IniFile](inifile-table.md)
-   [IniLocator](inilocator-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [ListBox](listbox-table.md)
-   [ListView](listview-table.md)
-   [Mine](mime-table.md)
-   [MoveFile](movefile-table.md)
-   [ODBCAttribute](odbcattribute-table.md)
-   [ODBCDataSource](odbcdatasource-table.md)
-   [ODBCDriver](odbcdriver-table.md)
-   [ODBCSourceAttribute](odbcsourceattribute-table.md)
-   [ODBCTranslator](odbctranslator-table.md)
-   [Tabla ProgID](progid-table.md)
-   [Propiedad](property-table.md)
-   [PublishComponent](publishcomponent-table.md)
-   [RadioButton](radiobutton-table.md)
-   [Tabla del registro](registry-table.md)
-   [RegLocator](reglocator-table.md)
-   [RemoveFile](removefile-table.md)
-   [RemoveIniFile](removeinifile-table.md)
-   [RemoveRegistry](removeregistry-table.md)
-   [ReserveCost](reservecost-table.md)
-   [SelfReg](selfreg-table.md)
-   [ServiceControl](servicecontrol-table.md)
-   [ServiceInstall](serviceinstall-table.md)
-   [Acceso directo](shortcut-table.md)
-   [Signature](signature-table.md)
-   [Estilo]](textstyle-table.md)
-   [TypeLib](typelib-table.md)
-   [UIText](uitext-table.md)
-   [Verbo](verb-table.md)

 

 



