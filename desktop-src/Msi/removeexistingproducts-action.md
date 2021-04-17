---
description: La acción RemoveExistingProducts recorre los códigos de producto que se muestran en la columna ActionProperty de la tabla de actualización y quita los productos en secuencia mediante la invocación de instalaciones simultáneas.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Acción RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667470"
---
# <a name="removeexistingproducts-action"></a><span data-ttu-id="280b5-103">Acción RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="280b5-103">RemoveExistingProducts Action</span></span>

<span data-ttu-id="280b5-104">La acción RemoveExistingProducts recorre los códigos de producto que se muestran en la columna ActionProperty de la [tabla de actualización](upgrade-table.md) y quita los productos en secuencia mediante la invocación de instalaciones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="280b5-104">The RemoveExistingProducts action goes through the product codes listed in the ActionProperty column of the [Upgrade table](upgrade-table.md) and removes the products in sequence by invoking concurrent installations.</span></span> <span data-ttu-id="280b5-105">Para cada instalación simultánea, el instalador establece la propiedad [**ProductCode**](productcode.md) en el código de producto y establece la propiedad [**Remove**](remove.md) en el valor del campo Remove de la tabla de actualización.</span><span class="sxs-lookup"><span data-stu-id="280b5-105">For each concurrent installation the installer sets the [**ProductCode**](productcode.md) property to the product code and sets the [**REMOVE**](remove.md) property to the value in the Remove field of the Upgrade table.</span></span> <span data-ttu-id="280b5-106">Si el campo quitar está en blanco, su valor predeterminado es todos y el instalador quita todo el producto.</span><span class="sxs-lookup"><span data-stu-id="280b5-106">If the Remove field is blank, its value defaults to ALL and the installer removes the entire product.</span></span>

<span data-ttu-id="280b5-107">El instalador solo ejecuta la acción RemoveExistingProducts la primera vez que instala un producto.</span><span class="sxs-lookup"><span data-stu-id="280b5-107">The installer only runs the RemoveExistingProducts action the first time it installs a product.</span></span> <span data-ttu-id="280b5-108">No ejecuta la acción durante una instalación o desinstalación de [mantenimiento](maintenance-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="280b5-108">It does not run the action during a [maintenance installation](maintenance-installation.md) or uninstallation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="280b5-109">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="280b5-109">Sequence Restrictions</span></span>

<span data-ttu-id="280b5-110">La acción RemoveExistingProducts se debe programar en la secuencia de acciones en una de las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="280b5-110">The RemoveExistingProducts action must be scheduled in the action sequence in one of the following locations.</span></span>

-   <span data-ttu-id="280b5-111">Entre la [acción InstallValidate](installvalidate-action.md) y la [acción InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="280b5-111">Between the [InstallValidate action](installvalidate-action.md) and the [InstallInitialize action](installinitialize-action.md).</span></span> <span data-ttu-id="280b5-112">En este caso, el instalador quita las aplicaciones antiguas completamente antes de instalar las nuevas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="280b5-112">In this case, the installer removes the old applications entirely before installing the new applications.</span></span> <span data-ttu-id="280b5-113">Se trata de una ubicación ineficaz para la acción, ya que todos los archivos reutilizados deben volver a copiarse.</span><span class="sxs-lookup"><span data-stu-id="280b5-113">This is an inefficient placement for the action because all reused files have to be recopied.</span></span>
-   <span data-ttu-id="280b5-114">Después de la [acción InstallInitialize](installinitialize-action.md) y antes de cualquier acción que genere el script de ejecución.</span><span class="sxs-lookup"><span data-stu-id="280b5-114">After the [InstallInitialize action](installinitialize-action.md) and before any actions that generate execution script.</span></span>
-   <span data-ttu-id="280b5-115">Entre la [acción InstallExecute](installexecute-action.md), la [acción InstallExecuteAgain](installexecuteagain-action.md)y la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="280b5-115">Between the [InstallExecute action](installexecute-action.md), or the [InstallExecuteAgain action](installexecuteagain-action.md), and the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="280b5-116">Por lo general, las tres últimas acciones se programan justo después de otra: InstallExecute, RemoveExistingProducts y InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="280b5-116">Generally the last three actions are scheduled right after one another: InstallExecute, RemoveExistingProducts, and InstallFinalize.</span></span> <span data-ttu-id="280b5-117">En este caso, los archivos actualizados se instalan primero y, a continuación, se quitan los archivos antiguos.</span><span class="sxs-lookup"><span data-stu-id="280b5-117">In this case the updated files are installed first and then the old files are removed.</span></span> <span data-ttu-id="280b5-118">Sin embargo, si se produce un error en la eliminación de la aplicación anterior, el instalador revierte tanto la eliminación de la aplicación anterior como la instalación de la nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="280b5-118">However, if the removal of the old application fails, then the installer rolls back both the removal of the old application and the install of the new application.</span></span>
-   <span data-ttu-id="280b5-119">Después de la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="280b5-119">After the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="280b5-120">Esta es la ubicación más eficaz para la acción.</span><span class="sxs-lookup"><span data-stu-id="280b5-120">This is the most efficient placement for the action.</span></span> <span data-ttu-id="280b5-121">En este caso, el instalador actualiza los archivos antes de quitar las aplicaciones antiguas.</span><span class="sxs-lookup"><span data-stu-id="280b5-121">In this case, the installer updates files before removing the old applications.</span></span> <span data-ttu-id="280b5-122">Solo los archivos que se van a actualizar se instalan durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="280b5-122">Only the files being updated get installed during the installation.</span></span> <span data-ttu-id="280b5-123">Si se produce un error en la eliminación de la aplicación anterior, el instalador solo revierte la desinstalación de la aplicación anterior.</span><span class="sxs-lookup"><span data-stu-id="280b5-123">If the removal of the old application fails, then the installer only rolls back the uninstallation of the old application.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="280b5-124">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="280b5-124">ActionData Messages</span></span>



| <span data-ttu-id="280b5-125">Campo</span><span class="sxs-lookup"><span data-stu-id="280b5-125">Field</span></span> | <span data-ttu-id="280b5-126">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="280b5-126">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="280b5-127">\[1\]</span><span class="sxs-lookup"><span data-stu-id="280b5-127">\[1\]</span></span> | <span data-ttu-id="280b5-128">Se quitó el producto.</span><span class="sxs-lookup"><span data-stu-id="280b5-128">Removed product.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="280b5-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="280b5-129">Remarks</span></span>

<span data-ttu-id="280b5-130">Windows Installer establece la propiedad [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) cuando se ejecuta esta acción.</span><span class="sxs-lookup"><span data-stu-id="280b5-130">Windows Installer sets the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) Property when it runs this action.</span></span>

 

 



