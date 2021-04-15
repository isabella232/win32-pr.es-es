---
description: 'Más información acerca de: JetGetIndexInfo (función)'
title: Función JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648519"
---
# <a name="jetgetindexinfo-function"></a><span data-ttu-id="0928b-103">Función JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="0928b-103">JetGetIndexInfo Function</span></span>


<span data-ttu-id="0928b-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0928b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetindexinfo-function"></a><span data-ttu-id="0928b-105">Función JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="0928b-105">JetGetIndexInfo Function</span></span>

<span data-ttu-id="0928b-106">La función **JetGetIndexInfo** recupera información acerca de un índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-106">The **JetGetIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="0928b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0928b-107">Parameters</span></span>

<span data-ttu-id="0928b-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0928b-108">*sesid*</span></span>

<span data-ttu-id="0928b-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="0928b-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="0928b-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="0928b-110">*dbid*</span></span>

<span data-ttu-id="0928b-111">Identificador de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="0928b-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="0928b-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="0928b-112">*szTableName*</span></span>

<span data-ttu-id="0928b-113">Nombre de la tabla que contiene el índice con la información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="0928b-113">The name of the table containing the index with the information to retrieve.</span></span>

<span data-ttu-id="0928b-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="0928b-114">*szIndexName*</span></span>

<span data-ttu-id="0928b-115">Nombre del índice con la información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="0928b-115">The name of the index with the information to retrieve.</span></span>

<span data-ttu-id="0928b-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="0928b-116">*pvResult*</span></span>

<span data-ttu-id="0928b-117">Puntero a un búfer que recibirá la información deseada.</span><span class="sxs-lookup"><span data-stu-id="0928b-117">Pointer to a buffer that will receive the desired information.</span></span> <span data-ttu-id="0928b-118">El búfer debe estar alineado para contener el tipo necesario.</span><span class="sxs-lookup"><span data-stu-id="0928b-118">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="0928b-119">El tipo de búfer depende del parámetro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="0928b-119">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="0928b-120">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="0928b-120">*cbResult*</span></span>

<span data-ttu-id="0928b-121">Tamaño, en bytes, del búfer pasado como *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="0928b-121">The size, in bytes, of the buffer passed as *pvResult*.</span></span>

<span data-ttu-id="0928b-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="0928b-122">*InfoLevel*</span></span>

<span data-ttu-id="0928b-123">La información que se almacenará en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="0928b-123">The information that will be stored in *pvResult*.</span></span> <span data-ttu-id="0928b-124">Se pueden usar las siguientes opciones para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="0928b-124">The following options can be used for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0928b-125">Value</span><span class="sxs-lookup"><span data-stu-id="0928b-125">Value</span></span></p></th>
<th><p><span data-ttu-id="0928b-126">Significado</span><span class="sxs-lookup"><span data-stu-id="0928b-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0928b-127">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="0928b-127">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="0928b-128"><em>pvResult</em> se interpreta como una estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="0928b-128"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="0928b-129">Si se ejecuta correctamente, la estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recibe información sobre el índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-129">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="0928b-130">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-130">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-131">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="0928b-131">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="0928b-132"><em>pvResult</em> se interpreta como ulong.</span><span class="sxs-lookup"><span data-stu-id="0928b-132"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="0928b-133">Si se ejecuta correctamente, ULONG contiene el recuento de índices de la tabla especificada.</span><span class="sxs-lookup"><span data-stu-id="0928b-133">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="0928b-134"><em>szIndexName</em> se omite.</span><span class="sxs-lookup"><span data-stu-id="0928b-134"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="0928b-135">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-135">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-136">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="0928b-136">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="0928b-137"><em>pvResult</em> se interpreta como <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="0928b-137"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="0928b-138">Si se ejecuta correctamente, la estructura de <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> recibe información sobre el índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-138">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="0928b-139">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-139">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-140">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="0928b-140">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="0928b-141">JET_IdxInfoLangid está en desuso.</span><span class="sxs-lookup"><span data-stu-id="0928b-141">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="0928b-142">En su lugar, use JET_IdxInfoLCID y la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</span><span class="sxs-lookup"><span data-stu-id="0928b-142">Use JET_IdxInfoLCID and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-143">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="0928b-143">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="0928b-144"><em>pvResult</em> se interpreta como un LCID.</span><span class="sxs-lookup"><span data-stu-id="0928b-144"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="0928b-145">Si se ejecuta correctamente, el LCID contiene el identificador de configuración regional del índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-145">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="0928b-146">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-146">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="0928b-147"><strong>Windows XP:  </strong> JET_IdxInfoLCID se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0928b-147"><strong>Windows XP:  </strong>JET_IdxInfoLCID is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-148">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="0928b-148">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="0928b-149"><em>pvResult</em> se interpreta como una estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="0928b-149"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="0928b-150">Si se ejecuta correctamente, la estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recibe información sobre el índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-150">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="0928b-151">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-151">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-152">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="0928b-152">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="0928b-153">JET_IdxInfoOLC está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0928b-153">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-154">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="0928b-154">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="0928b-155">JET_IdxInfoResetOLC está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0928b-155">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-156">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="0928b-156">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="0928b-157"><em>pvResult</em> se interpreta como ulong.</span><span class="sxs-lookup"><span data-stu-id="0928b-157"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="0928b-158">Si se ejecuta correctamente, ULONG contiene el uso de espacio del índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-158">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="0928b-159">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-160">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="0928b-160">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="0928b-161">JET_IdxInfoSysTabCursor está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0928b-161">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-162">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="0928b-162">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="0928b-163"><em>pvResult</em> se interpreta como un USHORT.</span><span class="sxs-lookup"><span data-stu-id="0928b-163"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="0928b-164">Si se ejecuta correctamente, USHORT contiene el valor de <em>cbVarSegMac</em> que se usa cuando se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-164">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="0928b-165">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbVarSegMac</em>.</span><span class="sxs-lookup"><span data-stu-id="0928b-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="0928b-166">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-166">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-167">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="0928b-167">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="0928b-168"><em>pvResult</em> se interpreta como un USHORT.</span><span class="sxs-lookup"><span data-stu-id="0928b-168"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="0928b-169">Si se ejecuta correctamente, USHORT contiene el valor de <em>cbKeyMost</em> que se usa cuando se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-169">On success, the USHORT holds the value of <em>cbKeyMost</em> used when the index was created.</span></span> <span data-ttu-id="0928b-170">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbKeyMost</em>.</span><span class="sxs-lookup"><span data-stu-id="0928b-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbKeyMost</em>.</span></span> <span data-ttu-id="0928b-171">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="0928b-172"><strong>Windows Vista:  </strong> JET_IdxInfoKeyMost se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0928b-172"><strong>Windows Vista:  </strong>JET_IdxInfoKeyMost is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-173">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="0928b-173">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="0928b-174"><em>pvResult</em> se interpreta como una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="0928b-174"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="0928b-175">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="0928b-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0928b-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-177">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="0928b-177">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="0928b-178"><em>pvResult</em> se interpreta como una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="0928b-178"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="0928b-179">En caso de error, el contenido de <em>pvBuffer</em> no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-179">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="0928b-180"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0928b-180"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0928b-181">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0928b-181">Return Value</span></span>

<span data-ttu-id="0928b-182">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="0928b-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0928b-183">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0928b-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0928b-184">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0928b-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="0928b-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="0928b-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0928b-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0928b-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0928b-187">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0928b-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-188">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="0928b-188">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="0928b-189">No se encuentra el índice especificado en la tabla especificada.</span><span class="sxs-lookup"><span data-stu-id="0928b-189">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-190">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="0928b-190">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="0928b-191">El búfer pasado como <em>pvResult</em> era demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="0928b-191">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="0928b-192">El contenido del búfer no está definido.</span><span class="sxs-lookup"><span data-stu-id="0928b-192">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="0928b-193">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0928b-193">Remarks</span></span>

<span data-ttu-id="0928b-194">**JetGetIndexInfo** y [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperan la misma información sobre un índice.</span><span class="sxs-lookup"><span data-stu-id="0928b-194">**JetGetIndexInfo** and [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) retrieve identical information about an index.</span></span> <span data-ttu-id="0928b-195">La diferencia radica en cómo se especifica la tabla.</span><span class="sxs-lookup"><span data-stu-id="0928b-195">The difference is in how the table is specified.</span></span> <span data-ttu-id="0928b-196">**JetGetIndexInfo** espera una base de datos (*DBID*) y el nombre de una tabla (*SzTableName*), mientras que [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) espera un identificador de tabla (*TABLEID*).</span><span class="sxs-lookup"><span data-stu-id="0928b-196">**JetGetIndexInfo** expects a database (*dbid*) and name of a table (*szTableName*), while [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="0928b-197">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0928b-197">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0928b-198"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0928b-198"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0928b-199">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0928b-199">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-200"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0928b-200"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0928b-201">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0928b-201">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-202"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0928b-202"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0928b-203">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="0928b-203">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-204"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="0928b-204"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0928b-205">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0928b-205">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0928b-206"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0928b-206"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0928b-207">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0928b-207">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0928b-208"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0928b-208"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0928b-209">Se implementa como <strong>JetGetIndexInfoW</strong> (Unicode) y <strong>JetGetIndexInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0928b-209">Implemented as <strong>JetGetIndexInfoW</strong> (Unicode) and <strong>JetGetIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0928b-210">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0928b-210">See Also</span></span>

[<span data-ttu-id="0928b-211">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="0928b-211">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="0928b-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0928b-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0928b-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0928b-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0928b-214">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="0928b-214">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="0928b-215">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="0928b-215">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="0928b-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0928b-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0928b-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0928b-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0928b-218">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="0928b-218">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
