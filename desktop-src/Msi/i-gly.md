---
description: Obtenga información Windows Installer conceptos que comienzan por la letra I, como la tabla Importar dirección y el nivel de instalación.
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33b5cfb9c4545a5482b214e0413ab3e3d981109
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010658"
---
# <a name="i-windows-installer"></a><span data-ttu-id="e57cc-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="e57cc-103">I (Windows Installer)</span></span>

<span data-ttu-id="e57cc-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L M [N](m-gly.md) [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="e57cc-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e57cc-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**Archivo .idt**</span><span class="sxs-lookup"><span data-stu-id="e57cc-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-106">Tabla de base de datos del instalador exportada.</span><span class="sxs-lookup"><span data-stu-id="e57cc-106">Exported installer database table.</span></span> <span data-ttu-id="e57cc-107">Para obtener más información, [vea Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Importar tabla de direcciones (IAT)**</span><span class="sxs-lookup"><span data-stu-id="e57cc-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-109">Donde se guarda la dirección virtual calculada de cada función importada de todos los archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="e57cc-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interfaz de usuario interna**</span><span class="sxs-lookup"><span data-stu-id="e57cc-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-111">Funcionalidades integradas del instalador que se pueden usar para crear una interfaz de usuario gráfica para la instalación.</span><span class="sxs-lookup"><span data-stu-id="e57cc-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="e57cc-112">Un autor puede elegir una [*interfaz de usuario externa.*](e-gly.md)</span><span class="sxs-lookup"><span data-stu-id="e57cc-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="e57cc-113">Para obtener más información, [vea Acerca de la Interfaz de usuario](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**nivel de instalación**</span><span class="sxs-lookup"><span data-stu-id="e57cc-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-115">Valor de instalación especificado.</span><span class="sxs-lookup"><span data-stu-id="e57cc-115">Specified installation value.</span></span> <span data-ttu-id="e57cc-116">Una aplicación solo se instala si su propio nivel es menor o igual que el nivel de instalación.</span><span class="sxs-lookup"><span data-stu-id="e57cc-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="e57cc-117">Por lo tanto, el conjunto de aplicaciones elegidas para la instalación se puede cambiar modificando el nivel de instalación.</span><span class="sxs-lookup"><span data-stu-id="e57cc-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="e57cc-118">Para obtener más información, vea [Tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**instalación a petición**</span><span class="sxs-lookup"><span data-stu-id="e57cc-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-120">Servicio que instala aplicaciones o características según lo solicitado por el usuario u otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="e57cc-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="e57cc-121">[*La*](a-gly.md) publicidad hace que una característica o aplicación esté disponible para la instalación a petición.</span><span class="sxs-lookup"><span data-stu-id="e57cc-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="e57cc-122">Para obtener más información, vea: [Instalación a petición.](installation-on-demand.md)</span><span class="sxs-lookup"><span data-stu-id="e57cc-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexto de instalación**</span><span class="sxs-lookup"><span data-stu-id="e57cc-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-124">La combinación de derechos de instalación y tipos de instalación genera tres contextos de instalación diferentes: por usuario no administrado, administrado por usuario y administrado por máquina.</span><span class="sxs-lookup"><span data-stu-id="e57cc-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="e57cc-125">No hay nada como por máquina no administrada.</span><span class="sxs-lookup"><span data-stu-id="e57cc-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**Instalador**</span><span class="sxs-lookup"><span data-stu-id="e57cc-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-127">El [*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**base de datos del instalador**</span><span class="sxs-lookup"><span data-stu-id="e57cc-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-129">Base de datos relacional que contiene instrucciones de configuración para una instalación.</span><span class="sxs-lookup"><span data-stu-id="e57cc-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="e57cc-130">La base de datos del instalador se almacena en [*.msi archivo*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="e57cc-131">Para obtener más información, vea [Installer Database](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**función del instalador**</span><span class="sxs-lookup"><span data-stu-id="e57cc-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-133">Lo llama un usuario o una aplicación para obtener la funcionalidad y los servicios del instalador.</span><span class="sxs-lookup"><span data-stu-id="e57cc-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="e57cc-134">Esta es la interfaz de programación de aplicaciones del instalador.</span><span class="sxs-lookup"><span data-stu-id="e57cc-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="e57cc-135">Para obtener información, vea [Installer Function Reference](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**herramienta de creación de paquetes del instalador**</span><span class="sxs-lookup"><span data-stu-id="e57cc-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-137">Software que permite a un desarrollador crear y editar un [*.msi archivo*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="e57cc-138">Esto junto con los [*archivos de origen externos*](e-gly.md) componen [*un paquete*](p-gly.md) que contiene toda la información necesaria para una instalación.</span><span class="sxs-lookup"><span data-stu-id="e57cc-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="e57cc-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**archivos de origen internos**</span><span class="sxs-lookup"><span data-stu-id="e57cc-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="e57cc-140">Almacenado en el [*.msi archivo*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e57cc-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="e57cc-141">Varios archivos de origen internos se pueden comprimir y almacenar juntos en un archivo [*de*](c-gly.md) archivador que se almacena dentro de un .msi archivo.</span><span class="sxs-lookup"><span data-stu-id="e57cc-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 



