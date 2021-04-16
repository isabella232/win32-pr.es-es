---
description: 'Más información acerca de: JetCloseTable (función)'
title: JetCloseTable función)
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548158"
---
# <a name="jetclosetable-function"></a><span data-ttu-id="b286a-103">JetCloseTable función)</span><span class="sxs-lookup"><span data-stu-id="b286a-103">JetCloseTable Function</span></span>


<span data-ttu-id="b286a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b286a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosetable-function"></a><span data-ttu-id="b286a-105">JetCloseTable función)</span><span class="sxs-lookup"><span data-stu-id="b286a-105">JetCloseTable Function</span></span>

<span data-ttu-id="b286a-106">La función **JetCloseTable** cierra una tabla abierta en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="b286a-106">The **JetCloseTable** function closes an open table in a database.</span></span> <span data-ttu-id="b286a-107">La tabla puede ser una tabla temporal o una tabla normal.</span><span class="sxs-lookup"><span data-stu-id="b286a-107">The table may be a temporary table or a normal table.</span></span>

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a><span data-ttu-id="b286a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b286a-108">Parameters</span></span>

<span data-ttu-id="b286a-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b286a-109">*sesid*</span></span>

<span data-ttu-id="b286a-110">Identifica el contexto de la sesión de base de datos que se utilizará para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="b286a-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="b286a-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="b286a-111">*tableid*</span></span>

<span data-ttu-id="b286a-112">Identifica la tabla que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="b286a-112">Identifies the table to be closed.</span></span>

<span data-ttu-id="b286a-113">Establezca *TABLEID* en JET_tableidNil para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="b286a-113">Set *tableid* to JET_tableidNil to release memory.</span></span>

### <a name="return-value"></a><span data-ttu-id="b286a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b286a-114">Return Value</span></span>

<span data-ttu-id="b286a-115">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="b286a-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b286a-116">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b286a-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b286a-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b286a-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="b286a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b286a-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b286a-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b286a-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b286a-120">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b286a-120">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b286a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b286a-121">Remarks</span></span>

<span data-ttu-id="b286a-122">Se debe llamar a esta función en todas las tablas abiertas con [JetOpenTable](./jetopentable-function.md).</span><span class="sxs-lookup"><span data-stu-id="b286a-122">This function must be called on all tables opened with [JetOpenTable](./jetopentable-function.md).</span></span>

<span data-ttu-id="b286a-123">La excepción a esta regla se produce cuando se llama a [JetOpenTable](./jetopentable-function.md) en una transacción y se revierte la transacción (con [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="b286a-123">The exception to this rule happens when [JetOpenTable](./jetopentable-function.md) is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="b286a-124">Cuando se revierte una transacción, la tabla se cierra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b286a-124">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="b286a-125">En este caso, es un error cerrar la tabla con **JetCloseTable**.</span><span class="sxs-lookup"><span data-stu-id="b286a-125">In this case, it is an error to close the table with **JetCloseTable**.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b286a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b286a-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b286a-127"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b286a-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b286a-128">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b286a-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b286a-129"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b286a-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b286a-130">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b286a-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b286a-131"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b286a-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b286a-132">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b286a-132">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b286a-133"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="b286a-133"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b286a-134">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b286a-134">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b286a-135"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b286a-135"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b286a-136">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b286a-136">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b286a-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b286a-137">See Also</span></span>

[<span data-ttu-id="b286a-138">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b286a-138">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b286a-139">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b286a-139">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b286a-140">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b286a-140">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b286a-141">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b286a-141">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b286a-142">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="b286a-142">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="b286a-143">JetRollback</span><span class="sxs-lookup"><span data-stu-id="b286a-143">JetRollback</span></span>](./jetrollback-function.md)
