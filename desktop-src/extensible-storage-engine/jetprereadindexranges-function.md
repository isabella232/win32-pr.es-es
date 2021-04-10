---
description: 'Más información acerca de: JetPrereadIndexRanges (función)'
title: JetPrereadIndexRanges función)
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153769"
---
# <a name="jetprereadindexranges-function"></a><span data-ttu-id="007b4-103">JetPrereadIndexRanges función)</span><span class="sxs-lookup"><span data-stu-id="007b4-103">JetPrereadIndexRanges Function</span></span>


<span data-ttu-id="007b4-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="007b4-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="007b4-105">La función **JetPrereadIndexRanges** prelee los índices para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="007b4-105">The **JetPrereadIndexRanges** function prereads indexes to improve the performance.</span></span>

<span data-ttu-id="007b4-106">La función **JetPrereadIndexRanges** se presentó en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="007b4-106">The **JetPrereadIndexRanges** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="007b4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="007b4-107">Parameters</span></span>

<span data-ttu-id="007b4-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="007b4-108">*sesid*</span></span>

<span data-ttu-id="007b4-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="007b4-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="007b4-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="007b4-110">*tableid*</span></span>

<span data-ttu-id="007b4-111">Tabla en la que se van a emitir las lecturas preleídas.</span><span class="sxs-lookup"><span data-stu-id="007b4-111">The table to issue the prereads against.</span></span>

<span data-ttu-id="007b4-112">*rgIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="007b4-112">*rgIndexRanges*</span></span>

<span data-ttu-id="007b4-113">Intervalos de clave que se van a leer como preleídos.</span><span class="sxs-lookup"><span data-stu-id="007b4-113">The key ranges to preread.</span></span>

<span data-ttu-id="007b4-114">*cIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="007b4-114">*cIndexRanges*</span></span>

<span data-ttu-id="007b4-115">Número de intervalos de clave que se van a leer antes, determinado por el número de elementos de *rgIndexRanges*.</span><span class="sxs-lookup"><span data-stu-id="007b4-115">The number of key ranges to preread, determined by the number of elements in *rgIndexRanges*.</span></span>

<span data-ttu-id="007b4-116">*pcRangesPreread*</span><span class="sxs-lookup"><span data-stu-id="007b4-116">*pcRangesPreread*</span></span>

<span data-ttu-id="007b4-117">Número de intervalos de clave que se leyeron realmente.</span><span class="sxs-lookup"><span data-stu-id="007b4-117">The number of key ranges that were actually preread.</span></span>

<span data-ttu-id="007b4-118">*rgcolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="007b4-118">*rgcolumnidPreread*</span></span>

<span data-ttu-id="007b4-119">Lista de identificadores de columna para las columnas de valor largo que se van a leer como prelectura.</span><span class="sxs-lookup"><span data-stu-id="007b4-119">List of column IDs for long value columns to preread.</span></span> <span data-ttu-id="007b4-120">De forma predeterminada, solo se prelee el registro en la página.</span><span class="sxs-lookup"><span data-stu-id="007b4-120">By default, only the on-page record is preread.</span></span> <span data-ttu-id="007b4-121">Si es necesario realizar una lectura de las columnas de valores largos fuera de la página, es necesario pasar los identificadores de columna a través de este parámetro.</span><span class="sxs-lookup"><span data-stu-id="007b4-121">If Off-page long value columns need to be preread, their column IDs need to be passed via this parameter.</span></span>

<span data-ttu-id="007b4-122">*ccolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="007b4-122">*ccolumnidPreread*</span></span>

<span data-ttu-id="007b4-123">El número de identificadores de columna para las columnas de valor largo que se van a leer de forma predeterminada, determinado por el número de elementos de *rgcolumnidPreread*.</span><span class="sxs-lookup"><span data-stu-id="007b4-123">The number of column IDs for long value columns to preread, determined by the number of elements in *rgcolumnidPreread*.</span></span>

<span data-ttu-id="007b4-124">*grbit*</span><span class="sxs-lookup"><span data-stu-id="007b4-124">*grbit*</span></span>

<span data-ttu-id="007b4-125">Grupo de bits que especifica cero o más de los valores de dirección de prelectura enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="007b4-125">A group of bits that specifies zero or more of the preread direction values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="007b4-126">Value</span><span class="sxs-lookup"><span data-stu-id="007b4-126">Value</span></span></p></th>
<th><p><span data-ttu-id="007b4-127">Significado</span><span class="sxs-lookup"><span data-stu-id="007b4-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="007b4-128">Adelante</span><span class="sxs-lookup"><span data-stu-id="007b4-128">Forward</span></span></p></td>
<td><p><span data-ttu-id="007b4-129">Avance de prelectura.</span><span class="sxs-lookup"><span data-stu-id="007b4-129">Preread forward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="007b4-130">Atrás</span><span class="sxs-lookup"><span data-stu-id="007b4-130">Backwards</span></span></p></td>
<td><p><span data-ttu-id="007b4-131">Lectura anterior.</span><span class="sxs-lookup"><span data-stu-id="007b4-131">Preread backward.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="007b4-132">FirstPageOnly</span><span class="sxs-lookup"><span data-stu-id="007b4-132">FirstPageOnly</span></span></p></td>
<td><p><span data-ttu-id="007b4-133">Preread solo la primera página de cualquier columna de tipo Long.</span><span class="sxs-lookup"><span data-stu-id="007b4-133">Preread only the first page of any long column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="007b4-134">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="007b4-134">NormalizedKey</span></span></p></td>
<td><p><span data-ttu-id="007b4-135">Clave/marcador normalizado proporcionado en lugar de valor de columna.</span><span class="sxs-lookup"><span data-stu-id="007b4-135">Normalized key/bookmark provided instead of column value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="007b4-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="007b4-136">Return value</span></span>

<span data-ttu-id="007b4-137">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="007b4-137">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="007b4-138">Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="007b4-138">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="007b4-139">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="007b4-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="007b4-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="007b4-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="007b4-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="007b4-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="007b4-142">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="007b4-142">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="007b4-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="007b4-143">Remarks</span></span>

<span data-ttu-id="007b4-144">Si los registros con los intervalos de claves especificados no están en la caché del búfer, debe iniciar lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="007b4-144">If the records with the specified key ranges are not in the buffer cache, you should start asynchronous reads to bring the records into the database buffer cache.</span></span>

#### <a name="requirements"></a><span data-ttu-id="007b4-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="007b4-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="007b4-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="007b4-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="007b4-147">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="007b4-147">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="007b4-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="007b4-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="007b4-149">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="007b4-149">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="007b4-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="007b4-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="007b4-151">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="007b4-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="007b4-152"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="007b4-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="007b4-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="007b4-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="007b4-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="007b4-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="007b4-155">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="007b4-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="007b4-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="007b4-156">See also</span></span>

[<span data-ttu-id="007b4-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="007b4-157">JET_ERR</span></span>](./jet-err.md)
