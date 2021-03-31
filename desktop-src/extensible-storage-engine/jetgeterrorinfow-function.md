---
description: 'Más información acerca de: JetGetErrorInfoW (función)'
title: JetGetErrorInfoW función)
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104157281"
---
# <a name="jetgeterrorinfow-function"></a><span data-ttu-id="28d3b-103">JetGetErrorInfoW función)</span><span class="sxs-lookup"><span data-stu-id="28d3b-103">JetGetErrorInfoW Function</span></span>


<span data-ttu-id="28d3b-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="28d3b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgeterrorinfow-function"></a><span data-ttu-id="28d3b-105">JetGetErrorInfoW función)</span><span class="sxs-lookup"><span data-stu-id="28d3b-105">JetGetErrorInfoW Function</span></span>

<span data-ttu-id="28d3b-106">La función **JetGetErrorInfoW** BAS_ del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="28d3b-106">The **JetGetErrorInfoW** function BAS_ of the database engine.</span></span>

<span data-ttu-id="28d3b-107">Nota: esta documentación se basa en una versión preliminar del motor de almacenamiento extensible.</span><span class="sxs-lookup"><span data-stu-id="28d3b-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="28d3b-108">Esta información está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="28d3b-108">This information is subject to change.</span></span>

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a><span data-ttu-id="28d3b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28d3b-109">Parameters</span></span>

<span data-ttu-id="28d3b-110">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="28d3b-110">*pvContext*</span></span>

<span data-ttu-id="28d3b-111">El valor de contexto o error para el que se necesita la información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="28d3b-111">The context or error value for which the extended error information is needed.</span></span> <span data-ttu-id="28d3b-112">El valor que se pasa depende del valor del parámetro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="28d3b-112">The value passed in depends on the *InfoLevel* parameter value.</span></span>

<span data-ttu-id="28d3b-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="28d3b-113">*pvResult*</span></span>

<span data-ttu-id="28d3b-114">Un puntero a un búfer que recibirá la información.</span><span class="sxs-lookup"><span data-stu-id="28d3b-114">A pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="28d3b-115">El tipo del búfer depende del valor del parámetro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="28d3b-115">The type of the buffer depends on the *InfoLevel* parameter value.</span></span> <span data-ttu-id="28d3b-116">El autor de la llamada debe estar configurado para alinear el búfer adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="28d3b-116">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="28d3b-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="28d3b-117">*cbMax*</span></span>

<span data-ttu-id="28d3b-118">Tamaño máximo de la estructura *pvResult* que se pasa.</span><span class="sxs-lookup"><span data-stu-id="28d3b-118">The maximum size of the *pvResult* structure that is passed in.</span></span>

<span data-ttu-id="28d3b-119">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="28d3b-119">*InfoLevel*</span></span>

<span data-ttu-id="28d3b-120">El tipo de información que se recuperará para el contexto o la información de error se especifica mediante el parámetro *pvContext* .</span><span class="sxs-lookup"><span data-stu-id="28d3b-120">The type of information that will be retrieved for the error info/context is specified by the *pvContext* parameter.</span></span> <span data-ttu-id="28d3b-121">El formato de los datos que se almacenan en *pvResult* depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="28d3b-121">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="28d3b-122">En la tabla siguiente se enumeran los posibles valores para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="28d3b-122">The following table lists the possible values for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28d3b-123">Value</span><span class="sxs-lookup"><span data-stu-id="28d3b-123">Value</span></span></p></th>
<th><p><span data-ttu-id="28d3b-124">Significado</span><span class="sxs-lookup"><span data-stu-id="28d3b-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28d3b-125">JET_ErrorInfoSpecificErr</span><span class="sxs-lookup"><span data-stu-id="28d3b-125">JET_ErrorInfoSpecificErr</span></span></p></td>
<td><p><span data-ttu-id="28d3b-126"><em>pvContext</em> se interpreta como un <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error Code, <em>pvResult</em> se interpreta como un <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>y los campos de la estructura <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> se rellenan de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="28d3b-126"><em>pvContext</em> is interpreted as a <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error code, <em>pvResult</em> is interpreted as a <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, and the fields of the <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> structure are filled in appropriately.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28d3b-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="28d3b-127">*grbit*</span></span>

<span data-ttu-id="28d3b-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="28d3b-128">Reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="28d3b-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28d3b-129">Return Value</span></span>

<span data-ttu-id="28d3b-130">Esta función devuelve el tipo de datos [JET_ERR](./extensible-storage-engine-error-codes.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="28d3b-130">This function returns the [JET_ERR](./extensible-storage-engine-error-codes.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="28d3b-131">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="28d3b-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28d3b-132">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="28d3b-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="28d3b-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="28d3b-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28d3b-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="28d3b-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="28d3b-135">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="28d3b-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d3b-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="28d3b-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="28d3b-137">Uno de los parámetros proporcionados contiene un valor inesperado o contiene un valor que no tiene sentido cuando se combina con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="28d3b-137">One of the parameters provided contains an unexpected value or contains a value that does not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="28d3b-138">Esto puede ocurrir para <strong>JetGetErrorInfo</strong> cuando se produce lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="28d3b-138">This can happen for <strong>JetGetErrorInfo</strong> when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="28d3b-139">El valor del parámetro <em>InfoLevel</em> especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="28d3b-139">The specified <em>InfoLevel</em> parameter value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="28d3b-140">El valor de <em>grbit</em> especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="28d3b-140">The specified <em>grbit</em> value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="28d3b-141">El valor de <em>cbMax</em> del búfer del parámetro <em>pvResult</em> especificado es menor que el tamaño necesario para la salida de este parámetro <em>InfoLevel</em> .</span><span class="sxs-lookup"><span data-stu-id="28d3b-141">The specified <em>pvResult</em> parameter buffer’s <em>cbMax</em> value is less than the required size for output of this <em>InfoLevel</em> parameter.</span></span></p></li>
<li><p><span data-ttu-id="28d3b-142">En el caso de <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, el motor no conoce el valor de <a href="gg294092(v=exchg.10).md">JET_ERR</a> pasado.</span><span class="sxs-lookup"><span data-stu-id="28d3b-142">For <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, the <a href="gg294092(v=exchg.10).md">JET_ERR</a> value passed in is unknown to the engine.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28d3b-143">JET_errDisabledFunctionality</span><span class="sxs-lookup"><span data-stu-id="28d3b-143">JET_errDisabledFunctionality</span></span></p></td>
<td><p><span data-ttu-id="28d3b-144">Si esta SKU de Windows no admite esta función, se devolverá este error.</span><span class="sxs-lookup"><span data-stu-id="28d3b-144">If this SKU of windows doesn’t support this function, this error will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28d3b-145">Si se ejecuta correctamente, el búfer de salida adecuado para el contexto o valor de error solicitado se establecerá en la información de error extendida solicitada.</span><span class="sxs-lookup"><span data-stu-id="28d3b-145">On success, the output buffer that is appropriate for the requested error context/value will be set to the extended error info requested.</span></span>

<span data-ttu-id="28d3b-146">En caso de error, el estado de los búferes de salida será undefined.</span><span class="sxs-lookup"><span data-stu-id="28d3b-146">On failure, the state of the output buffers will be undefined.</span></span>

### <a name="remarks"></a><span data-ttu-id="28d3b-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28d3b-147">Remarks</span></span>

<span data-ttu-id="28d3b-148">La función [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) y [JET_ERRCAT](./jet-errcat.md) grupo de constantes contienen documentación sobre la información de error extendida que se devuelve para *InfoLevel* = JET_ErrorInfoSpecificErr.</span><span class="sxs-lookup"><span data-stu-id="28d3b-148">The [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) function and [JET_ERRCAT](./jet-errcat.md) group of constants contain documentation about the extended error information that is returned for *InfoLevel* = JET_ErrorInfoSpecificErr.</span></span>

### <a name="requirements"></a><span data-ttu-id="28d3b-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28d3b-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28d3b-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="28d3b-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="28d3b-151">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="28d3b-151">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d3b-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="28d3b-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="28d3b-153">Requiere Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="28d3b-153">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28d3b-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="28d3b-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="28d3b-155">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="28d3b-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d3b-156"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="28d3b-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="28d3b-157">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="28d3b-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28d3b-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="28d3b-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="28d3b-159">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="28d3b-159">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d3b-160"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="28d3b-160"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="28d3b-161">Nota: solo se implementa <strong>JetGetErrorInfoW</strong> (Unicode).</span><span class="sxs-lookup"><span data-stu-id="28d3b-161">Note: Only the <strong>JetGetErrorInfoW</strong> (Unicode) is implemented.</span></span> <span data-ttu-id="28d3b-162">Esta API no tiene una versión A (ANSI).</span><span class="sxs-lookup"><span data-stu-id="28d3b-162">This API does not have an A (ANSI) version.</span></span></p></td>
</tr>
</tbody>
</table>
