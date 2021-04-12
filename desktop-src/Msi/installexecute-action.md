---
description: La acción InstallExecute ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción InstallExecute o InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Acción InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153877"
---
# <a name="installexecute-action"></a><span data-ttu-id="dd4d2-103">Acción InstallExecute</span><span class="sxs-lookup"><span data-stu-id="dd4d2-103">InstallExecute Action</span></span>

<span data-ttu-id="dd4d2-104">La acción InstallExecute ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción InstallExecute o [InstallExecuteAgain](installexecuteagain-action.md).</span><span class="sxs-lookup"><span data-stu-id="dd4d2-104">The InstallExecute action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecute action or [InstallExecuteAgain action](installexecuteagain-action.md).</span></span> <span data-ttu-id="dd4d2-105">La acción InstallExecute actualiza el sistema sin finalizar la transacción.</span><span class="sxs-lookup"><span data-stu-id="dd4d2-105">The InstallExecute action updates the system without ending the transaction.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="dd4d2-106">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="dd4d2-106">Sequence Restrictions</span></span>

<span data-ttu-id="dd4d2-107">La acción InstallExecute se incluye entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="dd4d2-107">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="dd4d2-108">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="dd4d2-108">ActionData Messages</span></span>

<span data-ttu-id="dd4d2-109">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="dd4d2-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd4d2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd4d2-110">Remarks</span></span>

<span data-ttu-id="dd4d2-111">La [acción InstallExecuteAgain](installexecuteagain-action.md) hace lo mismo que la acción InstallExecute.</span><span class="sxs-lookup"><span data-stu-id="dd4d2-111">The [InstallExecuteAgain action](installexecuteagain-action.md) does the same thing as the InstallExecute action.</span></span> <span data-ttu-id="dd4d2-112">Dado que las tablas de secuencia solo tienen una clave principal, la columna de acción, no se puede repetir la misma acción en una tabla de secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="dd4d2-112">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="dd4d2-113">Existen dos acciones que hacen lo mismo, InstallExecute y InstallExecuteAgain, para los casos en los que la funcionalidad de InstallExecute se necesita dos veces en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd4d2-113">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="dd4d2-114">Para obtener más información, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd4d2-114">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



