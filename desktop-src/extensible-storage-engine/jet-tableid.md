---
description: 'Más información acerca de: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697448"
---
# <a name="jet_tableid"></a><span data-ttu-id="9c7c4-103">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9c7c4-103">JET_TABLEID</span></span>


<span data-ttu-id="9c7c4-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c7c4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tableid"></a><span data-ttu-id="9c7c4-105">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9c7c4-105">JET_TABLEID</span></span>

<span data-ttu-id="9c7c4-106">El tipo de datos JET_TABLEID contiene un identificador para el cursor de base de datos que se va a usar para una llamada a la API de JET.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-106">The JET_TABLEID data type contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="9c7c4-107">Un cursor solo se puede usar con la sesión que se usó para abrir ese cursor.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-107">A cursor can only be used with the session that was used to open that cursor.</span></span>

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a><span data-ttu-id="9c7c4-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9c7c4-108">Data Types</span></span>

<span data-ttu-id="9c7c4-109">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9c7c4-109">JET_TABLEID</span></span>

<span data-ttu-id="9c7c4-110">Se puede utilizar **null** o [JET_tableidNil](./invalid-handle-constants.md) para indicar un identificador de cursor no válido.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-110">Either **NULL** or [JET_tableidNil](./invalid-handle-constants.md) can be used to indicate an invalid cursor handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="9c7c4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c7c4-111">Remarks</span></span>

<span data-ttu-id="9c7c4-112">Un cursor administra el uso de una tabla para el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-112">A cursor manages the use of a table for the database engine.</span></span> <span data-ttu-id="9c7c4-113">Un cursor puede realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c7c4-113">A cursor can do the following tasks:</span></span>

  - <span data-ttu-id="9c7c4-114">Examinar registros</span><span class="sxs-lookup"><span data-stu-id="9c7c4-114">Scan records</span></span>

  - <span data-ttu-id="9c7c4-115">Buscar registros</span><span class="sxs-lookup"><span data-stu-id="9c7c4-115">Search for records</span></span>

  - <span data-ttu-id="9c7c4-116">Elegir el criterio de ordenación y la visibilidad efectivos de esos registros</span><span class="sxs-lookup"><span data-stu-id="9c7c4-116">Choose the effective sort order and visibility of those records</span></span>

  - <span data-ttu-id="9c7c4-117">Crear, actualizar o eliminar registros</span><span class="sxs-lookup"><span data-stu-id="9c7c4-117">Create, update, or delete records</span></span>

  - <span data-ttu-id="9c7c4-118">Modificar el esquema de la tabla</span><span class="sxs-lookup"><span data-stu-id="9c7c4-118">Modify the schema of the table</span></span>

<span data-ttu-id="9c7c4-119">La funcionalidad admitida del cursor puede cambiar a medida que cambia el estado o el tipo de la tabla subyacente.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-119">The supported functionality of the cursor might change as the status or type of the underlying table changes.</span></span> <span data-ttu-id="9c7c4-120">Por ejemplo, una tabla temporal podría no permitir la búsqueda de datos cuando se abre con determinadas opciones.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-120">For example, a temporary table might disallow searching for data when it is opened with certain options.</span></span> <span data-ttu-id="9c7c4-121">El cursor siempre está totalmente conectado a la tabla subyacente e interactúa directamente con esos datos sin almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-121">The cursor is always fully connected to the underlying table and interacts with that data directly without any caching.</span></span> <span data-ttu-id="9c7c4-122">Casi toda la funcionalidad de ISAM básica que expone este motor de base de datos funciona a través del cursor.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-122">Almost all of the core ISAM functionality that is exposed by this database engine is works through the cursor.</span></span>

<span data-ttu-id="9c7c4-123">Se puede crear un cursor mediante [JetOpenTable](./jetopentable-function.md) o [JetOpenTempTable](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="9c7c4-123">A cursor can be created using [JetOpenTable](./jetopentable-function.md) or [JetOpenTempTable](./jetopentemptable-function.md).</span></span> <span data-ttu-id="9c7c4-124">Un cursor se puede duplicar mediante [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="9c7c4-124">A cursor can be duplicated using [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="9c7c4-125">Un cursor se puede cerrar explícitamente mediante [JetCloseTable](./jetclosetable-function.md) o cerrarse implícitamente mediante [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="9c7c4-125">A cursor can be explicitly closed using [JetCloseTable](./jetclosetable-function.md) or implicitly closed using [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span> <span data-ttu-id="9c7c4-126">[JetRollback](./jetrollback-function.md) también puede cerrar implícitamente un cursor si estaba abierto en la transacción que se ha anulado.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-126">A cursor can also be implicitly closed by [JetRollback](./jetrollback-function.md) if it was opened in the transaction that was aborted.</span></span> <span data-ttu-id="9c7c4-127">El número máximo de cursores que se pueden crear en cualquier momento se controla mediante [JET_paramMaxCursors](./resource-parameters.md), que puede configurarse mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="9c7c4-127">The maximum number of cursors that can be created at any one time is controlled by [JET_paramMaxCursors](./resource-parameters.md), which can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="9c7c4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c7c4-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c7c4-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9c7c4-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c7c4-130">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c7c4-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9c7c4-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c7c4-132">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c7c4-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9c7c4-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c7c4-134">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="9c7c4-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9c7c4-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9c7c4-135">See Also</span></span>

[<span data-ttu-id="9c7c4-136">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="9c7c4-136">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="9c7c4-137">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="9c7c4-137">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="9c7c4-138">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="9c7c4-138">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="9c7c4-139">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="9c7c4-139">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="9c7c4-140">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="9c7c4-140">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="9c7c4-141">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="9c7c4-141">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="9c7c4-142">JetRollback</span><span class="sxs-lookup"><span data-stu-id="9c7c4-142">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="9c7c4-143">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9c7c4-143">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9c7c4-144">JetTerm</span><span class="sxs-lookup"><span data-stu-id="9c7c4-144">JetTerm</span></span>](./jetterm-function.md)
