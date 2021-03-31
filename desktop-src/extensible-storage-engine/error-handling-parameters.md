---
description: 'Más información sobre: parámetros de control de errores'
title: Parámetros de control de errores
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913353"
---
# <a name="error-handling-parameters"></a><span data-ttu-id="534fc-103">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="534fc-103">Error Handling Parameters</span></span>


<span data-ttu-id="534fc-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="534fc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-parameters"></a><span data-ttu-id="534fc-105">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="534fc-105">Error Handling Parameters</span></span>

<span data-ttu-id="534fc-106">Este tema contiene los parámetros que se usan para el control de errores.</span><span class="sxs-lookup"><span data-stu-id="534fc-106">This topic contains parameters that are used for error handling.</span></span>

<span data-ttu-id="534fc-107">*JET_paramErrorToString* 70</span><span class="sxs-lookup"><span data-stu-id="534fc-107">*JET_paramErrorToString* 70</span></span>  

<span data-ttu-id="534fc-108">Este parámetro se puede utilizar para convertir un [JET_ERR](./jet-err.md) en una cadena.</span><span class="sxs-lookup"><span data-stu-id="534fc-108">This parameter can be used to convert a [JET_ERR](./jet-err.md) into a string.</span></span> <span data-ttu-id="534fc-109">Esto se hace mediante una llamada especial a [JetGetSystemParameter](./jetgetsystemparameter-function.md) , donde el búfer de salida entero contiene el valor [JET_ERR](./jet-err.md) que se va a convertir (como parámetro de entrada) y el búfer de salida de la cadena devuelve la cadena de error coincidente.</span><span class="sxs-lookup"><span data-stu-id="534fc-109">This is done using a special call to [JetGetSystemParameter](./jetgetsystemparameter-function.md) where the integer output buffer contains the [JET_ERR](./jet-err.md) value to be converted (as an input parameter) and the string output buffer returns the matching error string.</span></span> <span data-ttu-id="534fc-110">La cadena tendrá un aspecto similar al siguiente: "JET_errSuccess, operación correcta".</span><span class="sxs-lookup"><span data-stu-id="534fc-110">The string will look something like this: "JET_errSuccess,Successful Operation".</span></span> <span data-ttu-id="534fc-111">La cadena se compone del nombre simbólico de la cadena, después una coma y, a continuación, una descripción de texto simple del error.</span><span class="sxs-lookup"><span data-stu-id="534fc-111">The string is composed of the symbolic name for the string, then a comma, and then a simple text description of the error.</span></span> <span data-ttu-id="534fc-112">La cadena de descripción puede contener a su vez comas.</span><span class="sxs-lookup"><span data-stu-id="534fc-112">The description string may itself contain commas.</span></span> <span data-ttu-id="534fc-113">Si no se reconoce el error, la cadena será "error desconocido, error desconocido".</span><span class="sxs-lookup"><span data-stu-id="534fc-113">If the error is not recognized then the string will be "Unknown Error,Unknown Error".</span></span>

<span data-ttu-id="534fc-114">**Nota:**  Este parámetro es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="534fc-114">**Note**  This parameter is read only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534fc-115">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="534fc-115">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="534fc-116">Especial</span><span class="sxs-lookup"><span data-stu-id="534fc-116">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-117">Escriba:</span><span class="sxs-lookup"><span data-stu-id="534fc-117">Type:</span></span></p></td>
<td><p><span data-ttu-id="534fc-118">Especial</span><span class="sxs-lookup"><span data-stu-id="534fc-118">Special</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-119">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="534fc-119">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="534fc-120">Especial</span><span class="sxs-lookup"><span data-stu-id="534fc-120">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-121">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="534fc-121">Scope:</span></span></p></td>
<td><p><span data-ttu-id="534fc-122">Global</span><span class="sxs-lookup"><span data-stu-id="534fc-122">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-123">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="534fc-123">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="534fc-124">No</span><span class="sxs-lookup"><span data-stu-id="534fc-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-125">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="534fc-125">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="534fc-126">No</span><span class="sxs-lookup"><span data-stu-id="534fc-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-127">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="534fc-127">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="534fc-128">No</span><span class="sxs-lookup"><span data-stu-id="534fc-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-129">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="534fc-129">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="534fc-130">No</span><span class="sxs-lookup"><span data-stu-id="534fc-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-131">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="534fc-131">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="534fc-132">No</span><span class="sxs-lookup"><span data-stu-id="534fc-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-133">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="534fc-133">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="534fc-134">No</span><span class="sxs-lookup"><span data-stu-id="534fc-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-135">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="534fc-135">Availability:</span></span></p></td>
<td><p><span data-ttu-id="534fc-136">All</span><span class="sxs-lookup"><span data-stu-id="534fc-136">All</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="534fc-137">*JET_paramExceptionAction*</span><span class="sxs-lookup"><span data-stu-id="534fc-137">*JET_paramExceptionAction*</span></span>  
<span data-ttu-id="534fc-138">98</span><span class="sxs-lookup"><span data-stu-id="534fc-138">98</span></span>  

<span data-ttu-id="534fc-139">Este parámetro controla lo que ocurre cuando se produce una excepción en el motor de base de datos o en el código al que llama el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="534fc-139">This parameter controls what happens when an exception is thrown by the database engine or code that is called by the database engine.</span></span> <span data-ttu-id="534fc-140">Cuando se establece en JET_ExceptionMsgBox, se producirá cualquier excepción en el filtro de excepciones no controladas de Windows.</span><span class="sxs-lookup"><span data-stu-id="534fc-140">When set to JET_ExceptionMsgBox, any exception will be thrown to the Windows unhandled exception filter.</span></span> <span data-ttu-id="534fc-141">Esto hará que la excepción se controle como un error de aplicación.</span><span class="sxs-lookup"><span data-stu-id="534fc-141">This will result in the exception being handled as an application failure.</span></span> <span data-ttu-id="534fc-142">La intención es evitar que el código de aplicación intente detectar erróneamente y omitir una excepción generada por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="534fc-142">The intent is to prevent application code from erroneously trying to catch and ignore an exception generated by the database engine.</span></span> <span data-ttu-id="534fc-143">Esto no se permite porque podrían producirse daños en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="534fc-143">This cannot be allowed because database corruption could occur.</span></span> <span data-ttu-id="534fc-144">Si la aplicación desea administrar correctamente estas excepciones, la protección se puede deshabilitar estableciendo este parámetro en JET_ExceptionNone.</span><span class="sxs-lookup"><span data-stu-id="534fc-144">If the application wishes to properly handle these exceptions then the protection can be disabled by setting this parameter to JET_ExceptionNone.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534fc-145">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="534fc-145">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="534fc-146">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="534fc-146">JET_ExceptionMsgBox</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-147">Escriba:</span><span class="sxs-lookup"><span data-stu-id="534fc-147">Type:</span></span></p></td>
<td><p><span data-ttu-id="534fc-148">Entero</span><span class="sxs-lookup"><span data-stu-id="534fc-148">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-149">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="534fc-149">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="534fc-150">JET_ExceptionMsgBox, JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="534fc-150">JET_ExceptionMsgBox, JET_ExceptionNone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-151">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="534fc-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="534fc-152">Global</span><span class="sxs-lookup"><span data-stu-id="534fc-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-153">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="534fc-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="534fc-154"><strong>Windows 2000, Windows XP y Windows Server 2003:  </strong>  No</span><span class="sxs-lookup"><span data-stu-id="534fc-154"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="534fc-155"><strong>Windows Vista:</strong>  ?</span><span class="sxs-lookup"><span data-stu-id="534fc-155"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-156">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="534fc-156">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="534fc-157"><strong>Windows 2000, Windows XP y Windows Server 2003:  </strong>  No</span><span class="sxs-lookup"><span data-stu-id="534fc-157"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="534fc-158"><strong>Windows Vista:</strong>  ?</span><span class="sxs-lookup"><span data-stu-id="534fc-158"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-159">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="534fc-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="534fc-160">No</span><span class="sxs-lookup"><span data-stu-id="534fc-160">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-161">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="534fc-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="534fc-162">Sí</span><span class="sxs-lookup"><span data-stu-id="534fc-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-163">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="534fc-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="534fc-164">No</span><span class="sxs-lookup"><span data-stu-id="534fc-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-165">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="534fc-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="534fc-166">No</span><span class="sxs-lookup"><span data-stu-id="534fc-166">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-167">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="534fc-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="534fc-168">All</span><span class="sxs-lookup"><span data-stu-id="534fc-168">All</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a><span data-ttu-id="534fc-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="534fc-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534fc-170"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="534fc-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="534fc-171">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="534fc-171">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534fc-172"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="534fc-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="534fc-173">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="534fc-173">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534fc-174"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="534fc-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="534fc-175">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="534fc-175">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a><span data-ttu-id="534fc-176">Consulte también</span><span class="sxs-lookup"><span data-stu-id="534fc-176">See Also</span></span>

[<span data-ttu-id="534fc-177">Constantes de control de errores</span><span class="sxs-lookup"><span data-stu-id="534fc-177">Error Handling Constants</span></span>](./error-handling-constants.md)  
[<span data-ttu-id="534fc-178">Códigos de error del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="534fc-178">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="534fc-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="534fc-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="534fc-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="534fc-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="534fc-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="534fc-181">JetInit</span></span>](./jetinit-function.md)
