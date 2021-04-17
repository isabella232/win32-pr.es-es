---
description: La acción WriteRegistryValues configura la información del registro de una aplicación.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Acción WriteRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678019"
---
# <a name="writeregistryvalues-action"></a><span data-ttu-id="c183c-103">Acción WriteRegistryValues</span><span class="sxs-lookup"><span data-stu-id="c183c-103">WriteRegistryValues Action</span></span>

<span data-ttu-id="c183c-104">La acción WriteRegistryValues configura la información del registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c183c-104">The WriteRegistryValues action sets up an application's registry information.</span></span> <span data-ttu-id="c183c-105">La información del registro se valida mediante la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c183c-105">The registry information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="c183c-106">Un valor del registro se escribe en el registro si se ha establecido que el componente correspondiente se instale localmente o como ejecutado desde el origen.</span><span class="sxs-lookup"><span data-stu-id="c183c-106">A registry value is written to the registry if the corresponding component has been set to be installed either locally or as run from source.</span></span> <span data-ttu-id="c183c-107">Para obtener más información, vea [tabla del registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="c183c-107">For more information, see [Registry table](registry-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c183c-108">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="c183c-108">Sequence Restrictions</span></span>

<span data-ttu-id="c183c-109">La [acción InstallValidate](installvalidate-action.md) debe ser anterior a la acción WriteRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="c183c-109">The [InstallValidate action](installvalidate-action.md) must come before the WriteRegistryValues action.</span></span> <span data-ttu-id="c183c-110">Si hay una [acción RemoveRegistryValues](removeregistryvalues-action.md), debe ser anterior a la acción WriteRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="c183c-110">If there is a [RemoveRegistryValues action](removeregistryvalues-action.md), then it must come before the WriteRegistryValues action.</span></span>

<span data-ttu-id="c183c-111">Se puede utilizar una acción personalizada para agregar filas a la [tabla del registro](registry-table.md) durante una operación de instalación, desinstalación o reparación.</span><span class="sxs-lookup"><span data-stu-id="c183c-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="c183c-112">Estas filas no se conservan en la tabla del registro y la información solo está disponible durante la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="c183c-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="c183c-113">Por lo tanto, la acción personalizada se debe ejecutar en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales.</span><span class="sxs-lookup"><span data-stu-id="c183c-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="c183c-114">La acción personalizada debe ser anterior a las acciones [RemoveRegistryValues](removeregistryvalues-action.md) y WriteRegistryValues en la secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="c183c-114">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and WriteRegistryValues actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c183c-115">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="c183c-115">ActionData Messages</span></span>



| <span data-ttu-id="c183c-116">Campo</span><span class="sxs-lookup"><span data-stu-id="c183c-116">Field</span></span> | <span data-ttu-id="c183c-117">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="c183c-117">Description of action data</span></span>                               |
|-------|----------------------------------------------------------|
| <span data-ttu-id="c183c-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c183c-118">\[1\]</span></span> | <span data-ttu-id="c183c-119">Ruta de acceso a la clave del registro del valor escrito en el registro.</span><span class="sxs-lookup"><span data-stu-id="c183c-119">Path to registry key of value written to registry.</span></span>       |
| <span data-ttu-id="c183c-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="c183c-120">\[2\]</span></span> | <span data-ttu-id="c183c-121">Nombre de cadena de texto con formato del valor escrito en el registro.</span><span class="sxs-lookup"><span data-stu-id="c183c-121">Formatted text string name of value written to registry.</span></span> |
| <span data-ttu-id="c183c-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="c183c-122">\[3\]</span></span> | <span data-ttu-id="c183c-123">Cadena de texto con formato del valor escrito en el registro.</span><span class="sxs-lookup"><span data-stu-id="c183c-123">Formatted text string of value written to registry.</span></span>      |



 

 

 



