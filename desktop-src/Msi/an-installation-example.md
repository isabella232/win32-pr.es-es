---
description: En este ejemplo se muestra cómo crear un paquete de Windows Installer simple que instala una aplicación.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Un ejemplo de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909110"
---
# <a name="an-installation-example"></a><span data-ttu-id="eae58-103">Un ejemplo de instalación</span><span class="sxs-lookup"><span data-stu-id="eae58-103">An Installation Example</span></span>

<span data-ttu-id="eae58-104">En este ejemplo se muestra cómo crear un paquete de Windows Installer simple que instala una aplicación.</span><span class="sxs-lookup"><span data-stu-id="eae58-104">This example illustrates how to create a simple Windows Installer package that installs an application.</span></span> <span data-ttu-id="eae58-105">En el ejemplo se instala el Bloc de notas, un editor de texto incluido en Windows y varios archivos de texto que describen eventos y admisiones en el ámbito de estacionamiento rojo imaginario.</span><span class="sxs-lookup"><span data-stu-id="eae58-105">The sample installs Notepad, a text editor included with Windows, and several text files describing events and admissions at the imaginary Red Park Arena.</span></span>

<span data-ttu-id="eae58-106">El ejemplo tiene las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="eae58-106">The sample has the following specifications:</span></span>

-   <span data-ttu-id="eae58-107">La aplicación se proporciona a los usuarios como un paquete de Windows Installer de instalación automática que instala todos los archivos necesarios, accesos directos e información del registro.</span><span class="sxs-lookup"><span data-stu-id="eae58-107">The application is provided to users as a self-installing Windows Installer package that installs all the required files, shortcuts, and registry information.</span></span>
-   <span data-ttu-id="eae58-108">El paquete de instalación puede presentar al usuario un asistente para la interfaz de usuario durante la instalación para recopilar información del usuario.</span><span class="sxs-lookup"><span data-stu-id="eae58-108">The installation package may present a UI wizard to the user during setup to collect user information.</span></span>
-   <span data-ttu-id="eae58-109">Durante la instalación, los usuarios tienen la opción de seleccionar las características individuales que se instalarán para ejecutarse: localmente, en ejecutar desde el origen o en no instalarse.</span><span class="sxs-lookup"><span data-stu-id="eae58-109">During setup, users have the option of selecting individual features to be installed to run-locally, to run-from-source, or to not be installed.</span></span>
-   <span data-ttu-id="eae58-110">Una de las características se puede presentar a los usuarios como una característica de instalación a petición.</span><span class="sxs-lookup"><span data-stu-id="eae58-110">One of the features can be presented to users as an install-on-demand feature.</span></span>
-   <span data-ttu-id="eae58-111">El mismo paquete desinstala la aplicación y quita todos los archivos de aplicación y la información del registro del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="eae58-111">The same package uninstalls the application and removes all the application files and registry information from the user's computer.</span></span>
-   <span data-ttu-id="eae58-112">El paquete está preparado para recibir una actualización importante que incluye el cambio de su código de producto.</span><span class="sxs-lookup"><span data-stu-id="eae58-112">The package is prepared to receive a major upgrade that includes changing its product code.</span></span>

<span data-ttu-id="eae58-113">Para reproducir el ejemplo, necesita una herramienta de software capaz de crear y editar una base de datos Windows Installer en blanco.</span><span class="sxs-lookup"><span data-stu-id="eae58-113">To reproduce the example, you need a software tool capable of creating and editing a blank Windows Installer database.</span></span> <span data-ttu-id="eae58-114">Hay varias herramientas de creación de paquetes disponibles de fabricantes de software independientes.</span><span class="sxs-lookup"><span data-stu-id="eae58-114">Several package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="eae58-115">En los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md)se proporciona un editor de base de datos de Windows Installer denominado orca.</span><span class="sxs-lookup"><span data-stu-id="eae58-115">A Windows Installer database editor called Orca is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="eae58-116">Para completar el ejemplo, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="eae58-116">To complete the example, follow these steps:</span></span>

[<span data-ttu-id="eae58-117">Planeación de la instalación</span><span class="sxs-lookup"><span data-stu-id="eae58-117">Planning the Installation</span></span>](planning-the-installation.md)

[<span data-ttu-id="eae58-118">Importar una base de datos en blanco</span><span class="sxs-lookup"><span data-stu-id="eae58-118">Importing a Blank Database</span></span>](importing-a-blank-database.md)

[<span data-ttu-id="eae58-119">Especificar la estructura de directorios</span><span class="sxs-lookup"><span data-stu-id="eae58-119">Specifying Directory Structure</span></span>](specifying-directory-structure.md)

[<span data-ttu-id="eae58-120">Especificar componentes</span><span class="sxs-lookup"><span data-stu-id="eae58-120">Specifying Components</span></span>](specifying-components.md)

[<span data-ttu-id="eae58-121">Especificar archivos y atributos de archivo</span><span class="sxs-lookup"><span data-stu-id="eae58-121">Specifying Files and File Attributes</span></span>](specifying-files-and-file-attributes.md)

[<span data-ttu-id="eae58-122">Especificar medios de origen</span><span class="sxs-lookup"><span data-stu-id="eae58-122">Specifying Source Media</span></span>](specifying-source-media.md)

[<span data-ttu-id="eae58-123">Especificar características</span><span class="sxs-lookup"><span data-stu-id="eae58-123">Specifying Features</span></span>](specifying-features.md)

[<span data-ttu-id="eae58-124">Especificar relaciones Feature-Component</span><span class="sxs-lookup"><span data-stu-id="eae58-124">Specifying Feature-Component Relationships</span></span>](specifying-feature-component-relationships.md)

[<span data-ttu-id="eae58-125">Agregar información del registro</span><span class="sxs-lookup"><span data-stu-id="eae58-125">Adding Registry Information</span></span>](adding-registry-information.md)

[<span data-ttu-id="eae58-126">Especificar accesos directos</span><span class="sxs-lookup"><span data-stu-id="eae58-126">Specifying Shortcuts</span></span>](specifying-shortcuts.md)

[<span data-ttu-id="eae58-127">Especificar propiedades</span><span class="sxs-lookup"><span data-stu-id="eae58-127">Specifying Properties</span></span>](specifying-properties.md)

[<span data-ttu-id="eae58-128">Importación de InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="eae58-128">Importing the InstallExecuteSequence</span></span>](importing-the-installexecutesequence.md)

[<span data-ttu-id="eae58-129">Importación de InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="eae58-129">Importing the InstallUISequence</span></span>](importing-the-installuisequence.md)

[<span data-ttu-id="eae58-130">Importación de AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="eae58-130">Importing the AdminExecuteSequence</span></span>](importing-the-adminexecutesequence.md)

[<span data-ttu-id="eae58-131">Importación de AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="eae58-131">Importing the AdminUISequence</span></span>](importing-the-adminuisequence.md)

[<span data-ttu-id="eae58-132">Importación de AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="eae58-132">Importing the AdvtExecuteSequence</span></span>](importing-the-advtexecutesequence.md)

[<span data-ttu-id="eae58-133">Agregar información de Resumen</span><span class="sxs-lookup"><span data-stu-id="eae58-133">Adding Summary Information</span></span>](adding-summary-information.md)

[<span data-ttu-id="eae58-134">Importación de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="eae58-134">Importing the User Interface</span></span>](importing-the-user-interface.md)

[<span data-ttu-id="eae58-135">Validar una base de datos de instalación</span><span class="sxs-lookup"><span data-stu-id="eae58-135">Validating an Installation Database</span></span>](validating-an-installation-database.md)

 

 



