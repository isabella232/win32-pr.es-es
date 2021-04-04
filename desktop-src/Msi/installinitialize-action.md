---
description: La acción InstallInitialize y la acción InstallFinalize marcan el principio y el final de una secuencia de acciones que cambian el sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Acción InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810303"
---
# <a name="installinitialize-action"></a><span data-ttu-id="14487-103">Acción InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="14487-103">InstallInitialize Action</span></span>

<span data-ttu-id="14487-104">La acción InstallInitialize y la acción [InstallFinalize](installfinalize-action.md) marcan el principio y el final de una secuencia de acciones que cambian el sistema.</span><span class="sxs-lookup"><span data-stu-id="14487-104">The InstallInitialize action and [InstallFinalize](installfinalize-action.md) action mark the beginning and end of a sequence of actions that change the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="14487-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="14487-105">Sequence Restrictions</span></span>

<span data-ttu-id="14487-106">La acción InstallInitialize se debe secuenciar antes que cualquier acción que cambie el sistema, como la acción [InstallFiles](installfiles-action.md) , la acción [WriteRegistryValues](writeregistryvalues-action.md) , la acción [SelfRegModules](selfregmodules-action.md) y la acción [ProcessComponents](processcomponents-action.md) .</span><span class="sxs-lookup"><span data-stu-id="14487-106">The InstallInitialize action must be sequenced before any actions that change the system, such as the [InstallFiles](installfiles-action.md) action, the [WriteRegistryValues](writeregistryvalues-action.md) action, the [SelfRegModules](selfregmodules-action.md) action, and the [ProcessComponents](processcomponents-action.md) action.</span></span> <span data-ttu-id="14487-107">Por lo tanto, la acción InstallInitialize se debe secuenciar antes de la acción [InstallFinalize](installfinalize-action.md) y la acción [InstallExecute](installexecute-action.md) .</span><span class="sxs-lookup"><span data-stu-id="14487-107">The InstallInitialize action must therefore be sequenced before the [InstallFinalize](installfinalize-action.md) action and the [InstallExecute](installexecute-action.md) action.</span></span>

<span data-ttu-id="14487-108">Las [acciones personalizadas](custom-actions.md) que modifican el paquete de Windows Installer, por ejemplo, agregando filas a una tabla que controla los recursos instalables, como la tabla [del registro](registry-table.md) o la tabla [DuplicateFile](duplicatefile-table.md) , se deben secuenciar antes de la acción InstallInitialize.</span><span class="sxs-lookup"><span data-stu-id="14487-108">[Custom actions](custom-actions.md) that modify the Windows Installer package, for example by adding rows to a table that handles installable resources, such as the [Registry](registry-table.md) table or [DuplicateFile](duplicatefile-table.md) table, must be sequenced before InstallInitialize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="14487-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="14487-109">ActionData Messages</span></span>

<span data-ttu-id="14487-110">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="14487-110">There are no ActionData messages.</span></span>

 

 



