---
description: Una acción personalizada puede llamar a funciones escritas en VBScript o JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677912"
---
# <a name="scripts"></a><span data-ttu-id="d1e38-103">Scripts</span><span class="sxs-lookup"><span data-stu-id="d1e38-103">Scripts</span></span>

<span data-ttu-id="d1e38-104">Una acción personalizada puede llamar a funciones escritas en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="d1e38-104">A custom action can call functions that are written in VBScript or JScript.</span></span> <span data-ttu-id="d1e38-105">Windows Installer no proporciona el motor de scripts.</span><span class="sxs-lookup"><span data-stu-id="d1e38-105">Windows Installer does not provide the script engine.</span></span> <span data-ttu-id="d1e38-106">Los autores que deseen usar un lenguaje de scripting durante la instalación deben asegurarse de que el motor de scripting adecuado esté disponible.</span><span class="sxs-lookup"><span data-stu-id="d1e38-106">Authors wishing to make use of a scripting language during installation must therefore ensure that the appropriate scripting engine is available.</span></span>

<span data-ttu-id="d1e38-107">El instalador no admite la versión 1,0 de JScript.</span><span class="sxs-lookup"><span data-stu-id="d1e38-107">The installer does not support JScript version 1.0.</span></span>

<span data-ttu-id="d1e38-108">Una acción personalizada de 64 bits basada en scripts debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico Actions personalizado en la columna Type de la tabla [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-108">A 64-bit custom action based on scripts must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction](customaction-table.md) table.</span></span> <span data-ttu-id="d1e38-109">Para obtener información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d1e38-109">For information see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

<span data-ttu-id="d1e38-110">Los siguientes tipos de acción personalizados básicos llaman a funciones escritas en el script.</span><span class="sxs-lookup"><span data-stu-id="d1e38-110">The following basic custom action types call functions written in script.</span></span>



| <span data-ttu-id="d1e38-111">Tipo de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="d1e38-111">Custom action type</span></span>                                 | <span data-ttu-id="d1e38-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1e38-112">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1e38-113">Tipo de acción personalizada 5</span><span class="sxs-lookup"><span data-stu-id="d1e38-113">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="d1e38-114">Archivo JScript almacenado en un flujo de tabla binaria.</span><span class="sxs-lookup"><span data-stu-id="d1e38-114">JScript file stored in a Binary table stream.</span></span>                                                  |
| [<span data-ttu-id="d1e38-115">Tipo de acción personalizada 21</span><span class="sxs-lookup"><span data-stu-id="d1e38-115">Custom Action Type 21</span></span>](custom-action-type-21.md) | <span data-ttu-id="d1e38-116">Archivo JScript que se instala con un producto.</span><span class="sxs-lookup"><span data-stu-id="d1e38-116">JScript file that is installed with a product.</span></span>                                                 |
| [<span data-ttu-id="d1e38-117">Tipo de acción personalizada 53</span><span class="sxs-lookup"><span data-stu-id="d1e38-117">Custom Action Type 53</span></span>](custom-action-type-53.md) | <span data-ttu-id="d1e38-118">Texto JScript especificado por un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d1e38-118">JScript text specified by a property value.</span></span>                                                    |
| [<span data-ttu-id="d1e38-119">Tipo de acción personalizada 37</span><span class="sxs-lookup"><span data-stu-id="d1e38-119">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="d1e38-120">Texto JScript almacenado en la columna de destino de la tabla [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-120">JScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span>  |
| [<span data-ttu-id="d1e38-121">Tipo de acción personalizada 6</span><span class="sxs-lookup"><span data-stu-id="d1e38-121">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="d1e38-122">Archivo VBScript almacenado en una secuencia de tabla [binaria](binary-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-122">VBScript file stored in a [Binary](binary-table.md) table stream.</span></span>                             |
| [<span data-ttu-id="d1e38-123">Tipo de acción personalizada 22</span><span class="sxs-lookup"><span data-stu-id="d1e38-123">Custom Action Type 22</span></span>](custom-action-type-22.md) | <span data-ttu-id="d1e38-124">Archivo VBScript que se instala con un producto.</span><span class="sxs-lookup"><span data-stu-id="d1e38-124">VBScript file that is installed with a product.</span></span>                                                |
| [<span data-ttu-id="d1e38-125">Tipo de acción personalizada 54</span><span class="sxs-lookup"><span data-stu-id="d1e38-125">Custom Action Type 54</span></span>](custom-action-type-54.md) | <span data-ttu-id="d1e38-126">Texto de VBScript especificado por un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d1e38-126">VBScript text specified by a property value.</span></span>                                                   |
| [<span data-ttu-id="d1e38-127">Tipo de acción personalizada 38</span><span class="sxs-lookup"><span data-stu-id="d1e38-127">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="d1e38-128">Texto de VBScript almacenado en la columna de destino de la tabla [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-128">VBScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span> |



 

> [!Note]  
> <span data-ttu-id="d1e38-129">El instalador ejecuta las acciones personalizadas de script directamente y no utiliza Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="d1e38-129">The installer runs script custom actions directly and does not use the Windows Script Host.</span></span> <span data-ttu-id="d1e38-130">El objeto **Wscript** no se puede usar en una acción personalizada de script porque el host de Windows Script proporciona este objeto.</span><span class="sxs-lookup"><span data-stu-id="d1e38-130">The **WScript** object cannot be used inside a script custom action because this object is provided by the Windows Script Host.</span></span> <span data-ttu-id="d1e38-131">Los objetos del modelo de objetos de Windows Script Host solo se pueden usar en acciones personalizadas si Windows Script Host está instalado en el equipo mediante la creación de nuevas instancias del objeto, con una llamada a CreateObject, y proporcionando el ProgId del objeto (por ejemplo, "WScript. Shell").</span><span class="sxs-lookup"><span data-stu-id="d1e38-131">Objects in the Windows Script Host object model can only be used in custom actions if Windows Script Host is installed on the computer by creating new instances of the object, with a call to CreateObject, and providing the ProgId of the object (for example "WScript.Shell").</span></span> <span data-ttu-id="d1e38-132">Dependiendo del tipo de acción personalizada de script, se puede denegar el acceso a algunos objetos y métodos del modelo de objetos de Windows Script Host por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d1e38-132">Depending on the type of script custom action, access to some objects and methods of the Windows Script Host object model may be denied for security reasons.</span></span>

 

<span data-ttu-id="d1e38-133">Para obtener más información, vea [lista de Resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md) para obtener un resumen de todos los tipos de acciones personalizadas y cómo se codifican en la tabla [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-133">For more information, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction](customaction-table.md) table.</span></span>

 

 



