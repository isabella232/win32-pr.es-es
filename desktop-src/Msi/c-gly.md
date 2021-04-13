---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1970c8e9063657701183c91ff337d06d169914fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276513"
---
# <a name="c-windows-installer"></a><span data-ttu-id="b39a7-103">C (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="b39a7-103">C (Windows Installer)</span></span>

<span data-ttu-id="b39a7-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [o](o-gly.md) [p](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="b39a7-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b39a7-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**archivo. cab**</span><span class="sxs-lookup"><span data-stu-id="b39a7-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="b39a7-106">Archivo único, normalmente con una extensión. cab, que almacena archivos comprimidos en una biblioteca de archivos.</span><span class="sxs-lookup"><span data-stu-id="b39a7-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="b39a7-107">El formato de archivo. cab es una manera eficaz de empaquetar varios archivos, ya que la compresión se realiza a través de los límites del archivo, lo que mejora significativamente la relación de compresión.</span><span class="sxs-lookup"><span data-stu-id="b39a7-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="b39a7-108">Para obtener información sobre la creación de archivadores, consulte [archivos. cab](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="b39a7-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="b39a7-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**MD5**</span><span class="sxs-lookup"><span data-stu-id="b39a7-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="b39a7-110">Valor calculado que depende del contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="b39a7-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="b39a7-111">Se almacena con datos para detectar daños en los archivos.</span><span class="sxs-lookup"><span data-stu-id="b39a7-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="b39a7-112">El sistema comprueba este valor para asegurarse de que los datos no estén dañados.</span><span class="sxs-lookup"><span data-stu-id="b39a7-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="b39a7-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**pone**</span><span class="sxs-lookup"><span data-stu-id="b39a7-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="b39a7-114">Parte más pequeña de una instalación controlada por el instalador, también un bloque de creación de una aplicación o característica desde la perspectiva del programador.</span><span class="sxs-lookup"><span data-stu-id="b39a7-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="b39a7-115">Algunos ejemplos de componentes son un grupo de archivos relacionados, un objeto COM o una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b39a7-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="b39a7-116">Para obtener más información, vea [componentes y características](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="b39a7-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="b39a7-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**confirmar bases de datos**</span><span class="sxs-lookup"><span data-stu-id="b39a7-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="b39a7-118">Cambios acumulados realizados en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="b39a7-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="b39a7-119">Los cambios no se reflejan en la base de datos real hasta que se confirma la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b39a7-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="b39a7-120">Para obtener más información, consulte [confirmación de bases](committing-databases.md)de datos.</span><span class="sxs-lookup"><span data-stu-id="b39a7-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="b39a7-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent,**</span><span class="sxs-lookup"><span data-stu-id="b39a7-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="b39a7-122">Aspecto de la funcionalidad de la interfaz de usuario del instalador.</span><span class="sxs-lookup"><span data-stu-id="b39a7-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="b39a7-123">Un ControlEvent, típico desencadena alguna acción por parte del instalador al activar un control de cuadro de diálogo u otro evento.</span><span class="sxs-lookup"><span data-stu-id="b39a7-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="b39a7-124">Para obtener más información, consulte [información general de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b39a7-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="b39a7-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costos**</span><span class="sxs-lookup"><span data-stu-id="b39a7-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="b39a7-126">Método utilizado por el instalador para determinar los requisitos de espacio en disco para la instalación.</span><span class="sxs-lookup"><span data-stu-id="b39a7-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="b39a7-127">El costo tiene en cuenta factores como, por ejemplo, si es necesario sobrescribir los archivos existentes.</span><span class="sxs-lookup"><span data-stu-id="b39a7-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="b39a7-128">Para obtener más información, consulte [costo de archivos](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="b39a7-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="b39a7-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**archivo. Cub**</span><span class="sxs-lookup"><span data-stu-id="b39a7-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="b39a7-130">Módulo de validación que almacena y proporciona acceso a las acciones personalizadas de ICE.</span><span class="sxs-lookup"><span data-stu-id="b39a7-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="b39a7-131">Para obtener más información, consulte [sample. Cub File](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="b39a7-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="b39a7-132">Para obtener más información, consulte también [Windows Installer extensiones de archivo](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b39a7-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="b39a7-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**acción personalizada**</span><span class="sxs-lookup"><span data-stu-id="b39a7-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="b39a7-134">Escrito por el autor del [*paquete*](p-gly.md) , pero no integrado en el instalador como una acción estándar.</span><span class="sxs-lookup"><span data-stu-id="b39a7-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="b39a7-135">Para obtener más información, vea [acciones personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="b39a7-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 



