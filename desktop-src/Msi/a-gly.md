---
description: Obtenga información Windows Installer conceptos que comienzan con la letra A, como la fase de accesibilidad y adquisición.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011128"
---
# <a name="a-windows-installer"></a><span data-ttu-id="5a5f4-103">A (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="5a5f4-103">A (Windows Installer)</span></span>

<span data-ttu-id="5a5f4-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="5a5f4-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="5a5f4-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="5a5f4-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="5a5f4-106">Diseñe la implementación para que la interfaz de usuario del instalador sea accesible para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="5a5f4-107">Para obtener más información sobre la accesibilidad, vea el tema de información general: [Accesibilidad](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="5a5f4-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a5f4-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase de adquisición**</span><span class="sxs-lookup"><span data-stu-id="5a5f4-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="5a5f4-109">Fase de instalación durante la cual el instalador determina el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="5a5f4-110">La fase de adquisición comienza cuando una aplicación o un [*usuario Windows Installer*](m-gly.md) que instale una aplicación o característica.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="5a5f4-111">A continuación, el instalador consulta [*la base de*](i-gly.md) datos para obtener información a medida que genera el script de [*ejecución*](e-gly.md) para la instalación.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="5a5f4-112">Para obtener más información sobre las fases de una instalación, vea [Mecanismo de instalación](installation-mechanism.md)de .</span><span class="sxs-lookup"><span data-stu-id="5a5f4-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a5f4-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Acción**</span><span class="sxs-lookup"><span data-stu-id="5a5f4-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="5a5f4-114">Muchas de las funciones realizadas por Windows Installer se encapsulan en acciones.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="5a5f4-115">Cada acción especifica la ejecución de una función determinada y el flujo de procedimientos total de la instalación se prescribe mediante la secuencia de acciones de las [*tablas sequence*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5a5f4-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="5a5f4-116">[*Las acciones estándar*](s-gly.md) están integradas en Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="5a5f4-117">[*El autor*](c-gly.md) del paquete de instalación escribe acciones [*personalizadas.*](p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="5a5f4-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a5f4-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modo de aprobación de administrador**</span><span class="sxs-lookup"><span data-stu-id="5a5f4-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="5a5f4-119">Estado de aprobación habilitado por La protección de cuentas de usuario (UAC) que ejecuta todos los usuarios con privilegios mínimos, incluidos los administradores.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="5a5f4-120">Los usuarios deben dar su consentimiento para elevar las instalaciones que requieren privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="5a5f4-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Publicidad**</span><span class="sxs-lookup"><span data-stu-id="5a5f4-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="5a5f4-122">Capacidad para hacer que las interfaces necesarias para cargar y para que una aplicación esté disponible sin instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="5a5f4-123">Cuando un usuario o una aplicación activa una interfaz anunciada, el instalador continúa con la instalación de los componentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="5a5f4-124">Los dos tipos de publicidad son [*asignar*](/windows) y [*publicar*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5a5f4-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="5a5f4-125">Para obtener más información, vea [*también instalación a petición.*](i-gly.md)</span><span class="sxs-lookup"><span data-stu-id="5a5f4-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="5a5f4-126">Para obtener más información sobre cómo el instalador anuncia aplicaciones, vea [Anuncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="5a5f4-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a5f4-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span><span class="sxs-lookup"><span data-stu-id="5a5f4-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="5a5f4-128">Un servicio del sistema de Windows Vista que facilita el inicio de instalaciones que requieren privilegios elevados para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="5a5f4-129">Proporciona la interfaz de usuario de consentimiento que usa el control de cuentas de usuario para solicitar a un usuario autorización de administrador.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="5a5f4-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**Asignar**</span><span class="sxs-lookup"><span data-stu-id="5a5f4-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="5a5f4-131">Hace que una aplicación esté disponible y parezca que se ha instalado para un usuario, sin instalarla realmente.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="5a5f4-132">La asignación agrega accesos directos e iconos al **menú** Inicio, asocia los archivos adecuados y escribe entradas del Registro para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="5a5f4-133">Cuando un usuario intenta abrir una aplicación asignada, el instalador instala la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="5a5f4-134">La asignación [*y publicación son*](p-gly.md) dos métodos de [*publicidad.*](/windows)</span><span class="sxs-lookup"><span data-stu-id="5a5f4-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="5a5f4-135">Para obtener más información, vea [Anuncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="5a5f4-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a5f4-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**ejecución asincrónica**</span><span class="sxs-lookup"><span data-stu-id="5a5f4-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="5a5f4-137">[*Acción personalizada*](c-gly.md) durante la cual el instalador ejecuta subprocesos independientes de la acción personalizada y la instalación actual simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="5a5f4-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="5a5f4-138">Para obtener más información, vea [Acciones personalizadas sincrónicas y asincrónicas.](synchronous-and-asynchronous-custom-actions.md)</span><span class="sxs-lookup"><span data-stu-id="5a5f4-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 
