---
description: La acción FindRelatedProducts se ejecuta a través de cada registro de la tabla de actualización en secuencia y compara el código de actualización, la versión del producto y el idioma de cada fila con los productos instalados en el sistema.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Acción FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361032"
---
# <a name="findrelatedproducts-action"></a><span data-ttu-id="4e871-103">Acción FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="4e871-103">FindRelatedProducts Action</span></span>

<span data-ttu-id="4e871-104">La acción FindRelatedProducts se ejecuta a través de cada registro de la [tabla de actualización](upgrade-table.md) en secuencia y compara el código de actualización, la versión del producto y el idioma de cada fila con los productos instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4e871-104">The FindRelatedProducts action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to products installed on the system.</span></span> <span data-ttu-id="4e871-105">Cuando FindRelatedProducts detecta una correspondencia entre la información de actualización y un producto instalado, anexa el código de producto a la propiedad especificada en la columna ActionProperty de UpgradeTable.</span><span class="sxs-lookup"><span data-stu-id="4e871-105">When FindRelatedProducts detects a correspondence between the upgrade information and an installed product, it appends the product code to the property specified in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="4e871-106">La acción FindRelatedProducts solo se ejecuta la primera vez que se instala el producto.</span><span class="sxs-lookup"><span data-stu-id="4e871-106">The FindRelatedProducts action only runs the first time the product is installed.</span></span> <span data-ttu-id="4e871-107">La acción FindRelatedProducts no se ejecuta durante el modo de mantenimiento o la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="4e871-107">The FindRelatedProducts action does not run during maintenance mode or uninstallation.</span></span>

## <a name="database-tables-queried"></a><span data-ttu-id="4e871-108">Tablas de base de datos consultadas</span><span class="sxs-lookup"><span data-stu-id="4e871-108">Database Tables Queried</span></span>

<span data-ttu-id="4e871-109">Esta acción consulta la siguiente tabla:</span><span class="sxs-lookup"><span data-stu-id="4e871-109">This action queries the following table:</span></span>

[<span data-ttu-id="4e871-110">Actualizar tabla</span><span class="sxs-lookup"><span data-stu-id="4e871-110">Upgrade Table</span></span>](upgrade-table.md)

## <a name="properties-used"></a><span data-ttu-id="4e871-111">Propiedades usadas</span><span class="sxs-lookup"><span data-stu-id="4e871-111">Properties Used</span></span>

<span data-ttu-id="4e871-112">La acción FindRelatedProducts usa la propiedad [**UpgradeCode**](upgradecode.md) y la información de versión e idioma que se creó en la tabla de actualización para detectar los productos instalados afectados por la actualización pendiente.</span><span class="sxs-lookup"><span data-stu-id="4e871-112">The FindRelatedProducts action uses the [**UpgradeCode**](upgradecode.md) property and the version and language information authored into the Upgrade table to detect installed products affected by the pending upgrade.</span></span> <span data-ttu-id="4e871-113">Anexa el código de producto de los productos detectados a la propiedad en la columna ActionProperty de UpgradeTable.</span><span class="sxs-lookup"><span data-stu-id="4e871-113">It appends the product code of detected products to the property in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="4e871-114">FindRelatedProducts solo reconoce los productos existentes que se han instalado con el Windows Installer con un archivo. msi que define una propiedad [**UpgradeCode**](upgradecode.md) , una propiedad [**ProductVersion**](productversion.md) y un valor para la propiedad [**ProductLanguage**](productlanguage.md) que es uno de los idiomas enumerados en la propiedad Resumen de la [**plantilla**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="4e871-114">FindRelatedProducts only recognizes existing products that have been installed using the Windows Installer with an .msi that defines an [**UpgradeCode**](upgradecode.md) property, a [**ProductVersion**](productversion.md) property, and a value for the [**ProductLanguage**](productlanguage.md) property that is one of the languages listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="4e871-115">Tenga en cuenta que FindRelatedProducts usa el lenguaje devuelto por [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span><span class="sxs-lookup"><span data-stu-id="4e871-115">Note that FindRelatedProducts uses the language returned by [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span></span> <span data-ttu-id="4e871-116">Para que FindRelatedProducts funcione correctamente, el autor del paquete debe asegurarse de que la propiedad [**ProductLanguage**](productlanguage.md) de la [tabla de propiedades](property-table.md) esté establecida en un idioma que también aparezca en la propiedad Resumen de la [**plantilla**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="4e871-116">For FindRelatedProducts to work correctly, the package author must be sure that the [**ProductLanguage**](productlanguage.md) property in the [Property table](property-table.md) is set to a language that is also listed in the [**Template Summary**](template-summary.md) Property.</span></span> <span data-ttu-id="4e871-117">Consulte [preparación de una aplicación para futuras actualizaciones importantes](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="4e871-117">See [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4e871-118">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="4e871-118">Sequence Restrictions</span></span>

<span data-ttu-id="4e871-119">FindRelatedProducts debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en las tablas [InstallExecuteSequence](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4e871-119">FindRelatedProducts should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence](installexecutesequence-table.md) tables.</span></span> <span data-ttu-id="4e871-120">El instalador impide que los productos de FindRelated se ejecuten en InstallExecuteSequence si la acción ya se ejecutó en InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="4e871-120">The installer prevents FindRelated Products from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span> <span data-ttu-id="4e871-121">La acción FindRelatedProducts debe ser anterior a la [acción MigrateFeatureStates](migratefeaturestates-action.md) y la [acción RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="4e871-121">The FindRelatedProducts action must come before the [MigrateFeatureStates action](migratefeaturestates-action.md) and the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4e871-122">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="4e871-122">ActionData Messages</span></span>

<span data-ttu-id="4e871-123">FindRelatedProducts envía un mensaje de datos de acción para cada producto relacionado que detecta en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4e871-123">FindRelatedProducts sends an action data message for each related product it detects on the system.</span></span>

 

 



