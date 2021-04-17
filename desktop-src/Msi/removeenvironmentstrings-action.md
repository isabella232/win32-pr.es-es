---
description: La acción RemoveEnvironmentStrings modifica los valores de las variables de entorno.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Acción RemoveEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678596"
---
# <a name="removeenvironmentstrings-action"></a><span data-ttu-id="7f534-103">Acción RemoveEnvironmentStrings</span><span class="sxs-lookup"><span data-stu-id="7f534-103">RemoveEnvironmentStrings Action</span></span>

<span data-ttu-id="7f534-104">La acción RemoveEnvironmentStrings modifica los valores de las variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="7f534-104">The RemoveEnvironmentStrings action modifies the values of environment variables.</span></span>

<span data-ttu-id="7f534-105">Tenga en cuenta que las variables de entorno no cambian para la instalación en curso cuando se ejecutan las acciones [WriteEnvironmentStrings](writeenvironmentstrings-action.md) o RemoveEnvironmentStrings.</span><span class="sxs-lookup"><span data-stu-id="7f534-105">Note that environment variables do not change for the installation in progress when either the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) or RemoveEnvironmentStrings action are run.</span></span> <span data-ttu-id="7f534-106">En Windows 2000, esta información se almacena en el registro y se envía un mensaje para notificar al sistema los cambios cuando se completa la instalación.</span><span class="sxs-lookup"><span data-stu-id="7f534-106">On Windows 2000, this information is stored in the registry and a message is sent to notify the system of changes when the installation completes.</span></span> <span data-ttu-id="7f534-107">Un nuevo proceso u otro proceso que compruebe estos mensajes usará las nuevas variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="7f534-107">A new process, or another process that checks for these messages, will use the new environment variables.</span></span>

<span data-ttu-id="7f534-108">El instalador ejecuta la [acción WriteEnvironmentStrings](writeenvironmentstrings-action.md) solo durante la instalación o reinstalación de un componente, y ejecuta la acción RemoveEnvironmentStrings solo durante la eliminación de un componente.</span><span class="sxs-lookup"><span data-stu-id="7f534-108">The installer runs the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) only during the installation or reinstallation of a component, and runs the RemoveEnvironmentStrings action only during the removal of a component.</span></span>

<span data-ttu-id="7f534-109">Los valores se escriben o se quitan en función de la selección de las acciones y modificadores principales.</span><span class="sxs-lookup"><span data-stu-id="7f534-109">Values are written or removed based on the selection of primary actions and modifiers.</span></span> <span data-ttu-id="7f534-110">Se describen en la siguiente sección de mensajes de ActionData.</span><span class="sxs-lookup"><span data-stu-id="7f534-110">These are described in the following ActionData Messages section.</span></span> <span data-ttu-id="7f534-111">Tenga en cuenta que, en función de la acción especificada, WriteEnvironmentStrings puede quitar variables y RemoveEnvironmentStrings puede agregarlas en función de la creación de la [tabla de entorno](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="7f534-111">Note that depending upon the action specified, WriteEnvironmentStrings may remove variables, and RemoveEnvironmentStrings may add them based on the authoring of the [Environment table](environment-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7f534-112">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="7f534-112">Sequence Restrictions</span></span>

<span data-ttu-id="7f534-113">La [acción InstallValidate](installvalidate-action.md) se debe ejecutar antes de la acción RemoveEnvironmentStrings.</span><span class="sxs-lookup"><span data-stu-id="7f534-113">The [InstallValidate action](installvalidate-action.md) must be executed before the RemoveEnvironmentStrings action.</span></span> <span data-ttu-id="7f534-114">Dado que la acción WriteEnvironmentStrings y la acción RemoveEnvironmentStrings nunca se aplican durante la instalación o desinstalación de un componente, su secuencia relativa no está restringida.</span><span class="sxs-lookup"><span data-stu-id="7f534-114">Because the WriteEnvironmentStrings action and RemoveEnvironmentStrings action are never both applied during the installation or removal of a component, their relative sequence is not restricted.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7f534-115">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="7f534-115">ActionData Messages</span></span>



| <span data-ttu-id="7f534-116">Campo</span><span class="sxs-lookup"><span data-stu-id="7f534-116">Field</span></span> | <span data-ttu-id="7f534-117">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="7f534-117">Description of action data</span></span>                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f534-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7f534-118">\[1\]</span></span> | <span data-ttu-id="7f534-119">Nombre de la variable de entorno que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="7f534-119">Name of the environment variable to modify.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="7f534-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="7f534-120">\[2\]</span></span> | <span data-ttu-id="7f534-121">Valor de la variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="7f534-121">The environment variable value.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="7f534-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="7f534-122">\[3\]</span></span> | <span data-ttu-id="7f534-123">Se trata de un campo de marcas de bits que especifican la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="7f534-123">This is a field of bit flags that specify the action to be performed.</span></span> <span data-ttu-id="7f534-124">Incluya un solo bit para una acción principal.</span><span class="sxs-lookup"><span data-stu-id="7f534-124">Include only one bit for a primary action.</span></span> <span data-ttu-id="7f534-125">Puede haber más de un bit modificador incluido en este campo.</span><span class="sxs-lookup"><span data-stu-id="7f534-125">There may be more than one modifier bit included in this field.</span></span> <span data-ttu-id="7f534-126">Vea las siguientes descripciones de marcas de bits.</span><span class="sxs-lookup"><span data-stu-id="7f534-126">See the following bit flag descriptions.</span></span> |



 



| <span data-ttu-id="7f534-127">Valor de bit</span><span class="sxs-lookup"><span data-stu-id="7f534-127">Bit value</span></span> | <span data-ttu-id="7f534-128">Descripción de las acciones principales</span><span class="sxs-lookup"><span data-stu-id="7f534-128">Description of primary actions</span></span>                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f534-129">0x1</span><span class="sxs-lookup"><span data-stu-id="7f534-129">0x1</span></span>       | <span data-ttu-id="7f534-130">Establecer.</span><span class="sxs-lookup"><span data-stu-id="7f534-130">Set.</span></span> <span data-ttu-id="7f534-131">Establece el valor de la variable de entorno en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="7f534-131">Sets the value of the environment variable in all cases.</span></span><br/> <span data-ttu-id="7f534-132">Si este bit se combina con un bit de modificador Append o PREFIX, la acción agrega el valor a cualquier valor existente de la variable.</span><span class="sxs-lookup"><span data-stu-id="7f534-132">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/> |
| <span data-ttu-id="7f534-133">0x2</span><span class="sxs-lookup"><span data-stu-id="7f534-133">0x2</span></span>       | <span data-ttu-id="7f534-134">Establecer.</span><span class="sxs-lookup"><span data-stu-id="7f534-134">Set.</span></span> <span data-ttu-id="7f534-135">Establece el valor si la variable está ausente.</span><span class="sxs-lookup"><span data-stu-id="7f534-135">Sets the value if the variable is absent.</span></span><br/> <span data-ttu-id="7f534-136">Si este bit se combina con un bit de modificador Append o PREFIX, la acción agrega el valor a cualquier valor existente de la variable.</span><span class="sxs-lookup"><span data-stu-id="7f534-136">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/>                |
| <span data-ttu-id="7f534-137">0x4</span><span class="sxs-lookup"><span data-stu-id="7f534-137">0x4</span></span>       | <span data-ttu-id="7f534-138">Eliminar.</span><span class="sxs-lookup"><span data-stu-id="7f534-138">Remove.</span></span> <span data-ttu-id="7f534-139">Quita el valor de la variable.</span><span class="sxs-lookup"><span data-stu-id="7f534-139">Removes the value from the variable.</span></span><br/> <span data-ttu-id="7f534-140">Si este bit se combina con un bit de modificador Append o PREFIX, el valor se quita de la cadena existente, si el valor existe.</span><span class="sxs-lookup"><span data-stu-id="7f534-140">If this bit is combined with an Append or Prefix modifier bit, the value is removed from the existing string, if the value exists.</span></span><br/>               |



 



| <span data-ttu-id="7f534-141">Valor de bit</span><span class="sxs-lookup"><span data-stu-id="7f534-141">Bit value</span></span>  | <span data-ttu-id="7f534-142">Descripción del modificador</span><span class="sxs-lookup"><span data-stu-id="7f534-142">Description of modifier</span></span>                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f534-143">0x20000000</span><span class="sxs-lookup"><span data-stu-id="7f534-143">0x20000000</span></span> | <span data-ttu-id="7f534-144">Si se establece este bit, las acciones se aplican a las variables de entorno del equipo.</span><span class="sxs-lookup"><span data-stu-id="7f534-144">If this bit is set, actions are applied to the machine environment variables.</span></span><br/> <span data-ttu-id="7f534-145">Si no se establece este bit, las acciones se aplican a las variables de entorno del usuario.</span><span class="sxs-lookup"><span data-stu-id="7f534-145">If this bit is not set, actions are applied to the user's environment variables.</span></span><br/> |
| <span data-ttu-id="7f534-146">0x40000000</span><span class="sxs-lookup"><span data-stu-id="7f534-146">0x40000000</span></span> | <span data-ttu-id="7f534-147">Anexar.</span><span class="sxs-lookup"><span data-stu-id="7f534-147">Append.</span></span> <span data-ttu-id="7f534-148">Este bit es opcional.</span><span class="sxs-lookup"><span data-stu-id="7f534-148">This bit is optional.</span></span> <span data-ttu-id="7f534-149">No establezca los modificadores Append y prefix.</span><span class="sxs-lookup"><span data-stu-id="7f534-149">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |
| <span data-ttu-id="7f534-150">0x80000000</span><span class="sxs-lookup"><span data-stu-id="7f534-150">0x80000000</span></span> | <span data-ttu-id="7f534-151">Ceder.</span><span class="sxs-lookup"><span data-stu-id="7f534-151">Prefix.</span></span> <span data-ttu-id="7f534-152">Este bit es opcional.</span><span class="sxs-lookup"><span data-stu-id="7f534-152">This bit is optional.</span></span> <span data-ttu-id="7f534-153">No establezca los modificadores Append y prefix.</span><span class="sxs-lookup"><span data-stu-id="7f534-153">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |



 

 

 




