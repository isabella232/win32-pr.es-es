---
description: Además de la información descrita en las secciones anteriores, uisample.msi también contiene datos para una interfaz de usuario de ejemplo.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importación de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908185"
---
# <a name="importing-the-user-interface"></a><span data-ttu-id="c4679-103">Importación de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c4679-103">Importing the User Interface</span></span>

<span data-ttu-id="c4679-104">Además de la información descrita en las secciones anteriores, uisample.msi también contiene datos para una interfaz de usuario de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c4679-104">In addition to information discussed in previous sections, uisample.msi also contains data for a sample user interface.</span></span> <span data-ttu-id="c4679-105">Si combinó uisample.msi en MNP2000.msi en la sección [importar una base de datos en blanco](importing-a-blank-database.md), esta información también se encuentra en MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="c4679-105">If you merged uisample.msi into MNP2000.msi in the section [Importing a Blank Database](importing-a-blank-database.md), then this information is present in MNP2000.msi as well.</span></span> <span data-ttu-id="c4679-106">La información de la interfaz de usuario de ejemplo se encuentra en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c4679-106">The information for the sample user interface is in the following tables.</span></span>

-   [<span data-ttu-id="c4679-107">Tabla de ActionText</span><span class="sxs-lookup"><span data-stu-id="c4679-107">ActionText table</span></span>](actiontext-table.md)
-   [<span data-ttu-id="c4679-108">Tabla binaria</span><span class="sxs-lookup"><span data-stu-id="c4679-108">Binary table</span></span>](binary-table.md)
-   [<span data-ttu-id="c4679-109">Tabla de control</span><span class="sxs-lookup"><span data-stu-id="c4679-109">Control table</span></span>](control-table.md)
-   [<span data-ttu-id="c4679-110">Tabla ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="c4679-110">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="c4679-111">Tabla de cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="c4679-111">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="c4679-112">Tabla de errores</span><span class="sxs-lookup"><span data-stu-id="c4679-112">Error table</span></span>](error-table.md)
-   [<span data-ttu-id="c4679-113">Tabla EventMapping</span><span class="sxs-lookup"><span data-stu-id="c4679-113">EventMapping table</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="c4679-114">Tabla RadioButton</span><span class="sxs-lookup"><span data-stu-id="c4679-114">RadioButton table</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="c4679-115">Tabla de TextStyle</span><span class="sxs-lookup"><span data-stu-id="c4679-115">TextStyle table</span></span>](textstyle-table.md)
-   [<span data-ttu-id="c4679-116">Tabla UIText</span><span class="sxs-lookup"><span data-stu-id="c4679-116">UIText table</span></span>](uitext-table.md)

<span data-ttu-id="c4679-117">El editor de bases de datos Orca proporcionado con el instalador incluye una opción de vista previa del cuadro de diálogo que puede usar para obtener una vista previa de los cuadros de diálogo de la interfaz de usuario especificados por los datos de las tablas anteriores.</span><span class="sxs-lookup"><span data-stu-id="c4679-117">The database editor Orca provided with the installer includes a dialog preview option that you can use to preview the dialogs of the user interface that is specified by the data in the above tables.</span></span>

<span data-ttu-id="c4679-118">El paquete de instalación de ejemplo MNP2000.msi ya está listo para la validación del paquete.</span><span class="sxs-lookup"><span data-stu-id="c4679-118">The sample installation package MNP2000.msi is now ready for package validation.</span></span> <span data-ttu-id="c4679-119">Ejecute siempre la validación en un nuevo paquete antes de intentar instalar el paquete por primera vez.</span><span class="sxs-lookup"><span data-stu-id="c4679-119">Always run validation on a new package before attempting to install the package for the first time.</span></span> <span data-ttu-id="c4679-120">Esto se explica en validación del ejemplo de instalación.</span><span class="sxs-lookup"><span data-stu-id="c4679-120">This is discussed in Validating the Installation Sample.</span></span>

<span data-ttu-id="c4679-121">Si no desea incluir la interfaz de usuario en el paquete de ejemplo, omita o quite toda la información de las tablas mostradas anteriormente, excepto la [tabla de TextStyle](textstyle-table.md) (que es necesaria para definir la propiedad [**DefaultUIFont**](defaultuifont.md) ).</span><span class="sxs-lookup"><span data-stu-id="c4679-121">If you do not want to include the user interface in the sample package, omit or remove the all information in the tables shown above except for the [TextStyle table](textstyle-table.md) (which is needed to define the [**DefaultUIFont**](defaultuifont.md) property).</span></span> <span data-ttu-id="c4679-122">También debe quitar las propiedades de la interfaz de usuario de la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4679-122">You should also remove user interface properties from the [Property Table](property-table.md).</span></span> <span data-ttu-id="c4679-123">A continuación se muestra una tabla de propiedades de ejemplo para el ejemplo del Bloc de notas, sin una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c4679-123">An example Property table for the Notepad sample, without a UI, is shown below.</span></span> <span data-ttu-id="c4679-124">No reutilice los GUID que se muestran en la tabla si copia este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c4679-124">Do not reuse the GUIDs shown in the table if you copy this example.</span></span>

[<span data-ttu-id="c4679-125">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="c4679-125">Property Table</span></span>](property-table.md)



| <span data-ttu-id="c4679-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c4679-126">Property</span></span>                                   | <span data-ttu-id="c4679-127">Value</span><span class="sxs-lookup"><span data-stu-id="c4679-127">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="c4679-128">**DefaultUIFont**</span><span class="sxs-lookup"><span data-stu-id="c4679-128">**DefaultUIFont**</span></span>](defaultuifont.md)     | <span data-ttu-id="c4679-129">DlgFont8</span><span class="sxs-lookup"><span data-stu-id="c4679-129">DlgFont8</span></span>                               |
| [<span data-ttu-id="c4679-130">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="c4679-130">**INSTALLLEVEL**</span></span>](installlevel.md)       | <span data-ttu-id="c4679-131">3</span><span class="sxs-lookup"><span data-stu-id="c4679-131">3</span></span>                                      |
| [<span data-ttu-id="c4679-132">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="c4679-132">**LIMITUI**</span></span>](limitui.md)                 | <span data-ttu-id="c4679-133">1</span><span class="sxs-lookup"><span data-stu-id="c4679-133">1</span></span>                                      |
| [<span data-ttu-id="c4679-134">**Le**</span><span class="sxs-lookup"><span data-stu-id="c4679-134">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="c4679-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4679-135">Microsoft</span></span>                              |
| [<span data-ttu-id="c4679-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="c4679-136">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="c4679-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="c4679-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> |
| [<span data-ttu-id="c4679-138">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="c4679-138">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="c4679-139">3082</span><span class="sxs-lookup"><span data-stu-id="c4679-139">1033</span></span>                                   |
| [<span data-ttu-id="c4679-140">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="c4679-140">**ProductName**</span></span>](productname.md)         | <span data-ttu-id="c4679-141">MNP2000</span><span class="sxs-lookup"><span data-stu-id="c4679-141">MNP2000</span></span>                                |
| [<span data-ttu-id="c4679-142">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="c4679-142">**ProductVersion**</span></span>](productversion.md)   | <span data-ttu-id="c4679-143">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="c4679-143">01.40.0000</span></span>                             |
| [<span data-ttu-id="c4679-144">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="c4679-144">**UpgradeCode**</span></span>](upgradecode.md)         | <span data-ttu-id="c4679-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="c4679-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> |



 

<span data-ttu-id="c4679-146">Un paquete sin interfaz de usuario se puede instalar desde la línea de comandos o desde un programa.</span><span class="sxs-lookup"><span data-stu-id="c4679-146">A package without a user interface can be installed from the command line or from a program.</span></span> <span data-ttu-id="c4679-147">Para instalar un paquete desde la línea de comandos, use los métodos descritos en opciones de la [línea de comandos](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="c4679-147">To install a package from the command line use the methods described in [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="c4679-148">Para instalar un paquete desde un programa, use los métodos descritos en [uso de las funciones del instalador](using-installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c4679-148">To install a package from a program use the methods described in [Using Installer Functions](using-installer-functions.md).</span></span> <span data-ttu-id="c4679-149">Ejecute siempre la validación en un nuevo paquete antes de intentar instalar un nuevo paquete por primera vez.</span><span class="sxs-lookup"><span data-stu-id="c4679-149">Always run validation on a new package before attempting to install a new package for the first time.</span></span>

[<span data-ttu-id="c4679-150">Continuar</span><span class="sxs-lookup"><span data-stu-id="c4679-150">Continue</span></span>](validating-an-installation-database.md)

 

 



