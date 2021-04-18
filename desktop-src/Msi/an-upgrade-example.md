---
description: En las secciones siguientes se muestra un ejemplo de la creación de un paquete de actualización para la aplicación que se describe en un ejemplo de instalación.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Un ejemplo de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667045"
---
# <a name="an-upgrade-example"></a><span data-ttu-id="054f4-103">Un ejemplo de actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-103">An Upgrade Example</span></span>

<span data-ttu-id="054f4-104">En las secciones siguientes se muestra un ejemplo de la creación de un paquete de actualización para la aplicación que se describe en [un ejemplo de instalación](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="054f4-104">The following sections present an example of authoring an upgrade package for the application described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="054f4-105">Un ejemplo de una interfaz de usuario mínima para este ejemplo se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md) como Uisample.msi de archivos.</span><span class="sxs-lookup"><span data-stu-id="054f4-105">An example of a minimal user interface for this sample is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) as the file Uisample.msi.</span></span> <span data-ttu-id="054f4-106">Si tiene el SDK de, tendrá acceso a todas las herramientas y los datos necesarios para reproducir el paquete de instalación de ejemplo, la interfaz de usuario y el paquete de actualización de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="054f4-106">If you have the SDK, you have access to all the tools and data necessary to reproduce the sample installation package, user interface, and sample upgrade package.</span></span>

<span data-ttu-id="054f4-107">En este ejemplo se muestra cómo crear un paquete de Windows Installer que actualiza el MNP2000 de producto hipotético a un nuevo producto denominado MNP2001.</span><span class="sxs-lookup"><span data-stu-id="054f4-107">This example illustrates how to create a Windows Installer package that upgrades the hypothetical product MNP2000 to a new product called MNP2001.</span></span> <span data-ttu-id="054f4-108">El paquete de actualización de ejemplo aplica una actualización principal al producto que requiere cambiar el código de producto.</span><span class="sxs-lookup"><span data-stu-id="054f4-108">The example upgrade package applies a major upgrade to the product which requires changing the product code.</span></span> <span data-ttu-id="054f4-109">Para obtener más información acerca de las actualizaciones principales, consulte el tema sobre las [actualizaciones principales](major-upgrades.md) en la sección [revisiones y actualizaciones](patching-and-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="054f4-109">For more information about major upgrades, see the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section.</span></span>

<span data-ttu-id="054f4-110">El paquete de actualización de ejemplo tiene las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="054f4-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="054f4-111">Para calificar la recepción de esta actualización a MNP2001, un usuario debe haber instalado previamente las versiones 1,0 a 1,4 (incluido) del idioma inglés MNP2000 mediante Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="054f4-111">To qualify to receive this upgrade to MNP2001, a user must have previously installed the 1.0 to 1.4 (inclusive) versions of English language MNP2000 using Windows Installer.</span></span>
-   <span data-ttu-id="054f4-112">Cuando un usuario intenta instalar el paquete de actualización, la funcionalidad de actualización de Windows Installer busca en el equipo del usuario los productos que son aptos para la actualización.</span><span class="sxs-lookup"><span data-stu-id="054f4-112">When a user attempts to install the upgrade package, the upgrade functionality of Windows Installer searches the user's computer for any products that qualify for the upgrade.</span></span>
-   <span data-ttu-id="054f4-113">Windows Installer migra la configuración de las características del producto original al producto actualizado.</span><span class="sxs-lookup"><span data-stu-id="054f4-113">Windows Installer migrates all the of the original product's feature settings to the upgraded product.</span></span>
-   <span data-ttu-id="054f4-114">El instalador quita todas las características obsoletas del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="054f4-114">The installer removes all obsolete features from the user's computer.</span></span>
-   <span data-ttu-id="054f4-115">El instalador instala todas las características nuevas que pertenecen a la actualización.</span><span class="sxs-lookup"><span data-stu-id="054f4-115">The installer installs all new features belonging to the upgrade.</span></span>
-   <span data-ttu-id="054f4-116">Una desinstalación del paquete de actualización quita el producto del equipo del usuario y no restaura la versión anterior del producto.</span><span class="sxs-lookup"><span data-stu-id="054f4-116">An uninstall of the upgrade package removes the product from the user's computer, and does not restore the earlier version of the product.</span></span>
-   <span data-ttu-id="054f4-117">En el ejemplo se actualizan los accesos directos a nuevos archivos y características.</span><span class="sxs-lookup"><span data-stu-id="054f4-117">The sample upgrade updates shortcuts to new files and features.</span></span>

    [<span data-ttu-id="054f4-118">Planeación de una actualización importante</span><span class="sxs-lookup"><span data-stu-id="054f4-118">Planning a Major Upgrade</span></span>](planning-a-major-upgrade.md)

    [<span data-ttu-id="054f4-119">Importar la base de datos de instalación original</span><span class="sxs-lookup"><span data-stu-id="054f4-119">Importing Original Installation Database</span></span>](importing-original-installation-database.md)

    [<span data-ttu-id="054f4-120">Actualización de la estructura de directorios para una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-120">Updating Directory Structure for an Upgrade</span></span>](updating-directory-structure-for-an-upgrade.md)

    [<span data-ttu-id="054f4-121">Actualizar archivos y atributos de archivo para una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-121">Updating Files and File Attributes for an Upgrade</span></span>](updating-files-and-file-attributes-for-an-upgrade.md)

    [<span data-ttu-id="054f4-122">Actualización de componentes para una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-122">Updating Components for an Upgrade</span></span>](updating-components-for-an-upgrade.md)

    [<span data-ttu-id="054f4-123">Actualizar características para una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-123">Updating Features for an Upgrade</span></span>](updating-features-for-an-upgrade.md)

    [<span data-ttu-id="054f4-124">Actualización de accesos directos para una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-124">Updating Shortcuts for an Upgrade</span></span>](updating-shortcuts-for-an-upgrade.md)

    [<span data-ttu-id="054f4-125">Actualizando la tabla de actualización para una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-125">Updating Upgrade Table for an Upgrade</span></span>](updating-upgrade-table-for-an-upgrade.md)

    [<span data-ttu-id="054f4-126">Actualizar las propiedades de una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-126">Updating Properties for an Upgrade</span></span>](updating-properties-for-an-upgrade.md)

    [<span data-ttu-id="054f4-127">Actualización de tablas de secuencia para una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-127">Updating Sequence Tables for an Upgrade</span></span>](updating-sequence-tables-for-an-upgrade.md)

    [<span data-ttu-id="054f4-128">Actualización de la información de Resumen de una actualización</span><span class="sxs-lookup"><span data-stu-id="054f4-128">Updating Summary Information for an Upgrade</span></span>](updating-summary-information-for-an-upgrade.md)

    [<span data-ttu-id="054f4-129">Validar una actualización de instalación</span><span class="sxs-lookup"><span data-stu-id="054f4-129">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)

 

 



