---
description: Se crea un objeto SWbemMethod. Parameters y se proporciona con datos mediante el método de proveedor que se está ejecutando.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Analizar objetos Parameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361378"
---
# <a name="parsing-outparameters-objects"></a><span data-ttu-id="bdacf-103">Analizar objetos Parameters</span><span class="sxs-lookup"><span data-stu-id="bdacf-103">Parsing OutParameters Objects</span></span>

<span data-ttu-id="bdacf-104">Se crea un objeto [**SWbemMethod. Parameters**](swbemmethod-outparameters.md) y se proporciona con datos mediante el método de proveedor que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="bdacf-104">A [**SWbemMethod.OutParameters**](swbemmethod-outparameters.md) object is created and supplied with data by the provider method that is executing.</span></span> <span data-ttu-id="bdacf-105">Las propiedades del objeto **Parameters** son específicas del método llamado.</span><span class="sxs-lookup"><span data-stu-id="bdacf-105">Properties of the **OutParameters** object are specific to the method called.</span></span> <span data-ttu-id="bdacf-106">Por ejemplo, en el script siguiente, *SD* (incluido en *outParam*) es el parámetro de salida definido para el método **\_ \_ SystemSecurity.** .</span><span class="sxs-lookup"><span data-stu-id="bdacf-106">For example, in the script below, *SD* (contained in *outParam*) is the output parameter defined for the **\_\_SystemSecurity.GetSD** method.</span></span> <span data-ttu-id="bdacf-107">La propiedad **ReturnValue** es una propiedad genérica disponible para todos los objetos **Parameters** que contienen el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="bdacf-107">The **ReturnValue** property is a generic property available for all **OutParameters** objects which contain the result of the operation.</span></span>

<span data-ttu-id="bdacf-108">En el ejemplo de código siguiente se muestra cómo obtener los parámetros de salida de la ejecución [**del método obtenido en la clase**](--systemsecurity-getsd.md) [**\_ \_ SystemSecurity**](--systemsecurity.md) para el sistema local.</span><span class="sxs-lookup"><span data-stu-id="bdacf-108">The following code example illustrates obtaining output parameters from executing the [**GetSD**](--systemsecurity-getsd.md) method in class [**\_\_SystemSecurity**](--systemsecurity.md) for the local system.</span></span>


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



<span data-ttu-id="bdacf-109">Para obtener más información, consulte [**SWbemMethod. Parameters**](swbemmethod-inparameters.md).</span><span class="sxs-lookup"><span data-stu-id="bdacf-109">For more information, see [**SWbemMethod.InParameters**](swbemmethod-inparameters.md).</span></span>

 

 



