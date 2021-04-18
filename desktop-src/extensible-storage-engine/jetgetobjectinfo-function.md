---
description: 'Más información acerca de: JetGetObjectInfo (función)'
title: Función JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716164"
---
# <a name="jetgetobjectinfo-function"></a><span data-ttu-id="a5f82-103">Función JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="a5f82-103">JetGetObjectInfo Function</span></span>


<span data-ttu-id="a5f82-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a5f82-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetobjectinfo-function"></a><span data-ttu-id="a5f82-105">Función JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="a5f82-105">JetGetObjectInfo Function</span></span>

<span data-ttu-id="a5f82-106">La función **JetGetObjectInfo** recupera información acerca de los objetos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a5f82-106">The **JetGetObjectInfo** function retrieves information about database objects.</span></span> <span data-ttu-id="a5f82-107">Actualmente, solo se admiten tablas.</span><span class="sxs-lookup"><span data-stu-id="a5f82-107">Currently, only tables are supported.</span></span> <span data-ttu-id="a5f82-108">[JetGetTableInfo](./jetgettableinfo-function.md) se puede usar para obtener más información que **JetGetObjectInfo**.</span><span class="sxs-lookup"><span data-stu-id="a5f82-108">[JetGetTableInfo](./jetgettableinfo-function.md) can be used to fetch more information than **JetGetObjectInfo**.</span></span>

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="a5f82-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5f82-109">Parameters</span></span>

<span data-ttu-id="a5f82-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a5f82-110">*sesid*</span></span>

<span data-ttu-id="a5f82-111">Contexto de sesión de base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a5f82-111">The database session context to use.</span></span>

<span data-ttu-id="a5f82-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="a5f82-112">*dbid*</span></span>

<span data-ttu-id="a5f82-113">Base de datos de la que se recupera la información.</span><span class="sxs-lookup"><span data-stu-id="a5f82-113">The database from which the information is retrieved.</span></span>

<span data-ttu-id="a5f82-114">*objtyp*</span><span class="sxs-lookup"><span data-stu-id="a5f82-114">*objtyp*</span></span>

<span data-ttu-id="a5f82-115">Objetos que contienen información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="a5f82-115">The objects that contain information to be retrieved.</span></span> <span data-ttu-id="a5f82-116">Actualmente, solo se admiten JET_objtypNil y JET_objtypTable, ambos de los cuales se comportan exactamente igual.</span><span class="sxs-lookup"><span data-stu-id="a5f82-116">Currently, only JET_objtypNil and JET_objtypTable are supported, both of which behave identically.</span></span> <span data-ttu-id="a5f82-117">Solo se recuperarán las tablas.</span><span class="sxs-lookup"><span data-stu-id="a5f82-117">Only tables will be retrieved.</span></span>

<span data-ttu-id="a5f82-118">*szContainerName*</span><span class="sxs-lookup"><span data-stu-id="a5f82-118">*szContainerName*</span></span>

<span data-ttu-id="a5f82-119">Este parámetro está reservado para un uso futuro y pasa **null**.</span><span class="sxs-lookup"><span data-stu-id="a5f82-119">This parameter is reserved for future use and passes **NULL**.</span></span> <span data-ttu-id="a5f82-120">Nombre de los tipos de objetos sobre los que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="a5f82-120">The name of the types of objects about which to retrieve information.</span></span>

<span data-ttu-id="a5f82-121">*szObjectName*</span><span class="sxs-lookup"><span data-stu-id="a5f82-121">*szObjectName*</span></span>

<span data-ttu-id="a5f82-122">Nombre del objeto que contiene la información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="a5f82-122">The name of the object that contains information to retrieve.</span></span> <span data-ttu-id="a5f82-123">Cuando *InfoLevel* usa las opciones JET_ObjInfoList o JET_ObjInfoListNoStats para recuperar una lista de todos los objetos, este valor debe ser **null** o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="a5f82-123">When *InfoLevel* uses the JET_ObjInfoList or JET_ObjInfoListNoStats options to retrieve a list of all objects, this value should be **NULL** or an empty string.</span></span>

<span data-ttu-id="a5f82-124">Actualmente solo se admiten nombres de tabla.</span><span class="sxs-lookup"><span data-stu-id="a5f82-124">Only table names are currently supported.</span></span>

<span data-ttu-id="a5f82-125">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="a5f82-125">*pvResult*</span></span>

<span data-ttu-id="a5f82-126">Puntero a un búfer que recibe la información especificada.</span><span class="sxs-lookup"><span data-stu-id="a5f82-126">Pointer to a buffer which receives the specified information.</span></span>

<span data-ttu-id="a5f82-127">El tamaño del búfer, en bytes, se pasa en *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="a5f82-127">The size of the buffer, in bytes, is passed in *cbMax*.</span></span> <span data-ttu-id="a5f82-128">En caso de error, el contenido de *pvResult* no está definido.</span><span class="sxs-lookup"><span data-stu-id="a5f82-128">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="a5f82-129">La información que se almacena en *pvResult* depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="a5f82-129">The information that is stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="a5f82-130">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="a5f82-130">*cbMax*</span></span>

<span data-ttu-id="a5f82-131">Tamaño, en bytes, del búfer pasado en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="a5f82-131">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="a5f82-132">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="a5f82-132">*InfoLevel*</span></span>

<span data-ttu-id="a5f82-133">Especifica el tipo de información que se va a recuperar para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="a5f82-133">Specifies which type of information to retrieve for the specified object.</span></span> <span data-ttu-id="a5f82-134">Afecta al modo en que se interpreta *pvResult* .</span><span class="sxs-lookup"><span data-stu-id="a5f82-134">It affects how *pvResult* is interpreted.</span></span>

<span data-ttu-id="a5f82-135">Las siguientes opciones están disponibles para establecerse para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="a5f82-135">The following options are available to set for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5f82-136">Value</span><span class="sxs-lookup"><span data-stu-id="a5f82-136">Value</span></span></p></th>
<th><p><span data-ttu-id="a5f82-137">Significado</span><span class="sxs-lookup"><span data-stu-id="a5f82-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-138">JET_ObjInfo</span><span class="sxs-lookup"><span data-stu-id="a5f82-138">JET_ObjInfo</span></span></p></td>
<td><p><span data-ttu-id="a5f82-139"><em>pvResult</em> se interpreta como una estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="a5f82-139"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span></p>
<p><span data-ttu-id="a5f82-140">La estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> se rellena con información relacionada con el objeto denominado en <em>szObjectName</em>.</span><span class="sxs-lookup"><span data-stu-id="a5f82-140">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="a5f82-141">Si el autor de la llamada no desea conocer el número de registros y páginas del objeto, considere la posibilidad de usar JET_ObjInfoNoStats nivel de información, que podría ser más rápido, ya que no se incluyen las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="a5f82-141">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoNoStats information level, which might be faster since statistics are not included.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-142">JET_ObjInfoList</span><span class="sxs-lookup"><span data-stu-id="a5f82-142">JET_ObjInfoList</span></span></p></td>
<td><p><span data-ttu-id="a5f82-143"><em>pvResult</em> se interpreta como una estructura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="a5f82-143"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="a5f82-144">Se recupera información sobre todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="a5f82-144">Information about all objects is retrieved.</span></span> <span data-ttu-id="a5f82-145">Se creará una tabla temporal y la información necesaria para recorrer la tabla temporal se describe en la estructura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="a5f82-145">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="a5f82-146">Para obtener más información, vea <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="a5f82-146">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="a5f82-147">Si el autor de la llamada no desea conocer el número de registros y páginas del objeto, considere la posibilidad de usar JET_ObjInfoListNoStats, lo que podría ser más rápido.</span><span class="sxs-lookup"><span data-stu-id="a5f82-147">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoListNoStats, which might be faster.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-148">JET_ObjInfoListACM</span><span class="sxs-lookup"><span data-stu-id="a5f82-148">JET_ObjInfoListACM</span></span></p></td>
<td><p><span data-ttu-id="a5f82-149">En desuso y no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="a5f82-149">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-150">JET_ObjInfoListNoStats</span><span class="sxs-lookup"><span data-stu-id="a5f82-150">JET_ObjInfoListNoStats</span></span></p></td>
<td><p><span data-ttu-id="a5f82-151"><em>pvResult</em> se interpreta como una estructura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="a5f82-151"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="a5f82-152">Se recupera información sobre todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="a5f82-152">Information about all objects is retrieved.</span></span> <span data-ttu-id="a5f82-153">Se creará una tabla temporal y la información necesaria para recorrer la tabla temporal se describe en la estructura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="a5f82-153">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="a5f82-154">Para obtener más información, vea <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="a5f82-154">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="a5f82-155">JET_ObjInfoListNoStats es idéntica a JET_ObjInfoList, salvo que las columnas que informan del número de registros (<em>columnidcRecord</em>) y las páginas (<em>columnidcPage</em>) no se actualizarán.</span><span class="sxs-lookup"><span data-stu-id="a5f82-155">JET_ObjInfoListNoStats is identical to JET_ObjInfoList, except that the columns that report the number of records (<em>columnidcRecord</em>) and pages (<em>columnidcPage</em>) will not be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-156">JET_ObjInfoMax</span><span class="sxs-lookup"><span data-stu-id="a5f82-156">JET_ObjInfoMax</span></span></p></td>
<td><p><span data-ttu-id="a5f82-157"><em>pvResult</em> se interpreta como <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="a5f82-157"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="a5f82-158">El tamaño máximo del objeto está en páginas.</span><span class="sxs-lookup"><span data-stu-id="a5f82-158">The maximum size of the object is in pages.</span></span> <span data-ttu-id="a5f82-159">Actualmente solo se devolverán las tablas.</span><span class="sxs-lookup"><span data-stu-id="a5f82-159">Currently only tables will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-160">JET_ObjInfoNoStats</span><span class="sxs-lookup"><span data-stu-id="a5f82-160">JET_ObjInfoNoStats</span></span></p></td>
<td><p><span data-ttu-id="a5f82-161"><em>pvResult</em> se interpreta como <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="a5f82-161"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="a5f82-162">Solo se recuperará información sobre el objeto proporcionado en <em>szObjectName</em> .</span><span class="sxs-lookup"><span data-stu-id="a5f82-162">Information about only the object given in <em>szObjectName</em> will be retrieved.</span></span></p>
<p><span data-ttu-id="a5f82-163">La estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> se rellenará con información relativa al objeto denominado en <em>szObjectName</em>.</span><span class="sxs-lookup"><span data-stu-id="a5f82-163">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure will be populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="a5f82-164">JET_ObjInfoNoStats es idéntica a JET_ObjInfo, salvo que los campos que informan del número de registros y páginas se establecen en cero.</span><span class="sxs-lookup"><span data-stu-id="a5f82-164">JET_ObjInfoNoStats is identical to JET_ObjInfo, except that the fields that report the number of records and pages are set to zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-165">JET_ObjInfoRulesLoaded</span><span class="sxs-lookup"><span data-stu-id="a5f82-165">JET_ObjInfoRulesLoaded</span></span></p></td>
<td><p><span data-ttu-id="a5f82-166">En desuso y no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="a5f82-166">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-167">JET_ObjInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="a5f82-167">JET_ObjInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="a5f82-168">En desuso y no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="a5f82-168">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-169">JET_ObjInfoSysTabReadOnly</span><span class="sxs-lookup"><span data-stu-id="a5f82-169">JET_ObjInfoSysTabReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a5f82-170">En desuso y no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="a5f82-170">Deprecated and not currently supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a5f82-171">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5f82-171">Return Value</span></span>

<span data-ttu-id="a5f82-172">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="a5f82-172">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a5f82-173">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a5f82-173">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5f82-174">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a5f82-174">Return code</span></span></p></th>
<th><p><span data-ttu-id="a5f82-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5f82-175">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-176">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a5f82-176">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a5f82-177">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a5f82-177">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="a5f82-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="a5f82-179">El tamaño del búfer proporcionado en <em>cbMax</em> era demasiado pequeño para contener la información deseada.</span><span class="sxs-lookup"><span data-stu-id="a5f82-179">The size of the buffer given in <em>cbMax</em> was too small to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-180">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="a5f82-180">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="a5f82-181">Se proporcionó un nombre no válido en <em>szObjectName</em> o <em>szContainerName</em>.</span><span class="sxs-lookup"><span data-stu-id="a5f82-181">An invalid name was given in <em>szObjectName</em> or <em>szContainerName</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-182">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a5f82-182">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a5f82-183">Se proporcionó un parámetro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="a5f82-183">A bad parameter was given.</span></span> <span data-ttu-id="a5f82-184">Es posible que se haya pasado un nivel no válido a <em>InfoLevel</em>.</span><span class="sxs-lookup"><span data-stu-id="a5f82-184">It is possible that a bad level was passed in to <em>InfoLevel</em>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="a5f82-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5f82-185">Remarks</span></span>

<span data-ttu-id="a5f82-186">Si **JetGetObjectInfo** crea correctamente una tabla temporal (por ejemplo, JET_ObjInfoList o JET_ObjInfoNoStats), el autor de la llamada es responsable de cerrar la tabla temporal con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="a5f82-186">If **JetGetObjectInfo** successfully creates a temporary table (for example, JET_ObjInfoList or JET_ObjInfoNoStats), the caller is responsible for closing the temporary table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="a5f82-187">**JetGetObjectInfo** actualmente solo admite la recuperación de información sobre tablas.</span><span class="sxs-lookup"><span data-stu-id="a5f82-187">**JetGetObjectInfo** currently only supports retrieving information about tables.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a5f82-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5f82-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-189"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a5f82-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f82-190">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a5f82-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a5f82-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f82-192">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a5f82-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a5f82-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f82-194">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a5f82-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-195"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="a5f82-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f82-196">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a5f82-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f82-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a5f82-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f82-198">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a5f82-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f82-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a5f82-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f82-200">Se implementa como <strong>JetGetObjectInfoW</strong> (Unicode) y <strong>JetGetObjectInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a5f82-200">Implemented as <strong>JetGetObjectInfoW</strong> (Unicode) and <strong>JetGetObjectInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a5f82-201">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a5f82-201">See Also</span></span>

[<span data-ttu-id="a5f82-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a5f82-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a5f82-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a5f82-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a5f82-204">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="a5f82-204">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="a5f82-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a5f82-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a5f82-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a5f82-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a5f82-207">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="a5f82-207">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="a5f82-208">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="a5f82-208">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="a5f82-209">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="a5f82-209">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="a5f82-210">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="a5f82-210">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
