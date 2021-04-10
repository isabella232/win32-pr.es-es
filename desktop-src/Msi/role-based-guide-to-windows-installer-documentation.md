---
description: Windows Installer es la solución recomendada para la instalación y la configuración de aplicaciones en Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guía basada en roles para Windows Installer documentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082334"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a><span data-ttu-id="2b0d7-103">Guía basada en roles para Windows Installer documentación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-103">Role-based Guide to Windows Installer Documentation</span></span>

<span data-ttu-id="2b0d7-104">Windows Installer es la solución recomendada para la instalación y la configuración de aplicaciones en Windows.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-104">Windows Installer is the recommended solution for the installation and setup of applications on Windows.</span></span> <span data-ttu-id="2b0d7-105">Por lo tanto, parte de la información contenida en este SDK será de interés para una amplia gama de profesionales de ti y desarrollo de software.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-105">Therefore, some of the information contained in this SDK will be of interest to a wide range of software development and IT professionals.</span></span> <span data-ttu-id="2b0d7-106">Esta sección se proporciona como guía a los lectores que prefieren ver vínculos a temas organizados por rol profesional y escenarios de tareas comunes.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-106">This section is provided as a guide to readers who prefer to see links to topics organized by professional role and common task scenarios.</span></span> <span data-ttu-id="2b0d7-107">Dado que los roles pueden diferir en gran medida entre las organizaciones, la siguiente agrupación solo se debe considerar como guía de una ubicación para empezar a buscar la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-107">Because roles can differ greatly between organizations, the following grouping should only be considered as a guide to a location to start searching for the information you need.</span></span>

-   [<span data-ttu-id="2b0d7-108">Desarrolladores de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-108">Application Developers</span></span>](#application-developers)
-   [<span data-ttu-id="2b0d7-109">Configuración de autores</span><span class="sxs-lookup"><span data-stu-id="2b0d7-109">Setup Authors</span></span>](#setup-authors)
-   [<span data-ttu-id="2b0d7-110">Profesionales de TI</span><span class="sxs-lookup"><span data-stu-id="2b0d7-110">IT Professionals</span></span>](#it-professionals)
-   [<span data-ttu-id="2b0d7-111">Desarrolladores de infraestructura</span><span class="sxs-lookup"><span data-stu-id="2b0d7-111">Infrastructure Developers</span></span>](#infrastructure-developers)

<span data-ttu-id="2b0d7-112">Esta documentación está destinada a desarrolladores de software que desean crear aplicaciones que utilicen Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-112">This documentation is intended for software developers who want to make applications that use Windows Installer.</span></span> <span data-ttu-id="2b0d7-113">Como origen principal del material de referencia para el instalador, el SDK proporciona información acerca de los paquetes de instalación y el servicio del instalador.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-113">As the primary source of reference material for the installer, the SDK provides information about installation packages and the installer service.</span></span> <span data-ttu-id="2b0d7-114">Contiene descripciones completas de la interfaz de programación de aplicaciones (API) y los elementos de la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-114">It contains complete descriptions of the application programming interface (API) and the elements of the installer database.</span></span>

<span data-ttu-id="2b0d7-115">Para obtener más información, vea [otros orígenes de información de Windows Installer](other-sources-of-windows-installer-information.md).</span><span class="sxs-lookup"><span data-stu-id="2b0d7-115">For more information, see [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).</span></span>

## <a name="application-developers"></a><span data-ttu-id="2b0d7-116">Desarrolladores de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-116">Application Developers</span></span>

<span data-ttu-id="2b0d7-117">Los desarrolladores de aplicaciones crean aplicaciones que llaman a la interfaz de programación de aplicaciones Windows Installer e instalan paquetes de Windows Installer en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-117">Application developers create applications that call the Windows Installer application programming interface and install Windows installer packages at run time.</span></span> <span data-ttu-id="2b0d7-118">El Windows Installer puede trabajar en una aplicación como la reparación automática y la instalación a petición.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-118">The Windows Installer can do work in an application such as self-repair and installation-on-demand.</span></span> <span data-ttu-id="2b0d7-119">Normalmente, los desarrolladores de aplicaciones hacen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-119">Typically, application Developers do the following:</span></span>

-   <span data-ttu-id="2b0d7-120">Habilitar la instalación a petición de aplicaciones en tiempo de ejecución desde otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-120">Enable installation-on-demand of applications at run time from within another application.</span></span>

    <span data-ttu-id="2b0d7-121">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-121">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-122">Usar las funciones del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-122">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="2b0d7-123">Referencia de funciones del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-123">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-124">Instalación a petición</span><span class="sxs-lookup"><span data-stu-id="2b0d7-124">Installation-On-Demand</span></span>](installation-on-demand.md)
    -   [<span data-ttu-id="2b0d7-125">Administración de componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-125">Component Management</span></span>](component-management.md)
    -   [<span data-ttu-id="2b0d7-126">Editar accesos directos del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-126">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="2b0d7-127">**Propiedad OLEAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-127">**OLEAdvtSupport Property**</span></span>](oleadvtsupport.md)
    -   [<span data-ttu-id="2b0d7-128">Compatibilidad de la plataforma con el anuncio</span><span class="sxs-lookup"><span data-stu-id="2b0d7-128">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)

-   <span data-ttu-id="2b0d7-129">Habilite la reparación automática de las aplicaciones reinstalando los componentes según sea necesario en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-129">Enable self-repair of applications by reinstalling components as needed at run time.</span></span>

    <span data-ttu-id="2b0d7-130">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-130">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-131">Usar las funciones del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-131">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="2b0d7-132">Referencia de funciones del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-132">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-133">Resistencia</span><span class="sxs-lookup"><span data-stu-id="2b0d7-133">Resiliency</span></span>](resiliency.md)
    -   [<span data-ttu-id="2b0d7-134">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="2b0d7-134">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="2b0d7-135">Buscar una característica o componente interrumpido</span><span class="sxs-lookup"><span data-stu-id="2b0d7-135">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="2b0d7-136">Reemplazar archivos existentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-136">Replacing Existing Files</span></span>](replacing-existing-files.md)

-   <span data-ttu-id="2b0d7-137">Mostrar una interfaz de usuario para recopilar las preferencias de configuración e información de usuario la primera vez que se instala o se ejecuta una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-137">Display a user interface to collect user information and configuration preferences the first time an application is installed or run.</span></span> <span data-ttu-id="2b0d7-138">El autor del programa de instalación del paquete de Windows Installer debe agregar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-138">The user interface must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="2b0d7-139">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-139">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-140">Usar las funciones del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-140">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="2b0d7-141">Inicializar una aplicación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-141">Initializing an Application</span></span>](initializing-an-application.md)
    -   [<span data-ttu-id="2b0d7-142">Cuadro de diálogo FirstRun</span><span class="sxs-lookup"><span data-stu-id="2b0d7-142">FirstRun Dialog</span></span>](firstrun-dialog.md)
    -   [<span data-ttu-id="2b0d7-143">Acerca de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2b0d7-143">About the User Interface</span></span>](about-the-user-interface.md)

-   <span data-ttu-id="2b0d7-144">Cree aplicaciones que usen un modelo de direccionamiento indirecto para hacer referencia a componentes con funcionalidad paralela.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-144">Create applications that use an indirection model to refer to components with parallel functionality.</span></span> <span data-ttu-id="2b0d7-145">El autor del programa de instalación del paquete de Windows Installer debe agregar las categorías de componentes cualificadas.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-145">The qualified component categories must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="2b0d7-146">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-146">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-147">Componentes completos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-147">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="2b0d7-148">Uso de componentes calificados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-148">Using Qualified Components</span></span>](using-qualified-components.md)

-   <span data-ttu-id="2b0d7-149">Use ensamblados privados y en paralelo para aislar las aplicaciones y reducir los conflictos de DLL.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-149">Use private and side-by-side assemblies to isolate applications and reduce DLL conflicts.</span></span>

    <span data-ttu-id="2b0d7-150">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-150">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-151">Ensamblados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-151">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="2b0d7-152">Claves del registro de ensamblado escritas por Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-152">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="2b0d7-153">Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b0d7-153">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [<span data-ttu-id="2b0d7-154">Instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b0d7-154">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [<span data-ttu-id="2b0d7-155">Tabla MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="2b0d7-155">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="2b0d7-156">Tabla MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="2b0d7-156">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="2b0d7-157">**MsiProvideAssembly**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-157">**MsiProvideAssembly**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [<span data-ttu-id="2b0d7-158">**Propiedad MsiWin32AssemblySupport**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-158">**MsiWin32AssemblySupport Property**</span></span>](msiwin32assemblysupport.md)
    -   [<span data-ttu-id="2b0d7-159">**Propiedad MsiNetAssemblySupport**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-159">**MsiNetAssemblySupport Property**</span></span>](msinetassemblysupport.md)
    -   [<span data-ttu-id="2b0d7-160">**Componentes aislados**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-160">**Isolated Components**</span></span>](isolated-components.md)

-   <span data-ttu-id="2b0d7-161">Prepare la aplicación para instalar sus propias actualizaciones principales completas.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-161">Prepare the application to install its own comprehensive major upgrades.</span></span>

    <span data-ttu-id="2b0d7-162">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-162">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-163">Revisiones y actualizaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-163">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="2b0d7-164">Actualizaciones principales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-164">Major Upgrades</span></span>](major-upgrades.md)
    -   [<span data-ttu-id="2b0d7-165">**Propiedad UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-165">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="2b0d7-166">**Usar UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-166">**Using an UpgradeCode**</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="2b0d7-167">Impedir que un paquete antiguo se instale en una versión más reciente</span><span class="sxs-lookup"><span data-stu-id="2b0d7-167">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   <span data-ttu-id="2b0d7-168">Prepare la aplicación para instalar sus propias actualizaciones secundarias, pequeñas actualizaciones o correcciones.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-168">Prepare the application to install its own minor upgrades, small updates, or fixes.</span></span>

    <span data-ttu-id="2b0d7-169">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-169">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-170">Revisiones y actualizaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-170">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="2b0d7-171">Actualizaciones pequeñas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-171">Small Updates</span></span>](small-updates.md)
    -   [<span data-ttu-id="2b0d7-172">Actualizaciones secundarias</span><span class="sxs-lookup"><span data-stu-id="2b0d7-172">Minor Upgrades</span></span>](minor-upgrades.md)

-   <span data-ttu-id="2b0d7-173">Organice los recursos de la aplicación en componentes que pueden trabajar con el Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-173">Organize application resources into components that can work with the Windows Installer.</span></span>

    <span data-ttu-id="2b0d7-174">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-174">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-175">Componentes de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-175">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="2b0d7-176">Trabajar con características y componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-176">Working with Features and Components</span></span>](working-with-features-and-components.md)
    -   [<span data-ttu-id="2b0d7-177">Uso de componentes transitivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-177">Using Transitive Components</span></span>](using-transitive-components.md)
    -   [<span data-ttu-id="2b0d7-178">¿Qué ocurre si se interrumpen las reglas de componentes?</span><span class="sxs-lookup"><span data-stu-id="2b0d7-178">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="2b0d7-179">Organizar aplicaciones en componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-179">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="2b0d7-180">Componentes aislados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-180">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="2b0d7-181">Componentes completos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-181">Qualified Components</span></span>](qualified-components.md)

## <a name="setup-authors"></a><span data-ttu-id="2b0d7-182">Configuración de autores</span><span class="sxs-lookup"><span data-stu-id="2b0d7-182">Setup Authors</span></span>

<span data-ttu-id="2b0d7-183">Los autores del programa de instalación crean Windows Installer paquetes (archivos. msi) que contienen la lógica de instalación y la información necesaria para instalar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-183">Setup Authors create Windows Installer packages (.msi files) that contain the setup logic and information needed to install an application.</span></span> <span data-ttu-id="2b0d7-184">Normalmente usan herramientas de creación como [Orca.exe](orca-exe.md) para rellenar la base de datos Windows Installer con la lógica e información del programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-184">They typically use authoring tools such as [Orca.exe](orca-exe.md) to populate the Windows Installer database with the setup logic and information.</span></span> <span data-ttu-id="2b0d7-185">Normalmente, los autores de la instalación hacen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-185">Typically, Setup Authors do the following:</span></span>

-   <span data-ttu-id="2b0d7-186">Determine la funcionalidad disponible con diferentes versiones de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-186">Determine the functionality available with different Windows Installer versions.</span></span>

    <span data-ttu-id="2b0d7-187">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-187">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-188">Determinar la versión de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-188">Determining the Windows Installer Version</span></span>](determining-the-windows-installer-version.md)
    -   [<span data-ttu-id="2b0d7-189">Versiones de lanzamiento de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-189">Released Versions of Windows Installer</span></span>](released-versions-of-windows-installer.md)
    -   [<span data-ttu-id="2b0d7-190">Novedades de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-190">What's New in Windows Installer</span></span>](what-s-new-in-windows-installer.md)

-   <span data-ttu-id="2b0d7-191">Organice los recursos de la aplicación en componentes de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-191">Organize application resources into Windows Installer components.</span></span>

    <span data-ttu-id="2b0d7-192">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-192">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-193">Componentes de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-193">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="2b0d7-194">Organizar aplicaciones en componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-194">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="2b0d7-195">Cambiar el código del componente</span><span class="sxs-lookup"><span data-stu-id="2b0d7-195">Changing the Component Code</span></span>](changing-the-component-code.md)
    -   [<span data-ttu-id="2b0d7-196">¿Qué ocurre si se interrumpen las reglas de componentes?</span><span class="sxs-lookup"><span data-stu-id="2b0d7-196">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="2b0d7-197">Ejemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-197">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2b0d7-198">Use herramientas de creación de paquetes de Windows Installer de terceros o herramientas de SDK como [Orca.exe](orca-exe.md) para rellenar una base de datos de instalación y crear un paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-198">Use third-party Windows Installer package authoring tools or SDK tools such as [Orca.exe](orca-exe.md) to populate an installation database and create a Windows Installer package.</span></span>

    <span data-ttu-id="2b0d7-199">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-199">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-200">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-200">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="2b0d7-201">Paquete de instalación, acerca de la base de datos del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-201">Installation Package, About the Installer Database</span></span>](installation-package.md)
    -   [<span data-ttu-id="2b0d7-202">Extensiones de archivo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-202">Windows Installer File Extensions</span></span>](windows-installer-file-extensions.md)
    -   [<span data-ttu-id="2b0d7-203">Tablas de base de datos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-203">Database Tables</span></span>](database-tables.md)
    -   [<span data-ttu-id="2b0d7-204">Códigos de paquete</span><span class="sxs-lookup"><span data-stu-id="2b0d7-204">Package Codes</span></span>](package-codes.md)
    -   [<span data-ttu-id="2b0d7-205">Crear un paquete grande</span><span class="sxs-lookup"><span data-stu-id="2b0d7-205">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="2b0d7-206">Windows Installer en sistemas operativos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2b0d7-206">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="2b0d7-207">Asignar nombres a tablas, propiedades y acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-207">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
    -   [<span data-ttu-id="2b0d7-208">Limitaciones de OLE en secuencias</span><span class="sxs-lookup"><span data-stu-id="2b0d7-208">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
    -   [<span data-ttu-id="2b0d7-209">Formato de definición de columna</span><span class="sxs-lookup"><span data-stu-id="2b0d7-209">Column Definition Format</span></span>](column-definition-format.md)
    -   [<span data-ttu-id="2b0d7-210">Reducir el tamaño de un archivo. msi</span><span class="sxs-lookup"><span data-stu-id="2b0d7-210">Reducing the Size of an .msi File</span></span>](reducing-the-size-of-an--msi-file.md)

-   <span data-ttu-id="2b0d7-211">Cree la base de datos Windows Installer para instalar archivos.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-211">Author the Windows Installer database to install files.</span></span>

    <span data-ttu-id="2b0d7-212">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-212">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-213">Grupo de tablas principales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-213">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="2b0d7-214">Grupo de tablas de archivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-214">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="2b0d7-215">Tabla de archivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-215">File Table</span></span>](file-table.md)
    -   [<span data-ttu-id="2b0d7-216">Búsqueda de archivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-216">File Searching</span></span>](file-searching.md)
    -   [<span data-ttu-id="2b0d7-217">Costo de archivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-217">File Costing</span></span>](file-costing.md)
    -   [<span data-ttu-id="2b0d7-218">Instalación de archivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-218">File Installation</span></span>](file-installation.md)
    -   [<span data-ttu-id="2b0d7-219">Archivos complementarios</span><span class="sxs-lookup"><span data-stu-id="2b0d7-219">Companion Files</span></span>](companion-files.md)
    -   [<span data-ttu-id="2b0d7-220">Reglas de control de versiones de archivo</span><span class="sxs-lookup"><span data-stu-id="2b0d7-220">File Versioning Rules</span></span>](file-versioning-rules.md)
    -   [<span data-ttu-id="2b0d7-221">Control de versiones de archivo predeterminado</span><span class="sxs-lookup"><span data-stu-id="2b0d7-221">Default File Versioning</span></span>](default-file-versioning.md)
    -   [<span data-ttu-id="2b0d7-222">Reemplazar archivos existentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-222">Replacing Existing Files</span></span>](replacing-existing-files.md)
    -   [<span data-ttu-id="2b0d7-223">Uso de archivadores y orígenes comprimidos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-223">Using Cabinets and Compressed Sources</span></span>](using-cabinets-and-compressed-sources.md)
    -   [<span data-ttu-id="2b0d7-224">Quitar archivos en desuso</span><span class="sxs-lookup"><span data-stu-id="2b0d7-224">Removing Stranded Files</span></span>](removing-stranded-files.md)
    -   [<span data-ttu-id="2b0d7-225">Instalación de componentes permanentes, archivos, fuentes y claves del registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-225">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="2b0d7-226">Tabla FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="2b0d7-226">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
    -   [<span data-ttu-id="2b0d7-227">Buscar un archivo y crear una propiedad que contiene la ruta de acceso del archivo</span><span class="sxs-lookup"><span data-stu-id="2b0d7-227">Searching for a File and Creating a Property Holding the File's Path</span></span>](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [<span data-ttu-id="2b0d7-228">Buscar un directorio y un archivo en el directorio</span><span class="sxs-lookup"><span data-stu-id="2b0d7-228">Searching for a Directory and a File in the Directory</span></span>](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [<span data-ttu-id="2b0d7-229">Ejemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-229">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2b0d7-230">Cree una base de datos Windows Installer que instale una estructura de directorios y carpetas.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-230">Author a Windows Installer database that installs a directory structure and folders.</span></span>

    <span data-ttu-id="2b0d7-231">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-231">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-232">Grupo de tablas principales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-232">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="2b0d7-233">Grupo de tablas de archivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-233">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="2b0d7-234">Tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-234">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="2b0d7-235">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="2b0d7-235">Directory Table</span></span>](directory-table.md)
    -   [<span data-ttu-id="2b0d7-236">Usar la tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="2b0d7-236">Using the Directory Table</span></span>](using-the-directory-table.md)
    -   [<span data-ttu-id="2b0d7-237">Usar una propiedad de directorio en una ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="2b0d7-237">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)
    -   [<span data-ttu-id="2b0d7-238">Propiedades de la carpeta del sistema</span><span class="sxs-lookup"><span data-stu-id="2b0d7-238">System Folder Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="2b0d7-239">CreateFolder (tabla)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-239">CreateFolder Table</span></span>](createfolder-table.md)
    -   [<span data-ttu-id="2b0d7-240">Tabla LockPermissions</span><span class="sxs-lookup"><span data-stu-id="2b0d7-240">LockPermissions Table</span></span>](lockpermissions-table.md)
    -   [<span data-ttu-id="2b0d7-241">Tabla MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="2b0d7-241">MsiLockPermissionsEx Table</span></span>](msilockpermissionsex-table.md)
    -   [<span data-ttu-id="2b0d7-242">Cambiar la ubicación de destino de un directorio</span><span class="sxs-lookup"><span data-stu-id="2b0d7-242">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="2b0d7-243">Ejemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-243">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2b0d7-244">Cree una base de datos Windows Installer que instale las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-244">Author a Windows Installer database that installs registry keys.</span></span>

    <span data-ttu-id="2b0d7-245">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-245">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-246">Grupo de tablas principales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-246">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="2b0d7-247">Grupo de tablas del registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-247">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="2b0d7-248">Tabla del registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-248">Registry Table</span></span>](registry-table.md)
    -   [<span data-ttu-id="2b0d7-249">Modificar el registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-249">Modifying the Registry</span></span>](modifying-the-registry.md)
    -   [<span data-ttu-id="2b0d7-250">Agregar o quitar claves del registro en la instalación o desinstalación de componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-250">Adding or Removing Registry Keys on the Installation or Removal of Components</span></span>](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [<span data-ttu-id="2b0d7-251">Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-251">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="2b0d7-252">Instalación de componentes permanentes, archivos, fuentes y claves del registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-252">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="2b0d7-253">Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-253">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [<span data-ttu-id="2b0d7-254">Buscar una entrada del registro y crear una propiedad que contiene el valor del registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-254">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [<span data-ttu-id="2b0d7-255">Claves del registro de ensamblado escritas por el Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-255">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="2b0d7-256">Desinstalar la clave del registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-256">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
    -   [<span data-ttu-id="2b0d7-257">Tabla SelfReg</span><span class="sxs-lookup"><span data-stu-id="2b0d7-257">SelfReg Table</span></span>](selfreg-table.md)
    -   [<span data-ttu-id="2b0d7-258">Especificar el orden de registro automático</span><span class="sxs-lookup"><span data-stu-id="2b0d7-258">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
    -   [<span data-ttu-id="2b0d7-259">Ejemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-259">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2b0d7-260">Cree una base de datos Windows Installer que instale los servicios de.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-260">Author a Windows Installer database that installs services.</span></span>

    <span data-ttu-id="2b0d7-261">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-261">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-262">Tabla ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="2b0d7-262">ServiceInstall Table</span></span>](serviceinstall-table.md)
    -   [<span data-ttu-id="2b0d7-263">Tabla ServiceControl</span><span class="sxs-lookup"><span data-stu-id="2b0d7-263">ServiceControl Table</span></span>](servicecontrol-table.md)
    -   [<span data-ttu-id="2b0d7-264">Tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-264">Component Table</span></span>](component-table.md)

-   <span data-ttu-id="2b0d7-265">Cree una base de datos Windows Installer que instale componentes aislados o componentes COM.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-265">Author a Windows Installer database that installs isolated components or COM components.</span></span>

    <span data-ttu-id="2b0d7-266">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-266">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-267">Grupo de tablas del registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-267">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="2b0d7-268">Tabla de clases</span><span class="sxs-lookup"><span data-stu-id="2b0d7-268">Class Table</span></span>](class-table.md)
    -   [<span data-ttu-id="2b0d7-269">Tabla de ComPlus</span><span class="sxs-lookup"><span data-stu-id="2b0d7-269">Complus Table</span></span>](complus-table.md)
    -   [<span data-ttu-id="2b0d7-270">Componentes aislados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-270">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="2b0d7-271">Usar componentes aislados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-271">Using Isolated Components</span></span>](using-isolated-components.md)
    -   [<span data-ttu-id="2b0d7-272">Instalación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-272">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
    -   [<span data-ttu-id="2b0d7-273">Reinstalación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-273">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
    -   [<span data-ttu-id="2b0d7-274">Eliminación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-274">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
    -   [<span data-ttu-id="2b0d7-275">Instalar un componente COM en una ubicación privada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-275">Installing a COM Component to a Private Location</span></span>](installing-a-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="2b0d7-276">Convertir un componente COM en un paquete existente privado</span><span class="sxs-lookup"><span data-stu-id="2b0d7-276">Make a COM Component in an Existing Package Private</span></span>](make-a-com-component-in-an-existing-package-private.md)
    -   [<span data-ttu-id="2b0d7-277">Instalación de una aplicación COM+ con el Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-277">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
    -   [<span data-ttu-id="2b0d7-278">Instalar un componente que no es COM en una ubicación privada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-278">Installing a non-COM Component to a Private Location</span></span>](installing-a-non-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="2b0d7-279">Convertir un componente que no sea COM en un paquete existente privado</span><span class="sxs-lookup"><span data-stu-id="2b0d7-279">Make a non-COM Component in an Existing Package Private</span></span>](make-a-non-com-component-in-an-existing-package-private.md)

-   <span data-ttu-id="2b0d7-280">Cree una base de datos Windows Installer que instale los ensamblados.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-280">Author a Windows Installer database that installs assemblies.</span></span>

    <span data-ttu-id="2b0d7-281">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-281">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-282">Tabla MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="2b0d7-282">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="2b0d7-283">Tabla MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="2b0d7-283">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="2b0d7-284">Ensamblados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-284">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="2b0d7-285">Claves del registro de ensamblado escritas por el Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-285">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="2b0d7-286">Instalación de ensamblados Win32</span><span class="sxs-lookup"><span data-stu-id="2b0d7-286">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)

-   <span data-ttu-id="2b0d7-287">Cree una base de datos Windows Installer que instale controladores y traductores ODBC.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-287">Author a Windows Installer database that installs ODBC drivers and translators.</span></span>

    <span data-ttu-id="2b0d7-288">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-288">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-289">Tabla ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="2b0d7-289">ODBCAttribute Table</span></span>](odbcattribute-table.md)
    -   [<span data-ttu-id="2b0d7-290">Tabla ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="2b0d7-290">ODBCDriver Table</span></span>](odbcdriver-table.md)
    -   [<span data-ttu-id="2b0d7-291">Tabla ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="2b0d7-291">ODBCTranslator Table</span></span>](odbctranslator-table.md)
    -   [<span data-ttu-id="2b0d7-292">Tabla ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="2b0d7-292">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
    -   [<span data-ttu-id="2b0d7-293">Tabla ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="2b0d7-293">ODBCSourceAttribute Table</span></span>](odbcsourceattribute-table.md)

-   <span data-ttu-id="2b0d7-294">Cree una base de datos Windows Installer que instale MIME.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-294">Author a Windows Installer database that installs MIME.</span></span>

    <span data-ttu-id="2b0d7-295">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-295">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-296">Tabla MIME</span><span class="sxs-lookup"><span data-stu-id="2b0d7-296">MIME Table</span></span>](mime-table.md)
    -   [<span data-ttu-id="2b0d7-297">Tabla de extensión</span><span class="sxs-lookup"><span data-stu-id="2b0d7-297">Extension Table</span></span>](extension-table.md)
    -   [<span data-ttu-id="2b0d7-298">Modificar el registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-298">Modifying the Registry</span></span>](modifying-the-registry.md)

-   <span data-ttu-id="2b0d7-299">Cree una base de datos Windows Installer que instale variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-299">Author a Windows Installer database that installs environment variables.</span></span>

    <span data-ttu-id="2b0d7-300">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-300">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-301">Tabla de entorno</span><span class="sxs-lookup"><span data-stu-id="2b0d7-301">Environment Table</span></span>](environment-table.md)

-   <span data-ttu-id="2b0d7-302">Cree una base de datos Windows Installer que instale accesos directos.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-302">Author a Windows Installer database that installs shortcuts.</span></span>

    <span data-ttu-id="2b0d7-303">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-303">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-304">Tabla de acceso directo</span><span class="sxs-lookup"><span data-stu-id="2b0d7-304">Shortcut Table</span></span>](shortcut-table.md)
    -   [<span data-ttu-id="2b0d7-305">Tabla MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="2b0d7-305">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
    -   [<span data-ttu-id="2b0d7-306">Editar accesos directos del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-306">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="2b0d7-307">Ejemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-307">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2b0d7-308">Cree una base de datos Windows Installer que instale varias instancias de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-308">Author a Windows Installer database that installs multiple instances of applications.</span></span>

    <span data-ttu-id="2b0d7-309">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-309">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-310">Instalación de varias instancias de productos y revisiones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-310">Installing Multiple Instances of Products and Patches</span></span>](installing-multiple-instances-of-products-and-patches.md)
    -   [<span data-ttu-id="2b0d7-311">Crear varias instancias con transformaciones de instancia</span><span class="sxs-lookup"><span data-stu-id="2b0d7-311">Authoring Multiple Instances with Instance Transforms</span></span>](authoring-multiple-instances-with-instance-transforms.md)
    -   [<span data-ttu-id="2b0d7-312">Instalar varias instancias con transformaciones de instancia</span><span class="sxs-lookup"><span data-stu-id="2b0d7-312">Installing Multiple Instances with Instance Transforms</span></span>](installing-multiple-instances-with-instance-transforms.md)

-   <span data-ttu-id="2b0d7-313">Especifique las opciones y los Estados de selección de características predeterminados.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-313">Specify default feature selection states and options.</span></span>

    <span data-ttu-id="2b0d7-314">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-314">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-315">Grupo de tablas principales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-315">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="2b0d7-316">Tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-316">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="2b0d7-317">Tabla de características</span><span class="sxs-lookup"><span data-stu-id="2b0d7-317">Feature Table</span></span>](feature-table.md)
    -   [<span data-ttu-id="2b0d7-318">Tabla FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="2b0d7-318">FeatureComponents Table</span></span>](featurecomponents-table.md)
    -   [<span data-ttu-id="2b0d7-319">Control de los Estados de selección de características</span><span class="sxs-lookup"><span data-stu-id="2b0d7-319">Controlling Feature Selection States</span></span>](controlling-feature-selection-states.md)
    -   [<span data-ttu-id="2b0d7-320">Propiedades de opciones de instalación de características</span><span class="sxs-lookup"><span data-stu-id="2b0d7-320">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="2b0d7-321">Especifique las condiciones que deben cumplirse para instalar una aplicación o los componentes seleccionados.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-321">Specify conditions that must be met to install an application or selected components.</span></span>

    <span data-ttu-id="2b0d7-322">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-322">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-323">Tabla de condiciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-323">Condition Table</span></span>](condition-table.md)
    -   [<span data-ttu-id="2b0d7-324">Tabla LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="2b0d7-324">LaunchCondition Table</span></span>](launchcondition-table.md)
    -   [<span data-ttu-id="2b0d7-325">Tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-325">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="2b0d7-326">Usar propiedades en instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-326">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="2b0d7-327">Sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="2b0d7-327">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="2b0d7-328">Acciones de acondicionamiento que se ejecutan durante la eliminación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-328">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="2b0d7-329">Ejemplos de sintaxis de instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-329">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)

-   <span data-ttu-id="2b0d7-330">Cree la secuencia de acciones que se usa para instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-330">Author the sequence of actions used to install the application.</span></span>

    <span data-ttu-id="2b0d7-331">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-331">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-332">Usar una tabla de secuencia</span><span class="sxs-lookup"><span data-stu-id="2b0d7-332">Using a Sequence Table</span></span>](using-a-sequence-table.md)
    -   [<span data-ttu-id="2b0d7-333">Grupo de tablas de procedimientos de instalación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-333">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)
    -   [<span data-ttu-id="2b0d7-334">Ejemplo detallado de tabla de secuencias</span><span class="sxs-lookup"><span data-stu-id="2b0d7-334">Sequence Table Detailed Example</span></span>](sequence-table-detailed-example.md)
    -   [<span data-ttu-id="2b0d7-335">Acciones con restricciones de secuenciación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-335">Actions with Sequencing Restrictions</span></span>](actions-with-sequencing-restrictions.md)
    -   [<span data-ttu-id="2b0d7-336">Acciones sin restricciones de secuenciación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-336">Actions without Sequencing Restrictions</span></span>](actions-without-sequencing-restrictions.md)
    -   [<span data-ttu-id="2b0d7-337">Usar propiedades en instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-337">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="2b0d7-338">Sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="2b0d7-338">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="2b0d7-339">Ejemplos de sintaxis de instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-339">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
    -   [<span data-ttu-id="2b0d7-340">Acciones de acondicionamiento que se ejecutan durante la eliminación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-340">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="2b0d7-341">Acciones estándar</span><span class="sxs-lookup"><span data-stu-id="2b0d7-341">Standard Actions</span></span>](standard-actions.md)
    -   [<span data-ttu-id="2b0d7-342">Ejemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-342">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2b0d7-343">Preparar el paquete de instalación de la aplicación para futuras actualizaciones de la aplicación mediante el servicio de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-343">Prepare the installation package of the application for future upgrades of the application by the Windows Installer service.</span></span>

    <span data-ttu-id="2b0d7-344">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-344">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-345">Revisiones y actualizaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-345">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="2b0d7-346">Preparación de una aplicación para futuras actualizaciones principales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-346">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
    -   [<span data-ttu-id="2b0d7-347">Usar UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="2b0d7-347">Using an UpgradeCode</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="2b0d7-348">Actualizar tabla</span><span class="sxs-lookup"><span data-stu-id="2b0d7-348">Upgrade Table</span></span>](upgrade-table.md)
    -   [<span data-ttu-id="2b0d7-349">**Propiedad UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-349">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="2b0d7-350">Impedir que un paquete antiguo se instale en una versión más reciente</span><span class="sxs-lookup"><span data-stu-id="2b0d7-350">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [<span data-ttu-id="2b0d7-351">Cambiar el código de producto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-351">Changing the Product Code</span></span>](changing-the-product-code.md)
    -   [<span data-ttu-id="2b0d7-352">Actualizar ensamblados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-352">Updating Assemblies</span></span>](updating-assemblies.md)
    -   [<span data-ttu-id="2b0d7-353">Ejemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-353">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2b0d7-354">Solucionar problemas de los paquetes de Windows Installer en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-354">Troubleshoot Windows Installer packages under development.</span></span>

    <span data-ttu-id="2b0d7-355">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-355">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-356">Validación de paquetes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-356">Package Validation</span></span>](package-validation.md)
    -   [<span data-ttu-id="2b0d7-357">Evaluadores de coherencia interna-CIEM</span><span class="sxs-lookup"><span data-stu-id="2b0d7-357">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
    -   [<span data-ttu-id="2b0d7-358">Registro de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-358">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="2b0d7-359">Comprobar la instalación de características, componentes y archivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-359">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="2b0d7-360">Crear un paquete grande</span><span class="sxs-lookup"><span data-stu-id="2b0d7-360">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="2b0d7-361">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="2b0d7-361">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="2b0d7-362">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-362">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="2b0d7-363">Validar módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-363">Validating Merge Modules</span></span>](validating-merge-modules.md)
    -   [<span data-ttu-id="2b0d7-364">Validar una base de datos de instalación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-364">Validating an Installation Database</span></span>](validating-an-installation-database.md)
    -   [<span data-ttu-id="2b0d7-365">Validar una actualización de instalación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-365">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)
    -   [<span data-ttu-id="2b0d7-366">Buscar una característica o componente interrumpido</span><span class="sxs-lookup"><span data-stu-id="2b0d7-366">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="2b0d7-367">Windows Installer mensajes de error</span><span class="sxs-lookup"><span data-stu-id="2b0d7-367">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="2b0d7-368">Registro de solicitudes de reinicio</span><span class="sxs-lookup"><span data-stu-id="2b0d7-368">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="2b0d7-369">Asegúrese de configurar e instalar la aplicación de forma segura.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-369">Ensure a secure setup and installation of the application.</span></span>

    <span data-ttu-id="2b0d7-370">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-370">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-371">Directrices para crear instalaciones seguras</span><span class="sxs-lookup"><span data-stu-id="2b0d7-371">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="2b0d7-372">Directrices para proteger las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-372">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="2b0d7-373">Seguridad de la acción personalizada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-373">Custom Action Security</span></span>](custom-action-security.md)
    -   [<span data-ttu-id="2b0d7-374">Directrices para proteger paquetes en equipos bloqueados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-374">Guidelines for Securing Packages on Locked-Down Computers</span></span>](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [<span data-ttu-id="2b0d7-375">Crear una instalación firmada completamente comprobada mediante automatización</span><span class="sxs-lookup"><span data-stu-id="2b0d7-375">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [<span data-ttu-id="2b0d7-376">Ejemplo de instalación de Windows Installer basado en URL</span><span class="sxs-lookup"><span data-stu-id="2b0d7-376">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="2b0d7-377">Crear la interfaz de usuario para la entrada de contraseña</span><span class="sxs-lookup"><span data-stu-id="2b0d7-377">Authoring the User Interface for Password Input</span></span>](authoring-the-user-interface-for-password-input.md)
    -   [<span data-ttu-id="2b0d7-378">Firmas digitales y Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-378">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
    -   [<span data-ttu-id="2b0d7-379">Uso de Windows Installer con UAC</span><span class="sxs-lookup"><span data-stu-id="2b0d7-379">Using Windows Installer with UAC</span></span>](using-windows-installer-with-uac.md)
    -   [<span data-ttu-id="2b0d7-380">Revisión de control de cuentas de usuario (UAC)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-380">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
    -   [<span data-ttu-id="2b0d7-381">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="2b0d7-381">Msicert.exe</span></span>](msicert-exe.md)
    -   [<span data-ttu-id="2b0d7-382">**Propiedad AdminUser**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-382">**AdminUser property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="2b0d7-383">**Propiedad privileged**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-383">**Privileged property**</span></span>](privileged.md)
    -   [<span data-ttu-id="2b0d7-384">**Propiedad SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-384">**SecureCustomProperties property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="2b0d7-385">Cree una interfaz de usuario para presentar las opciones de configuración de la instalación y obtener información del usuario sobre el proceso de instalación pendiente.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-385">Create a user interface to present options to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="2b0d7-386">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-386">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-387">Acerca de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2b0d7-387">About the User Interface</span></span>](about-the-user-interface.md)
    -   [<span data-ttu-id="2b0d7-388">Agregar controles y texto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-388">Adding Controls and Text</span></span>](adding-controls-and-text.md)
    -   [<span data-ttu-id="2b0d7-389">Crear un control ProgressBar</span><span class="sxs-lookup"><span data-stu-id="2b0d7-389">Authoring a ProgressBar Control</span></span>](authoring-a-progressbar-control.md)
    -   [<span data-ttu-id="2b0d7-390">Creación de mensajes de solicitud de disco</span><span class="sxs-lookup"><span data-stu-id="2b0d7-390">Authoring Disk Prompt Messages</span></span>](authoring-disk-prompt-messages.md)
    -   [<span data-ttu-id="2b0d7-391">Creación de una instrucción condicional "espere...." Cuadro de mensaje</span><span class="sxs-lookup"><span data-stu-id="2b0d7-391">Authoring a Conditional "Please Wait . . ." Message Box</span></span>](authoring-a-conditional-please-wait-------message-box.md)
    -   [<span data-ttu-id="2b0d7-392">Obtener una vista previa de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2b0d7-392">Previewing the User Interface</span></span>](previewing-the-user-interface.md)
    -   [<span data-ttu-id="2b0d7-393">Agregar texto almacenado en una propiedad</span><span class="sxs-lookup"><span data-stu-id="2b0d7-393">Adding Text Stored in a Property</span></span>](adding-text-stored-in-a-property.md)
    -   [<span data-ttu-id="2b0d7-394">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-394">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   <span data-ttu-id="2b0d7-395">Cree una interfaz de usuario externa para presentar una interfaz de usuario personalizada con el fin de configurar la instalación y obtener información del usuario sobre el proceso de instalación pendiente.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-395">Create an external user interface to present a custom user interface to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="2b0d7-396">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-396">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-397">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-397">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [<span data-ttu-id="2b0d7-398">Supervisión de una instalación mediante MsiSetExternalUIRecord</span><span class="sxs-lookup"><span data-stu-id="2b0d7-398">Monitoring an Installation Using MsiSetExternalUIRecord</span></span>](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [<span data-ttu-id="2b0d7-399">Analizar mensajes de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-399">Parsing Windows Installer Messages</span></span>](parsing-windows-installer-messages.md)
    -   [<span data-ttu-id="2b0d7-400">Devolver valores de un controlador de interfaz de usuario externo</span><span class="sxs-lookup"><span data-stu-id="2b0d7-400">Returning Values from an External User Interface Handler</span></span>](returning-values-from-an-external-user-interface-handler.md)
    -   [<span data-ttu-id="2b0d7-401">\_controlador INSTALLUI</span><span class="sxs-lookup"><span data-stu-id="2b0d7-401">INSTALLUI\_HANDLER</span></span>](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [<span data-ttu-id="2b0d7-402">Controlar los mensajes de progreso mediante MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="2b0d7-402">Handling Progress Messages Using MsiSetExternalUI</span></span>](handling-progress-messages-using-msisetexternalui.md)
    -   [<span data-ttu-id="2b0d7-403">Supervisión de una instalación mediante MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="2b0d7-403">Monitoring an Installation Using MsiSetExternalUI</span></span>](monitoring-an-installation-using-msisetexternalui.md)

-   <span data-ttu-id="2b0d7-404">Establezca la información de la aplicación en **Agregar o quitar programas** (ARP).</span><span class="sxs-lookup"><span data-stu-id="2b0d7-404">Set information for the application in **Add/Remove Programs** (ARP.)</span></span>

    <span data-ttu-id="2b0d7-405">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-405">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-406">Configuración de agregar o quitar programas con Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-406">Configuring Add/Remove Programs with Windows Installer</span></span>](configuring-add-remove-programs-with-windows-installer.md)
    -   [<span data-ttu-id="2b0d7-407">Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-407">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="2b0d7-408">Desinstalar la clave del registro</span><span class="sxs-lookup"><span data-stu-id="2b0d7-408">Uninstall Registry Key</span></span>](uninstall-registry-key.md)

-   <span data-ttu-id="2b0d7-409">Escriba acciones personalizadas para controlar la lógica de configuración que no se admite de forma nativa en Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-409">Write custom actions to handle setup logic that is not natively supported by Windows Installer.</span></span>

    <span data-ttu-id="2b0d7-410">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-410">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-411">Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-411">Custom Actions</span></span>](custom-actions.md)
    -   [<span data-ttu-id="2b0d7-412">Lista de Resumen de todos los tipos de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-412">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)
    -   [<span data-ttu-id="2b0d7-413">Directrices para proteger las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-413">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="2b0d7-414">Referencia de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-414">Custom Action Reference</span></span>](custom-action-reference.md)
    -   [<span data-ttu-id="2b0d7-415">Usar una acción personalizada para crear cuentas de usuario en un equipo local</span><span class="sxs-lookup"><span data-stu-id="2b0d7-415">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="2b0d7-416">Usar una acción personalizada para iniciar un archivo instalado al final de la instalación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-416">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [<span data-ttu-id="2b0d7-417">Obtener acceso a una base de datos o una sesión desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-417">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="2b0d7-418">Obtener acceso a la sesión del instalador actual desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-418">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="2b0d7-419">Cambiar el estado del sistema mediante una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-419">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)

-   <span data-ttu-id="2b0d7-420">Arranque el Windows Installer en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-420">Bootstrap the Windows Installer onto a user's computer.</span></span>

    <span data-ttu-id="2b0d7-421">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-421">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-422">Arranque</span><span class="sxs-lookup"><span data-stu-id="2b0d7-422">Bootstrapping</span></span>](bootstrapping.md)
    -   [<span data-ttu-id="2b0d7-423">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="2b0d7-423">Instmsi.exe</span></span>](instmsi-exe.md)
    -   [<span data-ttu-id="2b0d7-424">Arranque de descarga de Internet</span><span class="sxs-lookup"><span data-stu-id="2b0d7-424">Internet Download Bootstrapping</span></span>](internet-download-bootstrapping.md)
    -   [<span data-ttu-id="2b0d7-425">Msistuff.exe</span><span class="sxs-lookup"><span data-stu-id="2b0d7-425">Msistuff.exe</span></span>](msistuff-exe.md)
    -   [<span data-ttu-id="2b0d7-426">Ejemplo de instalación de Windows Installer basado en URL</span><span class="sxs-lookup"><span data-stu-id="2b0d7-426">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="2b0d7-427">Configuración de los recursos de Setup.exe</span><span class="sxs-lookup"><span data-stu-id="2b0d7-427">Configuring the Setup.exe Resources</span></span>](configuring-the-setup-exe-resources.md)
    -   [<span data-ttu-id="2b0d7-428">Descarga de una instalación desde Internet</span><span class="sxs-lookup"><span data-stu-id="2b0d7-428">Downloading an Installation from the Internet</span></span>](downloading-an-installation-from-the-internet.md)

-   <span data-ttu-id="2b0d7-429">Siga las instrucciones de Active Accessibility al escribir paquetes de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-429">Adhere to Active Accessibility guidelines when writing Windows Installer packages.</span></span>

    <span data-ttu-id="2b0d7-430">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-430">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-431">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="2b0d7-431">Accessibility</span></span>](accessibility.md)

-   <span data-ttu-id="2b0d7-432">Prepárese para la internacionalización de una instalación de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-432">Prepare for the internationalization of an application setup.</span></span>

    <span data-ttu-id="2b0d7-433">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-433">For more information, see the following:</span></span>

    -   <span data-ttu-id="2b0d7-434">[Preparación de un paquete de Windows Installer para la localización](preparing-a-windows-installer-package-for-localization.md)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-434">[Preparing a Windows Installer Package for Localization](preparing-a-windows-installer-package-for-localization.md),</span></span>
    -   [<span data-ttu-id="2b0d7-435">Localizar un paquete de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-435">Localizing a Windows Installer Package</span></span>](localizing-a-windows-installer-package.md)
    -   [<span data-ttu-id="2b0d7-436">Control de páginas de códigos (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-436">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
    -   [<span data-ttu-id="2b0d7-437">Agregar recursos localizados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-437">Adding Localized Resources</span></span>](adding-localized-resources.md)
    -   [<span data-ttu-id="2b0d7-438">Un ejemplo de localización</span><span class="sxs-lookup"><span data-stu-id="2b0d7-438">A Localization Example</span></span>](a-localization-example.md)
    -   [<span data-ttu-id="2b0d7-439">Localizar las tablas de error y ActionText</span><span class="sxs-lookup"><span data-stu-id="2b0d7-439">Localizing the Error and ActionText Tables</span></span>](localizing-the-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="2b0d7-440">Localizar columnas de base de datos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-440">Localizing Database Columns</span></span>](localizing-database-columns.md)
    -   [<span data-ttu-id="2b0d7-441">Crear una base de datos con una página de códigos neutra</span><span class="sxs-lookup"><span data-stu-id="2b0d7-441">Creating a Database with a Neutral Code Page</span></span>](creating-a-database-with-a-neutral-code-page.md)
    -   [<span data-ttu-id="2b0d7-442">Control de páginas de códigos de tablas importadas y exportadas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-442">Code Page Handling of Imported and Exported Tables</span></span>](code-page-handling-of-imported-and-exported-tables.md)
    -   [<span data-ttu-id="2b0d7-443">Localizar el idioma que se muestra en los cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="2b0d7-443">Localizing the Language Displayed by Dialogs</span></span>](localizing-the-language-displayed-by-dialogs.md)
    -   [<span data-ttu-id="2b0d7-444">Importación de tablas de error y de ActionText localizadas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-444">Importing Localized Error and ActionText Tables</span></span>](importing-localized-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="2b0d7-445">Actualización de las propiedades ProductLanguage y ProductCode</span><span class="sxs-lookup"><span data-stu-id="2b0d7-445">Updating ProductLanguage and ProductCode Properties</span></span>](updating-productlanguage-and-productcode-properties.md)
    -   [<span data-ttu-id="2b0d7-446">Actualizar una secuencia de información de Resumen</span><span class="sxs-lookup"><span data-stu-id="2b0d7-446">Updating a Summary Information Stream</span></span>](updating-a-summary-information-stream.md)
    -   [<span data-ttu-id="2b0d7-447">Componentes completos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-447">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="2b0d7-448">Tabla UIText</span><span class="sxs-lookup"><span data-stu-id="2b0d7-448">UIText Table</span></span>](uitext-table.md)
    -   [<span data-ttu-id="2b0d7-449">Administrar idioma y página de códigos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-449">Manage Language and Codepage</span></span>](manage-language-and-codepage.md)
    -   [<span data-ttu-id="2b0d7-450">Comprobar la página de códigos de la base de datos de instalación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-450">Checking the Installation Database Code Page</span></span>](checking-the-installation-database-code-page.md)

-   <span data-ttu-id="2b0d7-451">Cree paquetes de Windows Installer para plataformas de 32 bits y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-451">Create Windows Installer packages for 32-bit and 64-bit platforms.</span></span>

    <span data-ttu-id="2b0d7-452">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-452">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-453">Windows Installer en sistemas operativos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2b0d7-453">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="2b0d7-454">Acciones personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2b0d7-454">64-Bit Custom Actions</span></span>](64-bit-custom-actions.md)
    -   [<span data-ttu-id="2b0d7-455">Uso de acciones personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2b0d7-455">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)
    -   [<span data-ttu-id="2b0d7-456">Usar módulos de combinación de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2b0d7-456">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)

-   <span data-ttu-id="2b0d7-457">Redistribuir los componentes Windows Installer compartidos y la lógica de configuración como módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-457">Redistribute shared Windows Installer components and setup logic as merge modules.</span></span>

    <span data-ttu-id="2b0d7-458">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-458">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-459">Módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-459">Merge Modules</span></span>](merge-modules.md)
    -   [<span data-ttu-id="2b0d7-460">Crear una transformación de idioma para un módulo de combinación de varios idiomas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-460">Authoring a Language Transform for a Multiple Language Merge Module</span></span>](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [<span data-ttu-id="2b0d7-461">Aplicar un módulo de combinación configurable con personalizaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-461">Applying a Configurable Merge Module with Customizations</span></span>](applying-a-configurable-merge-module-with-customizations.md)

-   <span data-ttu-id="2b0d7-462">Programar o suprimir los reinicios durante una instalación Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-462">Schedule or suppress reboots during a Windows Installer installation.</span></span>

    <span data-ttu-id="2b0d7-463">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-463">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-464">Reinicios del sistema</span><span class="sxs-lookup"><span data-stu-id="2b0d7-464">System Reboots</span></span>](system-reboots.md)
    -   [<span data-ttu-id="2b0d7-465">Registro de solicitudes de reinicio</span><span class="sxs-lookup"><span data-stu-id="2b0d7-465">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="2b0d7-466">Cree actualizaciones o correcciones para una aplicación existente mediante la creación de una revisión.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-466">Create updates or fixes for an existing application by creating a patch.</span></span>

    <span data-ttu-id="2b0d7-467">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-467">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-468">Crear una revisión de actualización pequeña</span><span class="sxs-lookup"><span data-stu-id="2b0d7-468">Creating a Small Update Patch</span></span>](creating-a-small-update-patch.md)
    -   [<span data-ttu-id="2b0d7-469">Un pequeño ejemplo de revisión de actualización</span><span class="sxs-lookup"><span data-stu-id="2b0d7-469">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

-   <span data-ttu-id="2b0d7-470">Cree un paquete de propósito dual capaz de instalar una aplicación para solo el usuario actual o para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-470">Author a dual-purpose package capable of installing an application either for only the current user or for all users of the computer.</span></span>

    <span data-ttu-id="2b0d7-471">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-471">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-472">Contexto de instalación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-472">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="2b0d7-473">Creación de un solo paquete</span><span class="sxs-lookup"><span data-stu-id="2b0d7-473">Single Package Authoring</span></span>](single-package-authoring.md)
    -   [<span data-ttu-id="2b0d7-474">Ejemplo de creación de un solo paquete</span><span class="sxs-lookup"><span data-stu-id="2b0d7-474">Single Package Authoring Example</span></span>](single-package-authoring-example.md)

-   <span data-ttu-id="2b0d7-475">Personalizar servicios en el equipo mediante el Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-475">Customize services on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="2b0d7-476">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-476">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-477">Uso de la configuración de servicios</span><span class="sxs-lookup"><span data-stu-id="2b0d7-477">Using Services Configuration</span></span>](using-services-configuration.md)

-   <span data-ttu-id="2b0d7-478">Proteja los recursos del equipo mediante el Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-478">Secure resources on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="2b0d7-479">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-479">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-480">Directrices para crear instalaciones seguras</span><span class="sxs-lookup"><span data-stu-id="2b0d7-480">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="2b0d7-481">Proteger recursos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-481">Securing Resources</span></span>](securing-resources-.md)

-   <span data-ttu-id="2b0d7-482">Enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de la clave del componente.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-482">Enumerate all components installed on the computer and obtain the key path for the component.</span></span>

    <span data-ttu-id="2b0d7-483">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-483">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-484">Enumerar componentes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-484">Enumerating Components</span></span>](enumerating-components-.md)

-   <span data-ttu-id="2b0d7-485">Instalar varios paquetes mediante el [*procesamiento de transacciones*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2b0d7-485">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="2b0d7-486">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-486">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-487">Instalaciones de varios paquetes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-487">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="2b0d7-488">Inserte una interfaz de usuario personalizada en el paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-488">Embed a custom user interface in the Windows Installer package.</span></span>

    <span data-ttu-id="2b0d7-489">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-489">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-490">Uso de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2b0d7-490">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="2b0d7-491">Usar una interfaz de usuario incrustada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-491">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="it-professionals"></a><span data-ttu-id="2b0d7-492">Profesionales de TI</span><span class="sxs-lookup"><span data-stu-id="2b0d7-492">IT Professionals</span></span>

<span data-ttu-id="2b0d7-493">Los profesionales de ti y los administradores personalizan e implementan paquetes de Windows Installer existentes.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-493">IT Professionals and Administrators customize and deploy existing Windows Installer packages.</span></span> <span data-ttu-id="2b0d7-494">Estos usuarios reempaquetan las configuraciones de las aplicaciones existentes en Windows Installer paquetes de instalación, e instalan y mantienen imágenes administrativas de instalaciones de Windows Installer en redes.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-494">These users repackage setups for existing applications into Windows Installer installation packages, and install and maintain administrative images of Windows Installer installations on networks.</span></span>

-   <span data-ttu-id="2b0d7-495">Personalización de aplicaciones y configuración mediante la generación y aplicación de transformaciones de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-495">Customize applications and setup by generating and applying Windows Installer transforms</span></span>

    <span data-ttu-id="2b0d7-496">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-496">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-497">Personalización</span><span class="sxs-lookup"><span data-stu-id="2b0d7-497">Customization</span></span>](customization.md)
    -   [<span data-ttu-id="2b0d7-498">Transformaciones de base de datos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-498">Database Transforms</span></span>](database-transforms.md)
    -   [<span data-ttu-id="2b0d7-499">Ejemplo de transformación de personalización</span><span class="sxs-lookup"><span data-stu-id="2b0d7-499">A Customization Transform Example</span></span>](a-customization-transform-example.md)
    -   [<span data-ttu-id="2b0d7-500">Combinaciones y transformaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-500">Merges and Transforms</span></span>](merges-and-transforms.md)
    -   [<span data-ttu-id="2b0d7-501">Usar transformaciones para agregar recursos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-501">Using Transforms to Add Resources</span></span>](using-transforms-to-add-resources.md)
    -   [<span data-ttu-id="2b0d7-502">Generar una transformación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-502">Generate a Transform</span></span>](generate-a-transform.md)
    -   [<span data-ttu-id="2b0d7-503">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-503">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="2b0d7-504">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="2b0d7-504">Msitran.exe</span></span>](msitran-exe.md)
    -   [<span data-ttu-id="2b0d7-505">Aplicar una transformación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-505">Apply a Transform</span></span>](apply-a-transform.md)
    -   [<span data-ttu-id="2b0d7-506">Ver una transformación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-506">View a Transform</span></span>](view-a-transform.md)
    -   [<span data-ttu-id="2b0d7-507">Ver las diferencias entre dos bases de datos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-507">View Differences Between Two Databases</span></span>](view-differences-between-two-databases.md)
    -   [<span data-ttu-id="2b0d7-508">Aplicación de revisiones a aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="2b0d7-508">Patching Customized Applications</span></span>](patching-customized-applications.md)

-   <span data-ttu-id="2b0d7-509">Implementar un paquete de instalación de Windows Installer, una actualización o una revisión.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-509">Deploy a Windows Installer installation package, update, or patch.</span></span>

    <span data-ttu-id="2b0d7-510">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-510">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-511">Instalación de una aplicación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-511">Installing an Application</span></span>](installing-an-application.md)
    -   [<span data-ttu-id="2b0d7-512">Revisiones y actualizaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-512">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="2b0d7-513">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="2b0d7-513">Transforms</span></span>](transforms.md)
    -   [<span data-ttu-id="2b0d7-514">Instalación de un paquete con privilegios elevados para un no administrador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-514">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="2b0d7-515">Aplicar las actualizaciones principales mediante la revisión de la instalación local del producto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-515">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="2b0d7-516">Aplicar las actualizaciones principales instalando el producto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-516">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="2b0d7-517">Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-517">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="2b0d7-518">Aplicar actualizaciones pequeñas reinstalando el producto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-518">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="2b0d7-519">Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa</span><span class="sxs-lookup"><span data-stu-id="2b0d7-519">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="2b0d7-520">Aplicar revisiones a las instalaciones iniciales</span><span class="sxs-lookup"><span data-stu-id="2b0d7-520">Patching Initial Installations</span></span>](patching-initial-installations.md)
    -   [<span data-ttu-id="2b0d7-521">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-521">Command Line Options</span></span>](command-line-options.md)

-   <span data-ttu-id="2b0d7-522">Solucionar problemas de Windows Installer paquetes.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-522">Troubleshoot Windows Installer packages.</span></span>

    <span data-ttu-id="2b0d7-523">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-523">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-524">Registro de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-524">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="2b0d7-525">Comprobar la instalación de características, componentes y archivos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-525">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="2b0d7-526">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="2b0d7-526">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="2b0d7-527">Buscar una característica o componente interrumpido</span><span class="sxs-lookup"><span data-stu-id="2b0d7-527">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="2b0d7-528">Windows Installer mensajes de error</span><span class="sxs-lookup"><span data-stu-id="2b0d7-528">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="2b0d7-529">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="2b0d7-529">Msicert.exe</span></span>](msicert-exe.md)

-   <span data-ttu-id="2b0d7-530">Use el scripting para consultar los paquetes de Windows Installer para obtener información sobre un producto y modificar la instalación.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-530">Use scripting to query Windows Installer packages for information about a product and modify the installation.</span></span>

    <span data-ttu-id="2b0d7-531">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-531">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-532">Interfaz de automatización</span><span class="sxs-lookup"><span data-stu-id="2b0d7-532">Automation Interface</span></span>](automation-interface.md)
    -   [<span data-ttu-id="2b0d7-533">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b0d7-533">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
    -   [<span data-ttu-id="2b0d7-534">Usar Windows Installer con WMI</span><span class="sxs-lookup"><span data-stu-id="2b0d7-534">Using Windows Installer with WMI</span></span>](using-windows-installer-with-wmi.md)

-   <span data-ttu-id="2b0d7-535">Crear y mantener instalaciones administrativas.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-535">Create and maintain administrative installations.</span></span>

    <span data-ttu-id="2b0d7-536">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-536">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-537">Instalación administrativa</span><span class="sxs-lookup"><span data-stu-id="2b0d7-537">Administrative Installation</span></span>](administrative-installation.md)
    -   [<span data-ttu-id="2b0d7-538">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-538">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="2b0d7-539">**Propiedad AdminProperties**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-539">**AdminProperties Property**</span></span>](adminproperties.md)
    -   [<span data-ttu-id="2b0d7-540">Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa</span><span class="sxs-lookup"><span data-stu-id="2b0d7-540">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="2b0d7-541">Aplicar un paquete de revisión a una instalación administrativa</span><span class="sxs-lookup"><span data-stu-id="2b0d7-541">Applying a Patch Package to an Administrative Installation</span></span>](applying-a-patch-package-to-an-administrative-installation.md)
    -   [<span data-ttu-id="2b0d7-542">Orden de ejecución de la acción</span><span class="sxs-lookup"><span data-stu-id="2b0d7-542">Action Execution Order</span></span>](action-execution-order.md)
    -   [<span data-ttu-id="2b0d7-543">**Propiedad IsAdminPackage**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-543">**IsAdminPackage Property**</span></span>](isadminpackage.md)
    -   [<span data-ttu-id="2b0d7-544">Orden de prioridad de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b0d7-544">Order of Property Precedence</span></span>](order-of-property-precedence.md)
    -   [<span data-ttu-id="2b0d7-545">**Propiedad AdminProperties**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-545">**AdminProperties Property**</span></span>](adminproperties.md)

-   <span data-ttu-id="2b0d7-546">Hacer que una aplicación esté disponible para todos los usuarios de un equipo o solo para un usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-546">Make an application available to all users of a computer or to a specified user only.</span></span>

    <span data-ttu-id="2b0d7-547">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-547">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-548">Contexto de instalación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-548">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="2b0d7-549">**Propiedad ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-549">**ALLUSERS Property**</span></span>](allusers.md)

-   <span data-ttu-id="2b0d7-550">Interpretar paquetes, instalar productos y configurar opciones de características mediante una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-550">Interpret packages, install products, and configure feature options using a command line.</span></span>

    <span data-ttu-id="2b0d7-551">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-551">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-552">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-552">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="2b0d7-553">Establecer valores de propiedades públicas en la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-553">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
    -   [<span data-ttu-id="2b0d7-554">Obtener y establecer propiedades</span><span class="sxs-lookup"><span data-stu-id="2b0d7-554">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
    -   [<span data-ttu-id="2b0d7-555">Reinstalación de una característica o aplicación</span><span class="sxs-lookup"><span data-stu-id="2b0d7-555">Reinstalling a Feature or Application</span></span>](reinstalling-a-feature-or-application.md)
    -   [<span data-ttu-id="2b0d7-556">Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-556">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="2b0d7-557">Aplicar actualizaciones pequeñas reinstalando el producto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-557">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="2b0d7-558">Cambiar la ubicación de destino de un directorio</span><span class="sxs-lookup"><span data-stu-id="2b0d7-558">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="2b0d7-559">Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa</span><span class="sxs-lookup"><span data-stu-id="2b0d7-559">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="2b0d7-560">Aplicar las actualizaciones principales instalando el producto</span><span class="sxs-lookup"><span data-stu-id="2b0d7-560">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="2b0d7-561">Propiedades de configuración</span><span class="sxs-lookup"><span data-stu-id="2b0d7-561">Configuration Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="2b0d7-562">Propiedades de opciones de instalación de características</span><span class="sxs-lookup"><span data-stu-id="2b0d7-562">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="2b0d7-563">Trabaje con la Directiva para administrar derechos y permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-563">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="2b0d7-564">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-564">For more information, see the following:</span></span>

    -   <span data-ttu-id="2b0d7-565">[Directivas de equipo](machine-policies.md),</span><span class="sxs-lookup"><span data-stu-id="2b0d7-565">[Machine Policies](machine-policies.md),</span></span>
    -   <span data-ttu-id="2b0d7-566">[Directivas de usuario](user-policies.md),</span><span class="sxs-lookup"><span data-stu-id="2b0d7-566">[User Policies](user-policies.md),</span></span>
    -   [<span data-ttu-id="2b0d7-567">Instalación de un paquete con privilegios elevados para un no administrador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-567">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="2b0d7-568">Anunciar una aplicación Per-User que se va a instalar con privilegios elevados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-568">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="2b0d7-569">Usar una acción personalizada para crear cuentas de usuario en un equipo local</span><span class="sxs-lookup"><span data-stu-id="2b0d7-569">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="2b0d7-570">**Propiedad AdminUser**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-570">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="2b0d7-571">**Propiedad privileged**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-571">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="2b0d7-572">**Propiedad EnableUserControl**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-572">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="2b0d7-573">**UserSID (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-573">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="2b0d7-574">**Propiedad SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-574">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="2b0d7-575">Instalar varios paquetes mediante el [*procesamiento de transacciones*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2b0d7-575">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="2b0d7-576">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-576">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-577">Instalaciones de varios paquetes</span><span class="sxs-lookup"><span data-stu-id="2b0d7-577">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="2b0d7-578">Incrustar una interfaz de usuario personalizada dentro de un paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-578">Embed a custom user interface within a Windows Installer package..</span></span>

    <span data-ttu-id="2b0d7-579">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-579">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-580">Uso de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2b0d7-580">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="2b0d7-581">Usar una interfaz de usuario incrustada</span><span class="sxs-lookup"><span data-stu-id="2b0d7-581">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a><span data-ttu-id="2b0d7-582">Desarrolladores de infraestructura</span><span class="sxs-lookup"><span data-stu-id="2b0d7-582">Infrastructure Developers</span></span>

<span data-ttu-id="2b0d7-583">Los desarrolladores de infraestructura pueden crear plataformas unificadas para la implementación y administración de software que usa el servicio de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-583">Infrastructure Developers can create unified platforms for the deployment and management of software that uses the Windows Installer service.</span></span> <span data-ttu-id="2b0d7-584">Pueden utilizar la interfaz de programación de Windows Installer para consultar, administrar y distribuir aplicaciones, revisiones y orígenes en un sistema.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-584">They can use the Windows Installer programming interface to query, manage, and distribute applications, patches, and sources on a system.</span></span>

-   <span data-ttu-id="2b0d7-585">Buscar, inventariar y consultar el estado, la información y los clientes de los componentes.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-585">Locate, inventory and query for the state, information, and clients of components.</span></span>

    <span data-ttu-id="2b0d7-586">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-586">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-587">Funciones específicas del componente</span><span class="sxs-lookup"><span data-stu-id="2b0d7-587">Component-Specific Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-588">Funciones de estado del sistema</span><span class="sxs-lookup"><span data-stu-id="2b0d7-588">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-589">Instalador (objeto)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-589">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="2b0d7-590">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="2b0d7-590">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="2b0d7-591">Patch (objeto)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-591">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2b0d7-592">Inventario y consulta para obtener información y el estado de los productos y las características.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-592">Inventory and query for information and the state of products and features.</span></span>

    <span data-ttu-id="2b0d7-593">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-593">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-594">Productos y revisiones de inventario</span><span class="sxs-lookup"><span data-stu-id="2b0d7-594">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="2b0d7-595">Funciones de estado del sistema</span><span class="sxs-lookup"><span data-stu-id="2b0d7-595">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-596">Funciones de consulta de productos</span><span class="sxs-lookup"><span data-stu-id="2b0d7-596">Product Query Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-597">Instalador (objeto)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-597">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="2b0d7-598">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="2b0d7-598">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="2b0d7-599">Patch (objeto)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-599">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2b0d7-600">Mejore la resistencia de origen mediante el Windows Installer para inventariar, consultar y modificar la lista de origen de las aplicaciones, las actualizaciones y las revisiones.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-600">Improve source resiliency by using the Windows Installer to inventory, query, and modify the source list of applications, upgrades, and patches.</span></span>

    <span data-ttu-id="2b0d7-601">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-601">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-602">**Propiedad SOURCELIST**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-602">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="2b0d7-603">**Resistencia de origen**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-603">**Source Resiliency**</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="2b0d7-604">Funciones de instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="2b0d7-604">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-605">Instalador (objeto)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-605">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="2b0d7-606">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="2b0d7-606">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="2b0d7-607">Patch (objeto)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-607">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2b0d7-608">Mejore la resistencia de origen mediante el Windows Installer para inventariar, consultar y modificar orígenes de medios.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-608">Improve source resiliency by using the Windows Installer to inventory, query, and modify media sources.</span></span>

    <span data-ttu-id="2b0d7-609">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-609">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-610">**Propiedad SOURCELIST**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-610">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="2b0d7-611">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="2b0d7-611">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="2b0d7-612">Funciones de instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="2b0d7-612">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-613">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="2b0d7-613">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="2b0d7-614">Patch (objeto)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-614">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2b0d7-615">Inventario y consulta para obtener información y el estado de las revisiones.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-615">Inventory and query for information and the state of patches.</span></span>

    <span data-ttu-id="2b0d7-616">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-616">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-617">Productos y revisiones de inventario</span><span class="sxs-lookup"><span data-stu-id="2b0d7-617">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="2b0d7-618">Referencia de funciones del instalador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-618">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2b0d7-619">Patch (objeto)</span><span class="sxs-lookup"><span data-stu-id="2b0d7-619">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2b0d7-620">Trabaje con la Directiva para administrar derechos y permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="2b0d7-620">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="2b0d7-621">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b0d7-621">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2b0d7-622">Directivas de equipo</span><span class="sxs-lookup"><span data-stu-id="2b0d7-622">Machine Policies</span></span>](machine-policies.md)
    -   [<span data-ttu-id="2b0d7-623">Directivas de usuario</span><span class="sxs-lookup"><span data-stu-id="2b0d7-623">User Policies</span></span>](user-policies.md)
    -   [<span data-ttu-id="2b0d7-624">Instalación de un paquete con privilegios elevados para un no administrador</span><span class="sxs-lookup"><span data-stu-id="2b0d7-624">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="2b0d7-625">Anunciar una aplicación Per-User que se va a instalar con privilegios elevados</span><span class="sxs-lookup"><span data-stu-id="2b0d7-625">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="2b0d7-626">Usar una acción personalizada para crear cuentas de usuario en un equipo local</span><span class="sxs-lookup"><span data-stu-id="2b0d7-626">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="2b0d7-627">**Propiedad AdminUser**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-627">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="2b0d7-628">**Propiedad privileged**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-628">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="2b0d7-629">**Propiedad EnableUserControl**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-629">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="2b0d7-630">**UserSID (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-630">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="2b0d7-631">**Propiedad SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="2b0d7-631">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

 

 



