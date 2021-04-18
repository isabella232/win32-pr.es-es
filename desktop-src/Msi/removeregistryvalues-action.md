---
description: La acción RemoveRegistryValues solo puede quitar valores del registro del sistema que se han creado en la tabla del registro o en la tabla RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Acción RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667670"
---
# <a name="removeregistryvalues-action"></a><span data-ttu-id="a6c90-103">Acción RemoveRegistryValues</span><span class="sxs-lookup"><span data-stu-id="a6c90-103">RemoveRegistryValues Action</span></span>

<span data-ttu-id="a6c90-104">La acción RemoveRegistryValues solo puede quitar valores del registro del sistema que se han creado en la [tabla del registro](registry-table.md) o en la [tabla RemoveRegistry](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="a6c90-104">The RemoveRegistryValues action can only remove values from the system registry that have been authored into the [Registry table](registry-table.md) or the [RemoveRegistry table](removeregistry-table.md).</span></span> <span data-ttu-id="a6c90-105">Esta acción quita un valor del registro que se ha creado en la tabla del registro si el componente asociado se instaló localmente o como ejecutado desde el origen y ahora está configurado para desinstalarse.</span><span class="sxs-lookup"><span data-stu-id="a6c90-105">This action removes a registry value that has been authored into the Registry table if the associated component was installed locally or as run from source and is now set to be uninstalled.</span></span> <span data-ttu-id="a6c90-106">Esta acción quita un valor del registro que se ha creado en la tabla RemoveRegistry si el componente asociado está configurado para instalarse localmente o como ejecutar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="a6c90-106">This action removes a registry value that has been authored into the RemoveRegistry table if the associated component is set to be installed locally or as run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a6c90-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="a6c90-107">Sequence Restrictions</span></span>

<span data-ttu-id="a6c90-108">Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de llamar a RemoveRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="a6c90-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveRegistryValues.</span></span> <span data-ttu-id="a6c90-109">Si se usa una acción [WriteRegistryValues](writeregistryvalues-action.md) , debe aparecer después de RemoveRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="a6c90-109">If a [WriteRegistryValues](writeregistryvalues-action.md) action is used, it must come after RemoveRegistryValues.</span></span> <span data-ttu-id="a6c90-110">RemoveRegistryValues debe ser anterior a [UnregisterMIMEInfo](unregistermimeinfo-action.md) o [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="a6c90-110">RemoveRegistryValues must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) or [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span></span>

<span data-ttu-id="a6c90-111">Se puede utilizar una acción personalizada para agregar filas a la [tabla del registro](registry-table.md) durante una operación de instalación, desinstalación o reparación.</span><span class="sxs-lookup"><span data-stu-id="a6c90-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="a6c90-112">Estas filas no se conservan en la tabla del registro y la información solo está disponible durante la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="a6c90-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="a6c90-113">Por lo tanto, la acción personalizada se debe ejecutar en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales.</span><span class="sxs-lookup"><span data-stu-id="a6c90-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="a6c90-114">La acción personalizada debe ser anterior a las acciones RemoveRegistryValues y [WriteRegistryValues](writeregistryvalues-action.md) en la secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="a6c90-114">The custom action must come before the RemoveRegistryValues and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a6c90-115">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="a6c90-115">ActionData Messages</span></span>



| <span data-ttu-id="a6c90-116">Campo</span><span class="sxs-lookup"><span data-stu-id="a6c90-116">Field</span></span> | <span data-ttu-id="a6c90-117">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="a6c90-117">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="a6c90-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a6c90-118">\[1\]</span></span> | <span data-ttu-id="a6c90-119">Ruta de acceso del registro a la clave del valor del registro que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="a6c90-119">Registry path to key of removed registry value.</span></span>     |
| <span data-ttu-id="a6c90-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a6c90-120">\[2\]</span></span> | <span data-ttu-id="a6c90-121">Cadena con formato del nombre del valor del registro que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="a6c90-121">Formatted string of name of removed registry value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a6c90-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6c90-122">Remarks</span></span>

<span data-ttu-id="a6c90-123">Para quitar un valor del registro, grabe el valor en la columna valor de la tabla del registro.</span><span class="sxs-lookup"><span data-stu-id="a6c90-123">To remove a registry value, record the value in the Value column of the Registry table.</span></span> <span data-ttu-id="a6c90-124">Si la acción de WriteRegistryValues ha adjuntado las cadenas de REG \_ multi \_ SZ al valor de la [tabla del registro](registry-table.md), la acción RemoveRegistryValues quita solo esas cadenas del valor del registro.</span><span class="sxs-lookup"><span data-stu-id="a6c90-124">If the WriteRegistryValues action has attached REG\_MULTI\_SZ strings to the value in the [Registry table](registry-table.md), then the RemoveRegistryValues action removes only those strings from the registry value.</span></span>

 

 



