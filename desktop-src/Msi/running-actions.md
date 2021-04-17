---
description: Las funciones de instalador se pueden usar para ejecutar acciones específicas o secuencias de acción.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Ejecutar acciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666796"
---
# <a name="running-actions"></a><span data-ttu-id="830d7-103">Ejecutar acciones</span><span class="sxs-lookup"><span data-stu-id="830d7-103">Running Actions</span></span>

<span data-ttu-id="830d7-104">Las funciones de instalador se pueden usar para ejecutar acciones específicas o secuencias de acción.</span><span class="sxs-lookup"><span data-stu-id="830d7-104">The installer functions can be used to run specific actions or action sequences.</span></span> <span data-ttu-id="830d7-105">Estas acciones pueden ser acciones [estándar](standard-actions.md) o [personalizadas](custom-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="830d7-105">These actions can either be [standard](standard-actions.md) or [custom](custom-actions.md) actions.</span></span> <span data-ttu-id="830d7-106">En el procedimiento siguiente se describe cómo ejecutar acciones:</span><span class="sxs-lookup"><span data-stu-id="830d7-106">The following procedure describes how to run actions:</span></span>

<span data-ttu-id="830d7-107">**Para ejecutar una secuencia de acciones**</span><span class="sxs-lookup"><span data-stu-id="830d7-107">**To run an action sequence**</span></span>

1.  <span data-ttu-id="830d7-108">Ejecute una secuencia de acciones definida en una tabla mediante una llamada a la función [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .</span><span class="sxs-lookup"><span data-stu-id="830d7-108">Run a sequence of actions defined in a table by calling the [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) function.</span></span>

    <span data-ttu-id="830d7-109">El instalador consulta la tabla indicada y ejecuta cada acción si su expresión condicional se evalúa como TRUE.</span><span class="sxs-lookup"><span data-stu-id="830d7-109">The installer queries the indicated table and runs each action if its conditional expression evaluates to TRUE.</span></span>

2.  <span data-ttu-id="830d7-110">Compruebe las expresiones condicionales mediante una llamada a la función [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="830d7-110">Check conditional expressions by calling the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>
3.  <span data-ttu-id="830d7-111">Ejecute la acción mediante una llamada a la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="830d7-111">Run the action by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span> <span data-ttu-id="830d7-112">La acción puede ser una acción estándar, una acción personalizada o un cuadro de diálogo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="830d7-112">The action can be a standard action, a custom action, or a user interface dialog box.</span></span>
4.  <span data-ttu-id="830d7-113">Si se produjo un error durante la ejecución de esta acción, llame a la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="830d7-113">If an error occurred during the execution of this action, call the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="830d7-114">El instalador procesará el error.</span><span class="sxs-lookup"><span data-stu-id="830d7-114">The installer will process the error.</span></span>

 

 



