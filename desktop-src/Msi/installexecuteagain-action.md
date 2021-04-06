---
description: La acción InstallExecuteAgain ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción InstallExecuteAgain o la última acción InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Acción InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001066"
---
# <a name="installexecuteagain-action"></a><span data-ttu-id="751f2-103">Acción InstallExecuteAgain</span><span class="sxs-lookup"><span data-stu-id="751f2-103">InstallExecuteAgain Action</span></span>

<span data-ttu-id="751f2-104">La acción InstallExecuteAgain ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción InstallExecuteAgain o la última [acción InstallExecute](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="751f2-104">The InstallExecuteAgain action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecuteAgain action or the last [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="751f2-105">La acción InstallExecute actualiza el sistema sin finalizar la transacción.</span><span class="sxs-lookup"><span data-stu-id="751f2-105">The InstallExecute action updates the system without ending the transaction.</span></span> <span data-ttu-id="751f2-106">InstallExecuteAgain realiza la misma operación que la [acción InstallExecute](installexecute-action.md) , pero solo debe usarse después de InstallExecute.</span><span class="sxs-lookup"><span data-stu-id="751f2-106">InstallExecuteAgain performs the same operation as the [InstallExecute action](installexecute-action.md) but should only be used after InstallExecute.</span></span>

<span data-ttu-id="751f2-107">InstallExecuteAgain siempre debe establecerse para que no se ejecute durante la eliminación.</span><span class="sxs-lookup"><span data-stu-id="751f2-107">InstallExecuteAgain should always be set so that it does not run during removal.</span></span> <span data-ttu-id="751f2-108">Para obtener más información, vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="751f2-108">For information, see [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="751f2-109">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="751f2-109">Sequence Restrictions</span></span>

<span data-ttu-id="751f2-110">La acción InstallExecute se incluye entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="751f2-110">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="751f2-111">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="751f2-111">ActionData Messages</span></span>

<span data-ttu-id="751f2-112">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="751f2-112">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="751f2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="751f2-113">Remarks</span></span>

<span data-ttu-id="751f2-114">La acción InstallExecuteAgain hace lo mismo que la [acción InstallExecute](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="751f2-114">The InstallExecuteAgain action does the same thing as the [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="751f2-115">Dado que las tablas de secuencia solo tienen una clave principal, la columna de acción, no se puede repetir la misma acción en una tabla de secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="751f2-115">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="751f2-116">Existen dos acciones que hacen lo mismo, InstallExecute y InstallExecuteAgain, para los casos en los que la funcionalidad de InstallExecute se necesita dos veces en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="751f2-116">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="751f2-117">Para obtener más información, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="751f2-117">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



