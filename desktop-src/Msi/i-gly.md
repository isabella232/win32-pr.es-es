---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca95a473f648ca9e1a08773d93f47bd198df11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910925"
---
# <a name="i-windows-installer"></a>I (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [o](o-gly.md) [p](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**archivo. IDT**
</dt> <dd>

Tabla de base de datos del instalador exportada. Para obtener más información, vea [importar y exportar](importing-and-exporting.md) y [Windows Installer extensiones de archivo](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Tabla de direcciones de importación (IAT)**
</dt> <dd>

Donde se guarda la dirección virtual calculada de cada función importada de todos los archivos dll.

</dd> <dt>

<span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interfaz de usuario interna**
</dt> <dd>

Capacidades integradas del instalador que se pueden usar para crear una interfaz de usuario gráfica para la instalación. Un autor puede elegir una [*interfaz de usuario externa*](e-gly.md). Para obtener más información, vea [acerca de la interfaz de usuario](about-the-user-interface.md).

</dd> <dt>

<span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**nivel de instalación**
</dt> <dd>

Valor de instalación especificado. Una aplicación se instala solo si su propio nivel es menor o igual que el nivel de instalación. Por lo tanto, el conjunto de aplicaciones elegidas para la instalación puede cambiarse modificando el nivel de instalación. Para obtener más información, consulte [tabla de características](feature-table.md).

</dd> <dt>

<span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**instalación a petición**
</dt> <dd>

Servicio que instala las aplicaciones o características tal y como las solicita el usuario u otra aplicación. La [*publicidad*](a-gly.md) hace que una característica o aplicación esté disponible para la instalación a petición. Para obtener más información, consulte: [instalación a petición](installation-on-demand.md).

</dd> <dt>

<span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexto de instalación**
</dt> <dd>

La combinación de los tipos de instalación y los derechos de instalación genera tres contextos de instalación diferentes: administrado por usuario no administrado, administrado por usuario y administrado por equipo. No hay ninguna tarea no administrada por máquina.

</dd> <dt>

<span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**instalador**
</dt> <dd>

[*Windows Installer*](m-gly.md).

</dd> <dt>

<span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**base de datos del instalador**
</dt> <dd>

Base de datos relacional que contiene instrucciones de instalación para una instalación de. La base de datos del instalador se almacena en el [*archivo. msi*](m-gly.md). Para obtener más información, consulte [base de datos del instalador](installer-database.md).

</dd> <dt>

<span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**función de instalador**
</dt> <dd>

Lo llama un usuario o una aplicación para obtener los servicios del instalador y la funcionalidad. Esta es la interfaz de programación de aplicaciones del instalador. Para obtener más información, vea referencia de la [función de instalador](installer-function-reference.md).

</dd> <dt>

<span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**herramienta de creación de paquetes del instalador**
</dt> <dd>

Software que permite a un desarrollador crear y editar un [*archivo. msi*](m-gly.md). Junto con los [*archivos de código fuente externos*](e-gly.md) se compone de un [*paquete*](p-gly.md) que contiene toda la información necesaria para una instalación de.

</dd> <dt>

<span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**archivos de código fuente internos**
</dt> <dd>

Almacenado en el [*archivo. msi*](m-gly.md). Varios archivos de código fuente internos se pueden comprimir y almacenar juntos en un [*archivo. cab*](c-gly.md) que se almacena en un archivo. msi.

</dd> </dl>

 

 



