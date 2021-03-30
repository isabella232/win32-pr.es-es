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
# <a name="i-windows-installer"></a><span data-ttu-id="a1481-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="a1481-103">I (Windows Installer)</span></span>

<span data-ttu-id="a1481-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [o](o-gly.md) [p](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="a1481-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a1481-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**archivo. IDT**</span><span class="sxs-lookup"><span data-stu-id="a1481-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-106">Tabla de base de datos del instalador exportada.</span><span class="sxs-lookup"><span data-stu-id="a1481-106">Exported installer database table.</span></span> <span data-ttu-id="a1481-107">Para obtener más información, vea [importar y exportar](importing-and-exporting.md) y [Windows Installer extensiones de archivo](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1481-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Tabla de direcciones de importación (IAT)**</span><span class="sxs-lookup"><span data-stu-id="a1481-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-109">Donde se guarda la dirección virtual calculada de cada función importada de todos los archivos dll.</span><span class="sxs-lookup"><span data-stu-id="a1481-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="a1481-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interfaz de usuario interna**</span><span class="sxs-lookup"><span data-stu-id="a1481-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-111">Capacidades integradas del instalador que se pueden usar para crear una interfaz de usuario gráfica para la instalación.</span><span class="sxs-lookup"><span data-stu-id="a1481-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="a1481-112">Un autor puede elegir una [*interfaz de usuario externa*](e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="a1481-113">Para obtener más información, vea [acerca de la interfaz de usuario](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1481-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**nivel de instalación**</span><span class="sxs-lookup"><span data-stu-id="a1481-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-115">Valor de instalación especificado.</span><span class="sxs-lookup"><span data-stu-id="a1481-115">Specified installation value.</span></span> <span data-ttu-id="a1481-116">Una aplicación se instala solo si su propio nivel es menor o igual que el nivel de instalación.</span><span class="sxs-lookup"><span data-stu-id="a1481-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="a1481-117">Por lo tanto, el conjunto de aplicaciones elegidas para la instalación puede cambiarse modificando el nivel de instalación.</span><span class="sxs-lookup"><span data-stu-id="a1481-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="a1481-118">Para obtener más información, consulte [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1481-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**instalación a petición**</span><span class="sxs-lookup"><span data-stu-id="a1481-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-120">Servicio que instala las aplicaciones o características tal y como las solicita el usuario u otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1481-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="a1481-121">La [*publicidad*](a-gly.md) hace que una característica o aplicación esté disponible para la instalación a petición.</span><span class="sxs-lookup"><span data-stu-id="a1481-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="a1481-122">Para obtener más información, consulte: [instalación a petición](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1481-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexto de instalación**</span><span class="sxs-lookup"><span data-stu-id="a1481-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-124">La combinación de los tipos de instalación y los derechos de instalación genera tres contextos de instalación diferentes: administrado por usuario no administrado, administrado por usuario y administrado por equipo.</span><span class="sxs-lookup"><span data-stu-id="a1481-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="a1481-125">No hay ninguna tarea no administrada por máquina.</span><span class="sxs-lookup"><span data-stu-id="a1481-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="a1481-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**instalador**</span><span class="sxs-lookup"><span data-stu-id="a1481-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-127">[*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1481-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**base de datos del instalador**</span><span class="sxs-lookup"><span data-stu-id="a1481-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-129">Base de datos relacional que contiene instrucciones de instalación para una instalación de.</span><span class="sxs-lookup"><span data-stu-id="a1481-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="a1481-130">La base de datos del instalador se almacena en el [*archivo. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="a1481-131">Para obtener más información, consulte [base de datos del instalador](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1481-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**función de instalador**</span><span class="sxs-lookup"><span data-stu-id="a1481-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-133">Lo llama un usuario o una aplicación para obtener los servicios del instalador y la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="a1481-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="a1481-134">Esta es la interfaz de programación de aplicaciones del instalador.</span><span class="sxs-lookup"><span data-stu-id="a1481-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="a1481-135">Para obtener más información, vea referencia de la [función de instalador](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1481-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**herramienta de creación de paquetes del instalador**</span><span class="sxs-lookup"><span data-stu-id="a1481-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-137">Software que permite a un desarrollador crear y editar un [*archivo. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="a1481-138">Junto con los [*archivos de código fuente externos*](e-gly.md) se compone de un [*paquete*](p-gly.md) que contiene toda la información necesaria para una instalación de.</span><span class="sxs-lookup"><span data-stu-id="a1481-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="a1481-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**archivos de código fuente internos**</span><span class="sxs-lookup"><span data-stu-id="a1481-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="a1481-140">Almacenado en el [*archivo. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a1481-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="a1481-141">Varios archivos de código fuente internos se pueden comprimir y almacenar juntos en un [*archivo. cab*](c-gly.md) que se almacena en un archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="a1481-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 



