---
description: La acción InstallFinalize ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la ejecución de las acciones InstallExecute o InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Acción InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811288"
---
# <a name="installfinalize-action"></a><span data-ttu-id="3441a-103">Acción InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="3441a-103">InstallFinalize Action</span></span>

<span data-ttu-id="3441a-104">La acción InstallFinalize ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la ejecución de las acciones [InstallExecute](installexecute-action.md) o [InstallExecuteAgain](installexecuteagain-action.md) .</span><span class="sxs-lookup"><span data-stu-id="3441a-104">The InstallFinalize action runs a script that contains all operations in the action sequence since either the start of the installation or the execution of the [InstallExecute](installexecute-action.md) or [InstallExecuteAgain](installexecuteagain-action.md) actions.</span></span> <span data-ttu-id="3441a-105">Esta acción marca el final de una transacción que comienza con la acción [InstallInitialize](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="3441a-105">This action marks the end of a transaction that begins with the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3441a-106">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="3441a-106">Sequence Restrictions</span></span>

<span data-ttu-id="3441a-107">La acción [InstallInitialize](installinitialize-action.md) debe ser anterior a la acción InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="3441a-107">The [InstallInitialize](installinitialize-action.md) action must come before the InstallFinalize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3441a-108">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="3441a-108">ActionData Messages</span></span>

<span data-ttu-id="3441a-109">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="3441a-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="3441a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3441a-110">Remarks</span></span>

<span data-ttu-id="3441a-111">Si se detecta que el producto está marcado para su eliminación completa, las operaciones se agregan automáticamente al script para quitar la **adición o eliminación de programas** en la información del **Panel de control** del producto, para anular el registro y anular la publicación del producto y para quitar la base de datos local almacenada en caché de% Windows%, si existe.</span><span class="sxs-lookup"><span data-stu-id="3441a-111">If it is detected that the product is marked for complete removal, operations are automatically added to the script to remove the **Add/Remove Programs** in the **Control Panel** information for the product, to unregister and unpublish the product, and to remove the cached local database from %WINDOWS%, if it exists.</span></span>

<span data-ttu-id="3441a-112">Es posible que los cambios realizados en el sistema antes de la acción no se restauren después de ejecutar la acción InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="3441a-112">System changes made before the action may not be restored after the InstallFinalize action is executed.</span></span> <span data-ttu-id="3441a-113">La acción InstallFinalize actualiza el sistema con todas las operaciones que se determinan en ese momento y, a continuación, finaliza la transacción.</span><span class="sxs-lookup"><span data-stu-id="3441a-113">The InstallFinalize action updates the system with all operations determined to that point and then ends the transaction.</span></span>

 

 



