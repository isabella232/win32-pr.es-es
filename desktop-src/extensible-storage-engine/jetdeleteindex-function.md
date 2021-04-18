---
description: 'Más información acerca de: JetDeleteIndex (función)'
title: JetDeleteIndex función)
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697824"
---
# <a name="jetdeleteindex-function"></a><span data-ttu-id="e3322-103">JetDeleteIndex función)</span><span class="sxs-lookup"><span data-stu-id="e3322-103">JetDeleteIndex Function</span></span>


<span data-ttu-id="e3322-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e3322-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeleteindex-function"></a><span data-ttu-id="e3322-105">JetDeleteIndex función)</span><span class="sxs-lookup"><span data-stu-id="e3322-105">JetDeleteIndex Function</span></span>

<span data-ttu-id="e3322-106">La función **JetDeleteIndex** elimina un índice de una tabla.</span><span class="sxs-lookup"><span data-stu-id="e3322-106">The **JetDeleteIndex** function deletes an index from a table.</span></span>

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="e3322-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3322-107">Parameters</span></span>

<span data-ttu-id="e3322-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e3322-108">*sesid*</span></span>

<span data-ttu-id="e3322-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="e3322-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="e3322-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="e3322-110">*tableid*</span></span>

<span data-ttu-id="e3322-111">Tabla que contiene la columna que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="e3322-111">The table that contains the column that is to be deleted.</span></span>

<span data-ttu-id="e3322-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="e3322-112">*szIndexName*</span></span>

<span data-ttu-id="e3322-113">Nombre del índice que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="e3322-113">The name of the index to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="e3322-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3322-114">Return Value</span></span>

<span data-ttu-id="e3322-115">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="e3322-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e3322-116">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e3322-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3322-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e3322-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="e3322-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3322-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3322-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e3322-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e3322-120">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3322-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3322-121">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="e3322-121">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="e3322-122">Se intentó eliminar un índice de una tabla fija (por ejemplo, uno creado con JET_bitTableCreateFixedDDL).</span><span class="sxs-lookup"><span data-stu-id="e3322-122">An attempt was made to delete an index from a fixed table (for example, one created with JET_bitTableCreateFixedDDL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3322-123">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="e3322-123">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="e3322-124">Se intentó eliminar un índice de una tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="e3322-124">An attempt was made to delete an index from a template table.</span></span> <span data-ttu-id="e3322-125">Una tabla de plantillas tiene un DDL fijo.</span><span class="sxs-lookup"><span data-stu-id="e3322-125">A template table has fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3322-126">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="e3322-126">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="e3322-127">No se encontró el índice con el nombre en <em>szIndexName</em> .</span><span class="sxs-lookup"><span data-stu-id="e3322-127">The index named in <em>szIndexName</em> was not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3322-128">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="e3322-128">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="e3322-129">No se puede actualizar la tabla porque se ha abierto como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3322-129">The table cannot be updated because it was opened read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3322-130">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e3322-130">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e3322-131">Varios subprocesos intentaron usar la misma sesión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e3322-131">Multiple threads attempted to use the same database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3322-132">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="e3322-132">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e3322-133">La transacción se abrió como una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3322-133">The transaction was opened as a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e3322-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3322-134">Remarks</span></span>

<span data-ttu-id="e3322-135">Cuando se realiza correctamente, se elimina el índice y, por tanto, no se puede usar posteriormente.</span><span class="sxs-lookup"><span data-stu-id="e3322-135">When successful, the index is deleted and therefore cannot be used subsequently.</span></span> <span data-ttu-id="e3322-136">No debe haber ninguna transacción activa que utilice el índice.</span><span class="sxs-lookup"><span data-stu-id="e3322-136">There must not be any active transaction using the index.</span></span>

<span data-ttu-id="e3322-137">Si se ejecuta correctamente, la moneda se establece antes del primer registro.</span><span class="sxs-lookup"><span data-stu-id="e3322-137">On success, the currency is set before the first record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e3322-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3322-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3322-139"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e3322-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e3322-140">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e3322-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3322-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e3322-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e3322-142">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e3322-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3322-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e3322-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e3322-144">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="e3322-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3322-145"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="e3322-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e3322-146">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e3322-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3322-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e3322-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e3322-148">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e3322-148">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3322-149"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e3322-149"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e3322-150">Se implementa como <strong>JetDeleteIndexW</strong> (Unicode) y <strong>JetDeleteIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e3322-150">Implemented as <strong>JetDeleteIndexW</strong> (Unicode) and <strong>JetDeleteIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e3322-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3322-151">See Also</span></span>

[<span data-ttu-id="e3322-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e3322-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e3322-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e3322-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e3322-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e3322-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e3322-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e3322-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e3322-156">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="e3322-156">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="e3322-157">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="e3322-157">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)
