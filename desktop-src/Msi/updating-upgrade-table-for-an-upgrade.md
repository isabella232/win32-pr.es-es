---
description: Para aplicar una actualización principal mediante Windows Installer, el paquete de instalación del producto original debe especificar una propiedad UpgradeCode, descrita en preparación de una aplicación para futuras actualizaciones principales, y el paquete de actualización debe tener una tabla de actualización.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Actualizando la tabla de actualización para una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156041"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a><span data-ttu-id="e2c74-103">Actualizando la tabla de actualización para una actualización</span><span class="sxs-lookup"><span data-stu-id="e2c74-103">Updating Upgrade Table for an Upgrade</span></span>

<span data-ttu-id="e2c74-104">Para aplicar una actualización principal mediante Windows Installer, el paquete de instalación del producto original debe especificar una propiedad [**UpgradeCode**](upgradecode.md) , descrita en [preparación de una aplicación para futuras actualizaciones principales](preparing-an-application-for-future-major-upgrades.md), y el paquete de actualización debe tener una [tabla de actualización](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="e2c74-104">To apply a major upgrade using Windows Installer, the original product installation package must specify an [**UpgradeCode**](upgradecode.md) Property, described in [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md), and the upgrade package must have an [Upgrade table](upgrade-table.md).</span></span>

<span data-ttu-id="e2c74-105">Para obtener más información acerca de las actualizaciones principales, consulte [actualizaciones principales](major-upgrades.md) en [revisiones y actualizaciones](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="e2c74-105">For more information about major upgrades, see [Major Upgrades](major-upgrades.md) in [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="e2c74-106">Al paquete de instalación de MNP2000.msi se le asignó una propiedad [**UpgradeCode**](upgradecode.md) , como se describe en la sección [especificar propiedades](specifying-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e2c74-106">The installation package of MNP2000.msi was assigned an [**UpgradeCode**](upgradecode.md) property, as described in the section [Specifying Properties](specifying-properties.md).</span></span>

<span data-ttu-id="e2c74-107">Windows Installer aplica la actualización si el usuario ya ha instalado las versiones 1,0 a 1,4 (inclusivas) del idioma inglés MNP2000.</span><span class="sxs-lookup"><span data-stu-id="e2c74-107">Windows Installer applies the upgrade if the user has already installed the 1.0 to 1.4 versions (inclusive) of English language MNP2000.</span></span> <span data-ttu-id="e2c74-108">Windows Installer migra la configuración de las características del producto original al producto actualizado.</span><span class="sxs-lookup"><span data-stu-id="e2c74-108">Windows Installer migrates all of the original product's feature settings to the upgraded product.</span></span> <span data-ttu-id="e2c74-109">El instalador quita los archivos que pertenecen a los productos originales que no se usan en la actualización del producto.</span><span class="sxs-lookup"><span data-stu-id="e2c74-109">The installer removes the files belonging to the original products not being used by the product's upgrade.</span></span>

<span data-ttu-id="e2c74-110">Si su copia de MNP2001.msi no incluye una [tabla de actualización](upgrade-table.md), utilice Orca u otro editor de tablas para importar una tabla de actualización vacía en la base de datos de Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="e2c74-110">If your copy of MNP2001.msi does not include an [Upgrade table](upgrade-table.md), use Orca, or another table editor, to import an empty Upgrade table into the database from Schema.msi.</span></span> <span data-ttu-id="e2c74-111">El SDK proporciona una copia de Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="e2c74-111">The SDK provides a copy of Schema.msi.</span></span> <span data-ttu-id="e2c74-112">Utilice el editor de base de datos para abrir MNP2001.msi y escriba los datos siguientes en la tabla de actualización vacía.</span><span class="sxs-lookup"><span data-stu-id="e2c74-112">Use your database editor to open MNP2001.msi and enter the following data into the empty Upgrade table.</span></span>



| <span data-ttu-id="e2c74-113">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="e2c74-113">UpgradeCode</span></span>                            | <span data-ttu-id="e2c74-114">VersionMin</span><span class="sxs-lookup"><span data-stu-id="e2c74-114">VersionMin</span></span> | <span data-ttu-id="e2c74-115">VersionMax</span><span class="sxs-lookup"><span data-stu-id="e2c74-115">VersionMax</span></span> | <span data-ttu-id="e2c74-116">Idioma</span><span class="sxs-lookup"><span data-stu-id="e2c74-116">Language</span></span> | <span data-ttu-id="e2c74-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="e2c74-117">Attributes</span></span> | <span data-ttu-id="e2c74-118">Remove</span><span class="sxs-lookup"><span data-stu-id="e2c74-118">Remove</span></span> | <span data-ttu-id="e2c74-119">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="e2c74-119">ActionProperty</span></span> |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| <span data-ttu-id="e2c74-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="e2c74-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> | <span data-ttu-id="e2c74-121">01.00.0000</span><span class="sxs-lookup"><span data-stu-id="e2c74-121">01.00.0000</span></span> | <span data-ttu-id="e2c74-122">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="e2c74-122">01.40.0000</span></span> | <span data-ttu-id="e2c74-123">3082</span><span class="sxs-lookup"><span data-stu-id="e2c74-123">1033</span></span>     | <span data-ttu-id="e2c74-124">769</span><span class="sxs-lookup"><span data-stu-id="e2c74-124">769</span></span>        |        | <span data-ttu-id="e2c74-125">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="e2c74-125">OLDAPPFOUND</span></span>    |



 

[<span data-ttu-id="e2c74-126">Continuar</span><span class="sxs-lookup"><span data-stu-id="e2c74-126">Continue</span></span>](updating-properties-for-an-upgrade.md)

 

 



