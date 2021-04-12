---
description: 'Más información acerca de: JetGetTableIndexInfo (función)'
title: Función JetGetTableIndexInfo
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 904391218fbd073cd273655ce74fdec116b6a22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279394"
---
# <a name="jetgettableindexinfo-function"></a><span data-ttu-id="c67a3-103">Función JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c67a3-103">JetGetTableIndexInfo Function</span></span>


<span data-ttu-id="c67a3-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c67a3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableindexinfo-function"></a><span data-ttu-id="c67a3-105">Función JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c67a3-105">JetGetTableIndexInfo Function</span></span>

<span data-ttu-id="c67a3-106">La función **JetGetTableIndexInfo** recupera información acerca de un índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-106">The **JetGetTableIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="c67a3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c67a3-107">Parameters</span></span>

<span data-ttu-id="c67a3-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c67a3-108">*sesid*</span></span>

<span data-ttu-id="c67a3-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="c67a3-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="c67a3-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="c67a3-110">*tableid*</span></span>

<span data-ttu-id="c67a3-111">La tabla de base de datos que contiene el índice que contiene la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="c67a3-111">The database table that contains the index that holds the needed information.</span></span>

<span data-ttu-id="c67a3-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="c67a3-112">*szIndexName*</span></span>

<span data-ttu-id="c67a3-113">Nombre del índice que contiene la información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c67a3-113">The name of the index that contains information that will be retrieved.</span></span>

<span data-ttu-id="c67a3-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="c67a3-114">*pvResult*</span></span>

<span data-ttu-id="c67a3-115">Puntero a un búfer que recibirá la información.</span><span class="sxs-lookup"><span data-stu-id="c67a3-115">Pointer to a buffer which will receive the information.</span></span> <span data-ttu-id="c67a3-116">El búfer debe estar alineado para contener el tipo necesario.</span><span class="sxs-lookup"><span data-stu-id="c67a3-116">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="c67a3-117">El tipo de búfer depende del parámetro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="c67a3-117">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="c67a3-118">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="c67a3-118">*cbResult*</span></span>

<span data-ttu-id="c67a3-119">Tamaño, en bytes, del búfer pasado en el parámetro *pvResult* .</span><span class="sxs-lookup"><span data-stu-id="c67a3-119">The size, in bytes, of the buffer passed in the *pvResult* parameter.</span></span>

<span data-ttu-id="c67a3-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="c67a3-120">*InfoLevel*</span></span>

<span data-ttu-id="c67a3-121">Especifica la información que se almacenará en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="c67a3-121">Specifies which information will be stored in *pvResult*.</span></span> <span data-ttu-id="c67a3-122">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="c67a3-122">The valid values are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c67a3-123">Value</span><span class="sxs-lookup"><span data-stu-id="c67a3-123">Value</span></span></p></th>
<th><p><span data-ttu-id="c67a3-124">Significado</span><span class="sxs-lookup"><span data-stu-id="c67a3-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-125">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="c67a3-125">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="c67a3-126"><em>pvResult</em> se interpreta como una estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="c67a3-126"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="c67a3-127">Si se ejecuta correctamente, la estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recibe información sobre el índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-127">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="c67a3-128">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-128">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-129">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="c67a3-129">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="c67a3-130"><em>pvResult</em> se interpreta como un LCID.</span><span class="sxs-lookup"><span data-stu-id="c67a3-130"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="c67a3-131">Si se ejecuta correctamente, el LCID contiene el identificador de configuración regional del índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-131">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="c67a3-132">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-132">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-133">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="c67a3-133">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="c67a3-134"><em>pvResult</em> se interpreta como una estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="c67a3-134"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="c67a3-135">Si se ejecuta correctamente, la estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recibe información sobre el índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-135">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="c67a3-136">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-136">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-137">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="c67a3-137">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="c67a3-138">JET_IdxInfoOLC está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="c67a3-138">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-139">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="c67a3-139">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="c67a3-140">JET_IdxInfoResetOLC está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="c67a3-140">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-141">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="c67a3-141">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="c67a3-142"><em>pvResult</em> se interpreta como ulong.</span><span class="sxs-lookup"><span data-stu-id="c67a3-142"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="c67a3-143">Si se ejecuta correctamente, ULONG contiene el uso de espacio del índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-143">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="c67a3-144">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-144">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-145">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="c67a3-145">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="c67a3-146">JET_IdxInfoSysTabCursor está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="c67a3-146">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-147">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="c67a3-147">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="c67a3-148">JET_IdxInfoLangid está en desuso.</span><span class="sxs-lookup"><span data-stu-id="c67a3-148">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="c67a3-149">En su lugar, use JET_IdxInfoLCID y la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</span><span class="sxs-lookup"><span data-stu-id="c67a3-149">Use JET_IdxInfoLCID instead, and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-150">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="c67a3-150">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="c67a3-151"><em>pvResult</em> se interpreta como ulong.</span><span class="sxs-lookup"><span data-stu-id="c67a3-151"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="c67a3-152">Si se ejecuta correctamente, ULONG contiene el recuento de índices de la tabla especificada.</span><span class="sxs-lookup"><span data-stu-id="c67a3-152">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="c67a3-153"><em>szIndexName</em> se omite.</span><span class="sxs-lookup"><span data-stu-id="c67a3-153"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="c67a3-154">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-154">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-155">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="c67a3-155">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="c67a3-156"><em>pvResult</em> se interpreta como un USHORT.</span><span class="sxs-lookup"><span data-stu-id="c67a3-156"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="c67a3-157">Si se ejecuta correctamente, USHORT contiene el valor de <em>cbVarSegMac</em> que se usa cuando se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-157">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="c67a3-158">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbVarSegMac</em>.</span><span class="sxs-lookup"><span data-stu-id="c67a3-158">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="c67a3-159">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-160">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="c67a3-160">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="c67a3-161"><em>pvResult</em> se interpreta como <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="c67a3-161"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="c67a3-162">Si se ejecuta correctamente, la estructura de <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> recibe información sobre el índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-162">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="c67a3-163">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-163">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-164">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="c67a3-164">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="c67a3-165"><em>pvResult</em> se interpreta como un USHORT.</span><span class="sxs-lookup"><span data-stu-id="c67a3-165"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="c67a3-166">Si se ejecuta correctamente, USHORT contiene el valor de cbKeyMost que se usa cuando se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-166">On success, the USHORT holds the value of cbKeyMost used when the index was created.</span></span> <span data-ttu-id="c67a3-167">Vea la <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura para obtener una descripción de cbKeyMost.</span><span class="sxs-lookup"><span data-stu-id="c67a3-167">See the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure for a description of cbKeyMost.</span></span> <span data-ttu-id="c67a3-168">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-168">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-169">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="c67a3-169">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="c67a3-170"><em>pvResult</em> se interpreta como una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="c67a3-170"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="c67a3-171">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="c67a3-172"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c67a3-172"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-173">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="c67a3-173">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="c67a3-174"><em>pvResult</em> se interpreta como una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="c67a3-174"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="c67a3-175">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="c67a3-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c67a3-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c67a3-177">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c67a3-177">Return Value</span></span>

<span data-ttu-id="c67a3-178">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="c67a3-178">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c67a3-179">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c67a3-179">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c67a3-180">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c67a3-180">Return code</span></span></p></th>
<th><p><span data-ttu-id="c67a3-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="c67a3-181">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-182">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c67a3-182">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c67a3-183">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c67a3-183">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-184">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="c67a3-184">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="c67a3-185">No se encuentra el índice especificado en la tabla especificada.</span><span class="sxs-lookup"><span data-stu-id="c67a3-185">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-186">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="c67a3-186">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="c67a3-187">El búfer pasado como <em>pvResult</em> era demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="c67a3-187">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="c67a3-188">El contenido del búfer no está definido.</span><span class="sxs-lookup"><span data-stu-id="c67a3-188">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="c67a3-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c67a3-189">Remarks</span></span>

<span data-ttu-id="c67a3-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) y **JetGetTableIndexInfo** recuperan la misma información sobre un índice.</span><span class="sxs-lookup"><span data-stu-id="c67a3-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) and **JetGetTableIndexInfo** retrieve identical information about an index.</span></span> <span data-ttu-id="c67a3-191">La diferencia radica en cómo se especifica la tabla.</span><span class="sxs-lookup"><span data-stu-id="c67a3-191">The difference is in how the table is specified.</span></span> <span data-ttu-id="c67a3-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) espera una base de datos (*DBID*) y el nombre de una tabla (*SzTableName*), mientras que **JetGetTableIndexInfo** espera un identificador de tabla (*TABLEID*).</span><span class="sxs-lookup"><span data-stu-id="c67a3-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) expects a database (*dbid*) and name of a table (*szTableName*), while **JetGetTableIndexInfo** expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="c67a3-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c67a3-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-194"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c67a3-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c67a3-195">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c67a3-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c67a3-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c67a3-197">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c67a3-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c67a3-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c67a3-199">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c67a3-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-200"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="c67a3-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c67a3-201">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c67a3-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c67a3-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c67a3-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c67a3-203">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c67a3-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c67a3-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c67a3-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c67a3-205">Se implementa como <strong>JetGetTableIndexInfoW</strong> (Unicode) y <strong>JetGetTableIndexInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c67a3-205">Implemented as <strong>JetGetTableIndexInfoW</strong> (Unicode) and <strong>JetGetTableIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c67a3-206">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c67a3-206">See Also</span></span>

[<span data-ttu-id="c67a3-207">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c67a3-207">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="c67a3-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c67a3-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c67a3-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c67a3-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c67a3-210">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c67a3-210">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c67a3-211">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c67a3-211">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c67a3-212">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="c67a3-212">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="c67a3-213">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="c67a3-213">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="c67a3-214">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c67a3-214">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)
