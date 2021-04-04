---
description: La acción BindImage enlaza cada archivo ejecutable o DLL que se debe enlazar a los archivos dll importados por él.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Acción BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909057"
---
# <a name="bindimage-action"></a><span data-ttu-id="8f806-103">Acción BindImage</span><span class="sxs-lookup"><span data-stu-id="8f806-103">BindImage Action</span></span>

<span data-ttu-id="8f806-104">La acción BindImage enlaza cada archivo ejecutable o DLL que se debe enlazar a los archivos dll importados por él.</span><span class="sxs-lookup"><span data-stu-id="8f806-104">The BindImage action binds each executable or DLL that must be bound to the DLLs imported by it.</span></span> <span data-ttu-id="8f806-105">La acción BindImage actúa en cada archivo de la tabla [BindImage](bindimage-table.md) , pero solo en los que se van a instalar localmente.</span><span class="sxs-lookup"><span data-stu-id="8f806-105">The BindImage action acts on each file in the [BindImage](bindimage-table.md) table, but only those that are to be installed locally.</span></span> <span data-ttu-id="8f806-106">El instalador calcula la dirección virtual de cada función importada de todos los archivos dll y, a continuación, guarda la dirección virtual calculada en la [*tabla de direcciones de importación*](i-gly.md) (IAT) de la imagen de importación.</span><span class="sxs-lookup"><span data-stu-id="8f806-106">The installer computes the virtual address of each function imported from all DLLs, then saves the computed virtual address in the importing image's [*import address table*](i-gly.md) (IAT).</span></span>

<span data-ttu-id="8f806-107">La acción BindImage llama internamente a la API de Windows **BindImageEx** .</span><span class="sxs-lookup"><span data-stu-id="8f806-107">The BindImage Action internally calls the **BindImageEx** Windows API.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8f806-108">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="8f806-108">Sequence Restrictions</span></span>

<span data-ttu-id="8f806-109">La acción BindImage debe aparecer después de la acción [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8f806-109">The BindImage action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8f806-110">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="8f806-110">ActionData Messages</span></span>



| <span data-ttu-id="8f806-111">Campo</span><span class="sxs-lookup"><span data-stu-id="8f806-111">Field</span></span> | <span data-ttu-id="8f806-112">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="8f806-112">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="8f806-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8f806-113">\[1\]</span></span> | <span data-ttu-id="8f806-114">Identificador del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="8f806-114">File identifier of executable.</span></span> |



 

 

 



