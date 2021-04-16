---
description: El valor lógico de una propiedad que se ha establecido es true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Usar propiedades en instrucciones condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677395"
---
# <a name="using-properties-in-conditional-statements"></a><span data-ttu-id="efdaf-103">Usar propiedades en instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="efdaf-103">Using Properties in Conditional Statements</span></span>

<span data-ttu-id="efdaf-104">El valor lógico de una propiedad que se ha establecido es true.</span><span class="sxs-lookup"><span data-stu-id="efdaf-104">The logical value of a property that has been set is True.</span></span> <span data-ttu-id="efdaf-105">Para determinar si una propiedad se establece sin obtener realmente su valor, pruebe la expresión lógica "propiedad" o "no propiedad".</span><span class="sxs-lookup"><span data-stu-id="efdaf-105">To determine whether a property is set without actually getting its value, test the logical expression "MyProperty" or "Not MyProperty".</span></span> <span data-ttu-id="efdaf-106">Cuando se establece la propiedad Property, el primero se evalúa como true y el último como false.</span><span class="sxs-lookup"><span data-stu-id="efdaf-106">When the property MyProperty is set, the former evaluates as True and the latter as False.</span></span>

<span data-ttu-id="efdaf-107">Una o más propiedades se pueden combinar con operadores para formar expresiones lógicas utilizadas en instrucciones condicionales.</span><span class="sxs-lookup"><span data-stu-id="efdaf-107">One or more properties can be combined with operators to form logical expressions used in a conditional statements.</span></span> <span data-ttu-id="efdaf-108">Para obtener más información sobre los operadores que se pueden utilizar en instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="efdaf-108">For more information about the operators that can be used in conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="efdaf-109">Se puede especificar una instrucción condicional con propiedades en la columna condición de la [tabla condición](condition-table.md) para modificar el estado de selección de cualquier entrada en la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="efdaf-109">A conditional statement using properties can be entered into the Condition column of the [Condition table](condition-table.md) to modify the selection state of any entry in the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="efdaf-110">Las instrucciones condicionales con una o más propiedades se usan normalmente en la columna condición de las tablas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="efdaf-110">Conditional statements with one or more properties are commonly used in the Condition column of database tables.</span></span>

<span data-ttu-id="efdaf-111">Cada una de las tablas siguientes tiene una columna para las expresiones condicionales:</span><span class="sxs-lookup"><span data-stu-id="efdaf-111">The following tables each have a column for conditional expressions:</span></span>

-   [<span data-ttu-id="efdaf-112">Tabla de condiciones</span><span class="sxs-lookup"><span data-stu-id="efdaf-112">Condition table</span></span>](condition-table.md)
-   [<span data-ttu-id="efdaf-113">Tabla ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="efdaf-113">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="efdaf-114">Tabla LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="efdaf-114">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="efdaf-115">Tabla InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="efdaf-115">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="efdaf-116">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="efdaf-116">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="efdaf-117">Tabla ControlCondition</span><span class="sxs-lookup"><span data-stu-id="efdaf-117">ControlCondition table</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="efdaf-118">Tabla AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="efdaf-118">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="efdaf-119">Tabla AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="efdaf-119">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="efdaf-120">Tabla AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="efdaf-120">AdminUISequence table</span></span>](adminuisequence-table.md)

<span data-ttu-id="efdaf-121">Tenga en cuenta que las seis tablas de secuencia de acciones tienen campos para una condición.</span><span class="sxs-lookup"><span data-stu-id="efdaf-121">Note that the six action sequence tables have fields for a condition.</span></span> <span data-ttu-id="efdaf-122">Si la expresión condicional de este campo se evalúa como false, el instalador omite esa acción.</span><span class="sxs-lookup"><span data-stu-id="efdaf-122">If the conditional expression in this field evaluates to False, the installer skips that action.</span></span>

<span data-ttu-id="efdaf-123">Si establece una [propiedad privada](private-properties.md) en la secuencia de la interfaz de usuario mediante la creación de una acción personalizada en una de las tablas de secuencia de la interfaz de usuario, esa propiedad no se establece en la secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="efdaf-123">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="efdaf-124">Para establecer la propiedad en la secuencia de ejecución, también debe colocar una acción personalizada en una tabla de secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="efdaf-124">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="efdaf-125">Como alternativa, puede convertir la propiedad en una [propiedad pública](public-properties.md) e incluirla en la propiedad [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="efdaf-125">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="efdaf-126">Para obtener más información, vea [usar una tabla de secuencia](using-a-sequence-table.md) o [usar propiedades](using-properties.md).</span><span class="sxs-lookup"><span data-stu-id="efdaf-126">For more information, see [Using a Sequence Table](using-a-sequence-table.md) or [Using Properties](using-properties.md).</span></span>

 

 



