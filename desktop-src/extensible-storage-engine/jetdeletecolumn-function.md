---
description: 'Más información acerca de: JetDeleteColumn (función)'
title: JetDeleteColumn función)
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104003991"
---
# <a name="jetdeletecolumn-function"></a><span data-ttu-id="13ff3-103">JetDeleteColumn función)</span><span class="sxs-lookup"><span data-stu-id="13ff3-103">JetDeleteColumn Function</span></span>


<span data-ttu-id="13ff3-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="13ff3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn-function"></a><span data-ttu-id="13ff3-105">JetDeleteColumn función)</span><span class="sxs-lookup"><span data-stu-id="13ff3-105">JetDeleteColumn Function</span></span>

<span data-ttu-id="13ff3-106">La función **JetDeleteColumn** elimina una columna de una tabla de base de datos ese.</span><span class="sxs-lookup"><span data-stu-id="13ff3-106">The **JetDeleteColumn** function deletes a column from an ESE database table.</span></span>

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a><span data-ttu-id="13ff3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13ff3-107">Parameters</span></span>

<span data-ttu-id="13ff3-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="13ff3-108">*sesid*</span></span>

<span data-ttu-id="13ff3-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="13ff3-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="13ff3-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="13ff3-110">*tableid*</span></span>

<span data-ttu-id="13ff3-111">Tabla de la que se va a eliminar la columna.</span><span class="sxs-lookup"><span data-stu-id="13ff3-111">The table from which to delete the column.</span></span>

<span data-ttu-id="13ff3-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="13ff3-112">*szColumnName*</span></span>

<span data-ttu-id="13ff3-113">Nombre de la columna que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="13ff3-113">The name of the column to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="13ff3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13ff3-114">Return Value</span></span>

<span data-ttu-id="13ff3-115">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="13ff3-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="13ff3-116">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="13ff3-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13ff3-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="13ff3-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="13ff3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="13ff3-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13ff3-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="13ff3-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="13ff3-120">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="13ff3-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13ff3-121">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="13ff3-121">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="13ff3-122">La columna está en uso actualmente.</span><span class="sxs-lookup"><span data-stu-id="13ff3-122">The column is currently in use.</span></span> <span data-ttu-id="13ff3-123">Es posible que un índice lo esté usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="13ff3-123">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13ff3-124">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="13ff3-124">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="13ff3-125">Se intentó modificar el DDL fijo.</span><span class="sxs-lookup"><span data-stu-id="13ff3-125">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13ff3-126">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="13ff3-126">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="13ff3-127">La columna denominada en <em>szColumnName</em> existe en la tabla de plantilla y el DDL de una tabla de plantilla no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="13ff3-127">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13ff3-128">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="13ff3-128">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="13ff3-129">Se puede devolver si se proporcionó un nombre incorrecto para <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="13ff3-129">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13ff3-130">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="13ff3-130">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="13ff3-131">No se puede escribir en la tabla.</span><span class="sxs-lookup"><span data-stu-id="13ff3-131">The table is not writable.</span></span> <span data-ttu-id="13ff3-132">Esto puede devolverse si la base de datos se abrió en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="13ff3-132">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13ff3-133">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="13ff3-133">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="13ff3-134">La transacción es una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="13ff3-134">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="13ff3-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13ff3-135">Remarks</span></span>

<span data-ttu-id="13ff3-136">Llamar a **JetDeleteColumn** es idéntico a llamar a [JetDeleteColumn2](./jetdeletecolumn2-function.md) con *grbit* establecido en cero (0).</span><span class="sxs-lookup"><span data-stu-id="13ff3-136">Calling **JetDeleteColumn** is identical to calling [JetDeleteColumn2](./jetdeletecolumn2-function.md) with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="13ff3-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ff3-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13ff3-138"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="13ff3-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="13ff3-139">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="13ff3-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13ff3-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="13ff3-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="13ff3-141">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="13ff3-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13ff3-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="13ff3-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="13ff3-143">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="13ff3-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13ff3-144"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="13ff3-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="13ff3-145">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="13ff3-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13ff3-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="13ff3-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="13ff3-147">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="13ff3-147">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13ff3-148"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="13ff3-148"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="13ff3-149">Se implementa como <strong>JetDeleteColumnW</strong> (Unicode) y <strong>JetDeleteColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="13ff3-149">Implemented as <strong>JetDeleteColumnW</strong> (Unicode) and <strong>JetDeleteColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="13ff3-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13ff3-150">See Also</span></span>

[<span data-ttu-id="13ff3-151">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="13ff3-151">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="13ff3-152">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="13ff3-152">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="13ff3-153">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="13ff3-153">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="13ff3-154">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="13ff3-154">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="13ff3-155">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="13ff3-155">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
