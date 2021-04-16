---
description: 'Más información acerca de: JetPrereadKeys (función)'
title: JetPrereadKeys función)
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497410"
---
# <a name="jetprereadkeys-function"></a><span data-ttu-id="1b606-103">JetPrereadKeys función)</span><span class="sxs-lookup"><span data-stu-id="1b606-103">JetPrereadKeys Function</span></span>


<span data-ttu-id="1b606-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1b606-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprereadkeys-function"></a><span data-ttu-id="1b606-105">JetPrereadKeys función)</span><span class="sxs-lookup"><span data-stu-id="1b606-105">JetPrereadKeys Function</span></span>

<span data-ttu-id="1b606-106">La función **JetPrereadKeys** Lee los valores de clave para mejorar el rendimiento de la limpieza del almacén de versiones.</span><span class="sxs-lookup"><span data-stu-id="1b606-106">The **JetPrereadKeys** function reads key values to improve the performance of version store cleanup.</span></span>

<span data-ttu-id="1b606-107">**Windows 7:** la función PrereadKeys se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1b606-107">**Windows 7:  PrereadKeys** function is introduced in Windows 7.</span></span>

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a><span data-ttu-id="1b606-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b606-108">Parameters</span></span>

<span data-ttu-id="1b606-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1b606-109">*sesid*</span></span>

<span data-ttu-id="1b606-110">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="1b606-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="1b606-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="1b606-111">*tableid*</span></span>

<span data-ttu-id="1b606-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="1b606-112">The cursor to use for this call.</span></span>

<span data-ttu-id="1b606-113">*rgpvKeys*</span><span class="sxs-lookup"><span data-stu-id="1b606-113">*rgpvKeys*</span></span>

<span data-ttu-id="1b606-114">Matriz de punteros a claves.</span><span class="sxs-lookup"><span data-stu-id="1b606-114">An array of pointers to keys.</span></span> <span data-ttu-id="1b606-115">Las claves se pueden realizar con [JetMakeKey](./jetmakekey-function.md) o recuperar con [JetGetBookmark](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="1b606-115">Keys can be made with [JetMakeKey](./jetmakekey-function.md) or retrieved with [JetGetBookmark](./jetgetbookmark-function.md).</span></span> <span data-ttu-id="1b606-116">Las claves deben ordenarse en orden ascendente o descendente, según el grbit pasado.</span><span class="sxs-lookup"><span data-stu-id="1b606-116">The keys must be sorted in ascending or descending order, depending on the grbit passed.</span></span> <span data-ttu-id="1b606-117">Las claves se pueden ordenar con memcmp.</span><span class="sxs-lookup"><span data-stu-id="1b606-117">Keys can be sorted with memcmp.</span></span>

<span data-ttu-id="1b606-118">*rgcbKeys*</span><span class="sxs-lookup"><span data-stu-id="1b606-118">*rgcbKeys*</span></span>

<span data-ttu-id="1b606-119">Matriz de longitudes de clave.</span><span class="sxs-lookup"><span data-stu-id="1b606-119">An array of key lengths.</span></span> <span data-ttu-id="1b606-120">rgpvKeys \[ n \] debe apuntar a una clave de longitud rgcbKeys \[ n\]</span><span class="sxs-lookup"><span data-stu-id="1b606-120">rgpvKeys\[n\] should point to a key of length rgcbKeys\[n\]</span></span>

<span data-ttu-id="1b606-121">*ckeys*</span><span class="sxs-lookup"><span data-stu-id="1b606-121">*ckeys*</span></span>

<span data-ttu-id="1b606-122">Número de claves.</span><span class="sxs-lookup"><span data-stu-id="1b606-122">The number of keys.</span></span> <span data-ttu-id="1b606-123">rgpvKeys y rgcbKeys deben apuntar a una matriz con al menos ckeys elementos.</span><span class="sxs-lookup"><span data-stu-id="1b606-123">rgpvKeys and rgcbKeys must each point to an array with at least ckeys elements.</span></span>

<span data-ttu-id="1b606-124">*pckeysPreread*</span><span class="sxs-lookup"><span data-stu-id="1b606-124">*pckeysPreread*</span></span>

<span data-ttu-id="1b606-125">Devuelve el número de claves para las que se han emitido realmente las lecturas.</span><span class="sxs-lookup"><span data-stu-id="1b606-125">Returns the number of keys that prereads were actually issued for.</span></span> <span data-ttu-id="1b606-126">Este parámetro puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="1b606-126">This parameter can be NULL.</span></span>

<span data-ttu-id="1b606-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1b606-127">*grbit*</span></span>

<span data-ttu-id="1b606-128">Debe ser JET_bitPrereadForward o JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="1b606-128">This must be either JET_bitPrereadForward or JET_bitPrereadBackward.</span></span> <span data-ttu-id="1b606-129">Si grbit es JET_bitPrereadForward, las claves se deben ordenar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="1b606-129">If grbit is JET_bitPrereadForward, the keys must be sorted in ascending order.</span></span> <span data-ttu-id="1b606-130">Si grbit es JET_bitPrereadBackward, las claves se deben ordenar en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="1b606-130">If grbit is JET_bitPrereadBackward, the keys must be sorted in descending order.</span></span>

### <a name="return-value"></a><span data-ttu-id="1b606-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b606-131">Return Value</span></span>

<span data-ttu-id="1b606-132">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="1b606-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1b606-133">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1b606-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="1b606-134">Pueden devolverse varios errores de e/s junto con estos errores de uso de la API:</span><span class="sxs-lookup"><span data-stu-id="1b606-134">Various I/O errors can be returned along with these API usage errors:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b606-135">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1b606-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="1b606-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b606-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b606-137">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="1b606-137">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="1b606-138">Grbit no se JET_bitPrereadForward ni JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="1b606-138">Grbit was neither JET_bitPrereadForward nor JET_bitPrereadBackward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b606-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="1b606-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="1b606-140">Se ha pasado un tamaño de clave incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1b606-140">An incorrect key size has been passed in.</span></span> <span data-ttu-id="1b606-141">Las claves no pueden ser 0 ni mayores que la longitud de clave máxima de la tabla.</span><span class="sxs-lookup"><span data-stu-id="1b606-141">Keys can neither be 0 nor longer than the maximum key length for the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b606-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1b606-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1b606-143">Se ha pasado un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="1b606-143">An invalid parameter has been passed in.</span></span> <span data-ttu-id="1b606-144">Esto puede deberse a un valor null para un parámetro necesario o puede indicar que la matriz de claves no está ordenada correctamente.</span><span class="sxs-lookup"><span data-stu-id="1b606-144">This can be caused by a null value for a required parameter or can indicate that the key array is not sorted properly.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1b606-145">**JetPrereadKeys** recorre las páginas internas del árbol b para determinar qué páginas hoja contienen las claves especificadas por RgpvKeys/rgcbKeys.</span><span class="sxs-lookup"><span data-stu-id="1b606-145">**JetPrereadKeys** traverses the internal pages of the b-tree to determine which leaf pages contain the keys specified by rgpvKeys/rgcbKeys.</span></span> <span data-ttu-id="1b606-146">La lista de páginas hoja está ordenada y, a continuación, se emiten las prelectura para los intervalos de páginas.</span><span class="sxs-lookup"><span data-stu-id="1b606-146">The list of leaf pages is sorted and then prereads are issued for the ranges of pages.</span></span> <span data-ttu-id="1b606-147">El número de páginas que se pueden leer de forma preleída es limitado, por lo que es posible que no se puedan leer todas las claves.</span><span class="sxs-lookup"><span data-stu-id="1b606-147">The number of pages that can be preread is limited so it is possible that not all keys may be preread.</span></span> <span data-ttu-id="1b606-148">En ese caso, el número de claves realmente leídas se devuelve en pckeysPreread.</span><span class="sxs-lookup"><span data-stu-id="1b606-148">In that case, the number of keys actually preread is returned in pckeysPreread.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1b606-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b606-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b606-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1b606-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1b606-151">Requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1b606-151">Requires Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b606-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1b606-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1b606-153">Requiere Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1b606-153">Requires Windows Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b606-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1b606-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1b606-155">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="1b606-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b606-156"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="1b606-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1b606-157">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1b606-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b606-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1b606-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1b606-159">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1b606-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>
