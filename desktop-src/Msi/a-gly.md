---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46677d8823c5298307db922f2d61285564add437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156360"
---
# <a name="a-windows-installer"></a><span data-ttu-id="69c26-103">A (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="69c26-103">A (Windows Installer)</span></span>

<span data-ttu-id="69c26-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [o](o-gly.md) [p](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="69c26-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="69c26-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Consejos**</span><span class="sxs-lookup"><span data-stu-id="69c26-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="69c26-106">Diseñar la implementación para que la interfaz de usuario del instalador sea accesible para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="69c26-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="69c26-107">Para obtener más información sobre la accesibilidad, vea el tema de información general: [accesibilidad](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="69c26-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase de adquisición**</span><span class="sxs-lookup"><span data-stu-id="69c26-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="69c26-109">Fase de instalación durante la cual el instalador determina el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="69c26-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="69c26-110">La fase de adquisición comienza cuando una aplicación o un usuario indica [*Windows Installer*](m-gly.md) para instalar una aplicación o una característica.</span><span class="sxs-lookup"><span data-stu-id="69c26-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="69c26-111">A continuación, el instalador consulta la [*base*](i-gly.md) de datos para obtener información, ya que genera el [*script de ejecución*](e-gly.md) para la instalación.</span><span class="sxs-lookup"><span data-stu-id="69c26-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="69c26-112">Para obtener más información acerca de las fases de una instalación, vea [mecanismo de instalación](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="69c26-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**actuar**</span><span class="sxs-lookup"><span data-stu-id="69c26-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="69c26-114">Muchas de las funciones realizadas por Windows Installer se encapsulan en acciones.</span><span class="sxs-lookup"><span data-stu-id="69c26-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="69c26-115">Cada acción especifica la ejecución de una función determinada y el flujo total de procedimientos de la instalación viene determinado por la secuencia de acciones de las [*tablas de secuencia*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="69c26-116">[*Las acciones estándar*](s-gly.md) están integradas en Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="69c26-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="69c26-117">El autor del [*paquete*](p-gly.md)de instalación escribe las [*acciones personalizadas*](c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="69c26-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="69c26-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modo de aprobación de administrador**</span><span class="sxs-lookup"><span data-stu-id="69c26-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="69c26-119">El estado de aprobación habilitado por la protección de cuentas de usuario (UAC) que ejecuta todos los usuarios con privilegios mínimos, incluidos los administradores.</span><span class="sxs-lookup"><span data-stu-id="69c26-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="69c26-120">Los usuarios deben dar su consentimiento para elevar las instalaciones que requieran privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="69c26-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="69c26-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Anunciar**</span><span class="sxs-lookup"><span data-stu-id="69c26-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="69c26-122">Capacidad de hacer que las interfaces sean necesarias para cargar y hacer que una aplicación esté disponible sin necesidad de instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69c26-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="69c26-123">Cuando un usuario o una aplicación activa una interfaz anunciada, el instalador continúa con la instalación de los componentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="69c26-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="69c26-124">Los dos tipos de publicidad son la [*asignación*](/windows) y [*publicación*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="69c26-125">Para obtener más información, consulte también [*instalación a petición*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="69c26-126">Para obtener más información acerca de cómo el instalador anuncia las aplicaciones, consulte el [anuncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="69c26-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Servicio de información de la aplicación (AIS)**</span><span class="sxs-lookup"><span data-stu-id="69c26-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="69c26-128">Servicio de sistema de Windows Vista que facilita el inicio de las instalaciones que requieren privilegios elevados para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="69c26-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="69c26-129">Proporciona la interfaz de usuario de consentimiento utilizada por el control de cuentas de usuario para solicitar a un usuario autorización de administrador.</span><span class="sxs-lookup"><span data-stu-id="69c26-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="69c26-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**asignar**</span><span class="sxs-lookup"><span data-stu-id="69c26-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="69c26-131">Hace que una aplicación esté disponible y hace que parezca que se ha instalado para un usuario, sin instalarla realmente.</span><span class="sxs-lookup"><span data-stu-id="69c26-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="69c26-132">La asignación agrega accesos directos e iconos al menú **Inicio** , asocia los archivos adecuados y escribe entradas del registro para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69c26-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="69c26-133">Cuando un usuario intenta abrir una aplicación asignada, el instalador instala la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69c26-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="69c26-134">La asignación y [*publicación*](p-gly.md) son dos métodos de [*publicidad*](/windows).</span><span class="sxs-lookup"><span data-stu-id="69c26-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="69c26-135">Para obtener más información, vea el [anuncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="69c26-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**ejecución asincrónica**</span><span class="sxs-lookup"><span data-stu-id="69c26-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="69c26-137">[*Acción personalizada*](c-gly.md) durante la cual el instalador ejecuta subprocesos independientes de la acción personalizada y la instalación actual simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="69c26-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="69c26-138">Para obtener más información, vea [acciones personalizadas sincrónicas y asincrónicas](synchronous-and-asynchronous-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 
