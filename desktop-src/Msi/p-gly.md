---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156321"
---
# <a name="p-windows-installer"></a><span data-ttu-id="23bfc-103">P (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="23bfc-103">P (Windows Installer)</span></span>

<span data-ttu-id="23bfc-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [o](o-gly.md) p [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="23bfc-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="23bfc-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**configura**</span><span class="sxs-lookup"><span data-stu-id="23bfc-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="23bfc-106">[*archivo. msi*](m-gly.md) y los [*archivos de código fuente externos a los*](e-gly.md) que puede apuntar este archivo.</span><span class="sxs-lookup"><span data-stu-id="23bfc-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="23bfc-107">Por lo tanto, un paquete contiene toda la información que necesita el Windows Installer para ejecutar la interfaz de usuario y para instalar o desinstalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23bfc-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="23bfc-108">Para obtener más información, consulte también [*base de datos del instalador*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="23bfc-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="23bfc-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**código de paquete**</span><span class="sxs-lookup"><span data-stu-id="23bfc-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="23bfc-110">GUID que identifica un paquete determinado.</span><span class="sxs-lookup"><span data-stu-id="23bfc-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="23bfc-111">Se requiere un código de paquete único porque algunas transformaciones o paquetes de revisión se pueden aplicar a más de una aplicación o puede actualizar una aplicación a otra aplicación o versión.</span><span class="sxs-lookup"><span data-stu-id="23bfc-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="23bfc-112">Para obtener más información, consulte [códigos de paquete](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="23bfc-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="23bfc-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**revisiones**</span><span class="sxs-lookup"><span data-stu-id="23bfc-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="23bfc-114">Método de actualización de un archivo que reemplaza solo los bits que se están cambiando, en lugar de todo el archivo.</span><span class="sxs-lookup"><span data-stu-id="23bfc-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="23bfc-115">Esto significa que los usuarios pueden descargar una revisión de actualización para un producto que sea mucho más pequeño que todo el producto.</span><span class="sxs-lookup"><span data-stu-id="23bfc-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="23bfc-116">Para obtener más información, vea [patch Packages](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="23bfc-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="23bfc-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**archivo de revisión**</span><span class="sxs-lookup"><span data-stu-id="23bfc-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="23bfc-118">[Paquete P atch](patch-packages.md) usado para la revisión.</span><span class="sxs-lookup"><span data-stu-id="23bfc-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="23bfc-119">Para obtener más información, consulte [revisiones y actualizaciones](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="23bfc-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="23bfc-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modo de vista previa**</span><span class="sxs-lookup"><span data-stu-id="23bfc-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="23bfc-121">Modo para ver el diseño de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="23bfc-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="23bfc-122">Para obtener más información, vea obtener [una vista previa de la interfaz de usuario](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="23bfc-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="23bfc-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barra de progreso**</span><span class="sxs-lookup"><span data-stu-id="23bfc-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="23bfc-124">Controlar el instalador se puede mostrar durante el tiempo de ejecución del script que representa el progreso de la instalación.</span><span class="sxs-lookup"><span data-stu-id="23bfc-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="23bfc-125">Para obtener más información, vea [crear un control ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="23bfc-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="23bfc-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**propiedad**</span><span class="sxs-lookup"><span data-stu-id="23bfc-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="23bfc-127">Variables globales utilizadas durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="23bfc-127">Global variables used during an installation.</span></span> <span data-ttu-id="23bfc-128">(Consulte [acerca de las propiedades](about-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="23bfc-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="23bfc-129">El término "propiedad" también hace referencia a un atributo de un objeto de automatización.</span><span class="sxs-lookup"><span data-stu-id="23bfc-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="23bfc-130">(Consulte [interfaz de automatización](automation-interface.md)).</span><span class="sxs-lookup"><span data-stu-id="23bfc-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="23bfc-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**edición**</span><span class="sxs-lookup"><span data-stu-id="23bfc-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="23bfc-132">Método de [*publicidad*](a-gly.md) de una característica o aplicación.</span><span class="sxs-lookup"><span data-stu-id="23bfc-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="23bfc-133">La publicación no rellena la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="23bfc-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="23bfc-134">Sin embargo, si otra aplicación intenta abrir una aplicación publicada, hay suficiente información en el instalador para asignar la aplicación publicada.</span><span class="sxs-lookup"><span data-stu-id="23bfc-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="23bfc-135">Para obtener más información, vea [*asignar*](a-gly.md) componentes y [características](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="23bfc-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 



