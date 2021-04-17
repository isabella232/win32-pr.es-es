---
description: La acción RemoveShortcuts administra la eliminación de un acceso directo anunciado cuya característica está seleccionada para la desinstalación o un acceso directo no anunciado cuyo componente está seleccionado para la desinstalación. Para obtener más información, vea la tabla de acceso directo.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Acción RemoveShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652786"
---
# <a name="removeshortcuts-action"></a><span data-ttu-id="7279e-104">Acción RemoveShortcuts</span><span class="sxs-lookup"><span data-stu-id="7279e-104">RemoveShortcuts Action</span></span>

<span data-ttu-id="7279e-105">La acción RemoveShortcuts administra la eliminación de un acceso directo anunciado cuya característica está seleccionada para la desinstalación o un acceso directo no anunciado cuyo componente está seleccionado para la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="7279e-105">The RemoveShortcuts action manages the removal of an advertised shortcut whose feature is selected for uninstallation or a nonadvertised shortcut whose component is selected for uninstallation.</span></span> <span data-ttu-id="7279e-106">Para obtener más información, vea la [tabla de acceso directo](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="7279e-106">For more information, see the [Shortcut Table](shortcut-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7279e-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="7279e-107">Sequence Restrictions</span></span>

<span data-ttu-id="7279e-108">La acción RemoveShortcuts debe ser anterior a la acción [CreateShortcuts](createshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7279e-108">The RemoveShortcuts action must come before the [CreateShortcuts](createshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7279e-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="7279e-109">ActionData Messages</span></span>



| <span data-ttu-id="7279e-110">Campo</span><span class="sxs-lookup"><span data-stu-id="7279e-110">Field</span></span> | <span data-ttu-id="7279e-111">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="7279e-111">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="7279e-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7279e-112">\[1\]</span></span> | <span data-ttu-id="7279e-113">Identificador del acceso directo quitado.</span><span class="sxs-lookup"><span data-stu-id="7279e-113">Identifier of removed shortcut.</span></span> |



 

 

 



