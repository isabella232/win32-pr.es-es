---
description: Las acciones personalizadas escritas en JScript o Visual Basic, Scripting Edition (VBScript) pueden llamar a una función opcional. Estas funciones deben devolver uno de los valores que se muestran en la tabla siguiente.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valores devueltos de las acciones personalizadas de JScript y VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666800"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a><span data-ttu-id="ea8a5-104">Valores devueltos de las acciones personalizadas de JScript y VBScript</span><span class="sxs-lookup"><span data-stu-id="ea8a5-104">Return Values of JScript and VBScript Custom Actions</span></span>

<span data-ttu-id="ea8a5-105">Las acciones personalizadas escritas en JScript o Visual Basic, Scripting Edition (VBScript) pueden llamar a una función opcional.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-105">Custom actions written in JScript or Visual Basic, Scripting Edition (VBScript) can call an optional function.</span></span> <span data-ttu-id="ea8a5-106">Estas funciones deben devolver uno de los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-106">These functions must return one of the values shown in the following table.</span></span>



| <span data-ttu-id="ea8a5-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea8a5-107">Return value</span></span>              | <span data-ttu-id="ea8a5-108">Value</span><span class="sxs-lookup"><span data-stu-id="ea8a5-108">Value</span></span>        | <span data-ttu-id="ea8a5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea8a5-109">Description</span></span>                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8a5-110">msiDoActionStatusNoAction</span><span class="sxs-lookup"><span data-stu-id="ea8a5-110">msiDoActionStatusNoAction</span></span> | <span data-ttu-id="ea8a5-111">0</span><span class="sxs-lookup"><span data-stu-id="ea8a5-111">0</span></span>            | <span data-ttu-id="ea8a5-112">Acción no ejecutada.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-112">Action not executed.</span></span>                                                                                       |
| <span data-ttu-id="ea8a5-113">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="ea8a5-113">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="ea8a5-114">IDOK = 1</span><span class="sxs-lookup"><span data-stu-id="ea8a5-114">IDOK = 1</span></span>     | <span data-ttu-id="ea8a5-115">Acción completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-115">Action completed successfully.</span></span>                                                                             |
| <span data-ttu-id="ea8a5-116">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="ea8a5-116">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="ea8a5-117">IDCANCEL = 2</span><span class="sxs-lookup"><span data-stu-id="ea8a5-117">IDCANCEL = 2</span></span> | <span data-ttu-id="ea8a5-118">Finalización prematura por usuario.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-118">Premature termination by user.</span></span>                                                                             |
| <span data-ttu-id="ea8a5-119">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="ea8a5-119">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="ea8a5-120">IDABORT = 3</span><span class="sxs-lookup"><span data-stu-id="ea8a5-120">IDABORT = 3</span></span>  | <span data-ttu-id="ea8a5-121">Error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-121">Unrecoverable error.</span></span> <span data-ttu-id="ea8a5-122">Se devuelve si se produce un error durante el análisis o la ejecución de JScript o VBScript.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-122">Returned if there is an error during parsing or execution of the JScript or VBScript.</span></span> |
| <span data-ttu-id="ea8a5-123">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="ea8a5-123">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="ea8a5-124">IDRETRY = 4</span><span class="sxs-lookup"><span data-stu-id="ea8a5-124">IDRETRY = 4</span></span>  | <span data-ttu-id="ea8a5-125">Secuencia suspendida que se reanudará más adelante.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-125">Suspended sequence to be resumed later.</span></span>                                                                    |
| <span data-ttu-id="ea8a5-126">msiDoActionStatusFinished</span><span class="sxs-lookup"><span data-stu-id="ea8a5-126">msiDoActionStatusFinished</span></span> | <span data-ttu-id="ea8a5-127">IDIGNORE = 5</span><span class="sxs-lookup"><span data-stu-id="ea8a5-127">IDIGNORE = 5</span></span> | <span data-ttu-id="ea8a5-128">Omitir las acciones restantes.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-128">Skip remaining actions.</span></span> <span data-ttu-id="ea8a5-129">No es un error.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-129">Not an error.</span></span>                                                                      |



 

<span data-ttu-id="ea8a5-130">Tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-130">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="ea8a5-131">Por ejemplo, si el valor devuelto de la acción aparece como 1 (uno) en el archivo de registro, significa que la acción devolvió msiDoActionStatusSuccess.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-131">For example, if the action return value appears as 1 (one) in the log file, this means that the action returned msiDoActionStatusSuccess.</span></span> <span data-ttu-id="ea8a5-132">Para obtener más información sobre esta traducción, consulte [registro de valores devueltos de acciones](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ea8a5-132">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="ea8a5-133">Para devolver un valor distinto de Success desde una acción personalizada de script, debe usar un destino de función para la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-133">To return a value other than success from a script custom action, you must use a function target for the custom action.</span></span> <span data-ttu-id="ea8a5-134">La función de destino se especifica en la columna de destino de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="ea8a5-134">The target function is specified in the Target column of the [CustomAction Table](customaction-table.md).</span></span>

<span data-ttu-id="ea8a5-135">En el ejemplo de script siguiente se muestra cómo devolver Success o Failure desde una acción personalizada de VBScript.</span><span class="sxs-lookup"><span data-stu-id="ea8a5-135">The following script example shows you how to return success or failure from a VBScript custom action.</span></span>


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



<span data-ttu-id="ea8a5-136">Si este VBScript se incrustó en la [tabla binaria](binary-table.md) del paquete de instalación como MyCA.vbs, la entrada de la [tabla CustomAction](customaction-table.md) del script sería la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ea8a5-136">If this VBScript were embedded in the [Binary table](binary-table.md) of the installation package as MyCA.vbs, the [CustomAction Table](customaction-table.md) entry for the script would be the following:</span></span>



| <span data-ttu-id="ea8a5-137">Acción</span><span class="sxs-lookup"><span data-stu-id="ea8a5-137">Action</span></span>         | <span data-ttu-id="ea8a5-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea8a5-138">Type</span></span> | <span data-ttu-id="ea8a5-139">Source</span><span class="sxs-lookup"><span data-stu-id="ea8a5-139">Source</span></span>   | <span data-ttu-id="ea8a5-140">Destino</span><span class="sxs-lookup"><span data-stu-id="ea8a5-140">Target</span></span>       |
|----------------|------|----------|--------------|
| <span data-ttu-id="ea8a5-141">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="ea8a5-141">MyCustomAction</span></span> | <span data-ttu-id="ea8a5-142">6</span><span class="sxs-lookup"><span data-stu-id="ea8a5-142">6</span></span>    | <span data-ttu-id="ea8a5-143">MyCA.vbs</span><span class="sxs-lookup"><span data-stu-id="ea8a5-143">MyCA.vbs</span></span> | <span data-ttu-id="ea8a5-144">MyVBScriptCA</span><span class="sxs-lookup"><span data-stu-id="ea8a5-144">MyVBScriptCA</span></span> |



 

 

 



