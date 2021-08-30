---
description: Obtenga información Windows conceptos del instalador que comienzan por la letra I, como la tabla Importar dirección y el nivel de instalación.
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8894b61907062c7b68cdb0a70e9b20e49729b8a3a04c76b9a59d82efbefdbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129455"
---
# <a name="i-windows-installer"></a>I (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L M [N](m-gly.md) [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**Archivo .idt**
</dt> <dd>

Tabla de base de datos del instalador exportada. Para obtener más información, vea [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Importar tabla de direcciones (IAT)**
</dt> <dd>

Donde se guarda la dirección virtual calculada de cada función importada desde todos los archivos DLL.

</dd> <dt>

<span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interfaz de usuario interna**
</dt> <dd>

Funcionalidades integradas del instalador que se pueden usar para crear una interfaz de usuario gráfica para la instalación. Un autor puede elegir una [*interfaz de usuario externa.*](e-gly.md) Para obtener más información, [vea Acerca de la Interfaz de usuario](about-the-user-interface.md).

</dd> <dt>

<span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**nivel de instalación**
</dt> <dd>

Valor de instalación especificado. Una aplicación solo se instala si su propio nivel es menor o igual que el nivel de instalación. Por lo tanto, el conjunto de aplicaciones elegido para la instalación se puede cambiar modificando el nivel de instalación. Para obtener más información, vea [Tabla de características](feature-table.md).

</dd> <dt>

<span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**instalación a petición**
</dt> <dd>

Servicio que instala aplicaciones o características según lo solicitado por el usuario u otra aplicación. [*La*](a-gly.md) publicidad hace que una característica o aplicación esté disponible para la instalación a petición. Para obtener más información, vea: [Instalación a petición.](installation-on-demand.md)

</dd> <dt>

<span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexto de instalación**
</dt> <dd>

La combinación de derechos de instalación y tipos de instalación genera tres contextos de instalación diferentes: por usuario no administrado, administrado por usuario y administrado por máquina. No hay nada como por máquina no administrada.

</dd> <dt>

<span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**Instalador**
</dt> <dd>

El [*Windows de instalación*](m-gly.md)de .

</dd> <dt>

<span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**base de datos del instalador**
</dt> <dd>

Base de datos relacional que contiene instrucciones de configuración para una instalación. La base de datos del instalador se almacena en [*.msi archivo*](m-gly.md). Para obtener más información, vea [Installer Database](installer-database.md).

</dd> <dt>

<span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**función del instalador**
</dt> <dd>

Lo llama un usuario o una aplicación para obtener la funcionalidad y los servicios del instalador. Esta es la interfaz de programación de aplicaciones del instalador. Para obtener información, vea [Installer Function Reference](installer-function-reference.md).

</dd> <dt>

<span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**herramienta de creación de paquetes del instalador**
</dt> <dd>

Software que permite a un desarrollador crear y editar un [*.msi archivo*](m-gly.md). Esto junto con los [*archivos de origen externos*](e-gly.md) componen [*un paquete*](p-gly.md) que contiene toda la información necesaria para una instalación.

</dd> <dt>

<span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**archivos de origen internos**
</dt> <dd>

Almacenado en el [*.msi archivo*](m-gly.md). Varios archivos de origen internos se pueden comprimir y almacenar juntos en un archivo [*de*](c-gly.md) archivador que se almacena dentro de un .msi archivo.

</dd> </dl>

 

 



