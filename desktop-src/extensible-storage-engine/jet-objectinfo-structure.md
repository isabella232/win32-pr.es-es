---
description: 'Más información acerca de: estructura de JET_OBJECTINFO'
title: Estructura de JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
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
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083049"
---
# <a name="jet_objectinfo-structure"></a><span data-ttu-id="3b2fb-103">Estructura de JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="3b2fb-103">JET_OBJECTINFO Structure</span></span>


<span data-ttu-id="3b2fb-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b2fb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectinfo-structure"></a><span data-ttu-id="3b2fb-105">Estructura de JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="3b2fb-105">JET_OBJECTINFO Structure</span></span>

<span data-ttu-id="3b2fb-106">La estructura de **JET_OBJECTINFO** contiene información sobre un objeto.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-106">The **JET_OBJECTINFO** structure holds information about an object.</span></span> <span data-ttu-id="3b2fb-107">Las tablas son los únicos tipos de objeto que se admiten actualmente.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-107">Tables are the only object types that are currently supported.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a><span data-ttu-id="3b2fb-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b2fb-108">Members</span></span>

<span data-ttu-id="3b2fb-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="3b2fb-109">**cbStruct**</span></span>

<span data-ttu-id="3b2fb-110">Tamaño, en bytes, de la estructura de **JET_OBJECTINFO** .</span><span class="sxs-lookup"><span data-stu-id="3b2fb-110">The size, in bytes, of the **JET_OBJECTINFO** structure.</span></span>

<span data-ttu-id="3b2fb-111">**objtyp**</span><span class="sxs-lookup"><span data-stu-id="3b2fb-111">**objtyp**</span></span>

<span data-ttu-id="3b2fb-112">Contiene el [JET_OBJTYP](./jet-objtyp.md) de la estructura.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-112">Holds the [JET_OBJTYP](./jet-objtyp.md) of the structure.</span></span> <span data-ttu-id="3b2fb-113">Actualmente solo se devolverán las tablas (es decir, JET_objtypTable).</span><span class="sxs-lookup"><span data-stu-id="3b2fb-113">Currently only tables will be returned (that is, JET_objtypTable).</span></span>

<span data-ttu-id="3b2fb-114">**dtCreate**</span><span class="sxs-lookup"><span data-stu-id="3b2fb-114">**dtCreate**</span></span>

<span data-ttu-id="3b2fb-115">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-115">Obsolete.</span></span> <span data-ttu-id="3b2fb-116">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-116">Do not use.</span></span>

<span data-ttu-id="3b2fb-117">**dtUpdate**</span><span class="sxs-lookup"><span data-stu-id="3b2fb-117">**dtUpdate**</span></span>

<span data-ttu-id="3b2fb-118">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-118">Obsolete.</span></span> <span data-ttu-id="3b2fb-119">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-119">Do not use.</span></span>

<span data-ttu-id="3b2fb-120">**grbit**</span><span class="sxs-lookup"><span data-stu-id="3b2fb-120">**grbit**</span></span>

<span data-ttu-id="3b2fb-121">Grupo de bits que contiene las opciones disponibles para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-121">A group of bits that contain the options that are available for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b2fb-122">Value</span><span class="sxs-lookup"><span data-stu-id="3b2fb-122">Value</span></span></p></th>
<th><p><span data-ttu-id="3b2fb-123">Significado</span><span class="sxs-lookup"><span data-stu-id="3b2fb-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2fb-124">JET_bitTableInfoBookmark</span><span class="sxs-lookup"><span data-stu-id="3b2fb-124">JET_bitTableInfoBookmark</span></span></p></td>
<td><p><span data-ttu-id="3b2fb-125">La tabla puede tener marcadores.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-125">The table can have bookmarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fb-126">JET_bitTableInfoRollback</span><span class="sxs-lookup"><span data-stu-id="3b2fb-126">JET_bitTableInfoRollback</span></span></p></td>
<td><p><span data-ttu-id="3b2fb-127">La tabla se puede revertir.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-127">The table can be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fb-128">JET_bitTableInfoUpdatable</span><span class="sxs-lookup"><span data-stu-id="3b2fb-128">JET_bitTableInfoUpdatable</span></span></p></td>
<td><p><span data-ttu-id="3b2fb-129">Se puede actualizar la tabla.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-129">The table can be updated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b2fb-130">**flags**</span><span class="sxs-lookup"><span data-stu-id="3b2fb-130">**flags**</span></span>

<span data-ttu-id="3b2fb-131">Campo de bits que contiene cero o más de los siguientes marcadores.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-131">A bit field that contains zero or more of the following flags.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b2fb-132">Value</span><span class="sxs-lookup"><span data-stu-id="3b2fb-132">Value</span></span></p></th>
<th><p><span data-ttu-id="3b2fb-133">Significado</span><span class="sxs-lookup"><span data-stu-id="3b2fb-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2fb-134">JET_bitObjectSystem</span><span class="sxs-lookup"><span data-stu-id="3b2fb-134">JET_bitObjectSystem</span></span></p></td>
<td><p><span data-ttu-id="3b2fb-135">La tabla es una tabla del sistema y solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-135">The table is a System Table and is for internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fb-136">JET_bitObjectTableDerived</span><span class="sxs-lookup"><span data-stu-id="3b2fb-136">JET_bitObjectTableDerived</span></span></p></td>
<td><p><span data-ttu-id="3b2fb-137">La tabla DDL heredado de una tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-137">The table inherited DDL from a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fb-138">JET_bitObjectTableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="3b2fb-138">JET_bitObjectTableFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="3b2fb-139">No se puede modificar el DDL de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-139">The DDL for the table cannot be modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fb-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="3b2fb-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="3b2fb-141">Se usa junto con JET_bitObjectTableTemplate para no permitir columnas fijas o variables en las tablas derivadas (de modo que se puedan agregar columnas fijas o de variables a la plantilla en el futuro).</span><span class="sxs-lookup"><span data-stu-id="3b2fb-141">Used in conjunction with JET_bitObjectTableTemplate to disallow fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span></p>
<p><span data-ttu-id="3b2fb-142"><strong>Windows XP:  </strong> Este valor se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-142"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fb-143">JET_bitObjectTableTemplate</span><span class="sxs-lookup"><span data-stu-id="3b2fb-143">JET_bitObjectTableTemplate</span></span></p></td>
<td><p><span data-ttu-id="3b2fb-144">La tabla es una tabla de plantillas.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-144">The table is a template table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b2fb-145">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="3b2fb-145">**cRecord**</span></span>

<span data-ttu-id="3b2fb-146">Número de registros de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-146">The number of records in the table.</span></span>

<span data-ttu-id="3b2fb-147">Este valor se recupera solo si **JET_OBJECTINFO** se pasó a [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="3b2fb-147">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

<span data-ttu-id="3b2fb-148">**cPage**</span><span class="sxs-lookup"><span data-stu-id="3b2fb-148">**cPage**</span></span>

<span data-ttu-id="3b2fb-149">Número de páginas que utiliza la tabla.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-149">The number of pages that are being used by the table.</span></span>

<span data-ttu-id="3b2fb-150">Este valor se recupera solo si **JET_OBJECTINFO** se pasó a [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="3b2fb-150">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="3b2fb-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b2fb-151">Remarks</span></span>

<span data-ttu-id="3b2fb-152">Una estructura de **JET_OBJECTINFO** se rellena mediante una llamada a [JetGetObjectInfo](./jetgetobjectinfo-function.md) o [JetGetTableInfo](./jetgettableinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="3b2fb-152">A **JET_OBJECTINFO** structure gets populated by a call to [JetGetObjectInfo](./jetgetobjectinfo-function.md) or [JetGetTableInfo](./jetgettableinfo-function.md).</span></span> <span data-ttu-id="3b2fb-153">Si la llamada a la API no se realiza correctamente, el contenido de la estructura es indefinido.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-153">If the API call does not succeed, the contents of the structure are undefined.</span></span>

<span data-ttu-id="3b2fb-154">Si procede, las estadísticas de la tabla incluyen el número de registros y el número de páginas que se encuentran en el índice clúster (es decir, el índice que contiene los datos del registro).</span><span class="sxs-lookup"><span data-stu-id="3b2fb-154">If applicable, the table statistics include the number of records and the number of pages that are in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="3b2fb-155">Se tiene acceso a las estadísticas de índice por separado por nombre, mediante [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="3b2fb-155">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="3b2fb-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b2fb-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2fb-157"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fb-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fb-158">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fb-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fb-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fb-160">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fb-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fb-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fb-162">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-162">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3b2fb-163">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3b2fb-163">See Also</span></span>

[<span data-ttu-id="3b2fb-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3b2fb-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3b2fb-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3b2fb-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3b2fb-166">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="3b2fb-166">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="3b2fb-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3b2fb-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3b2fb-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3b2fb-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3b2fb-169">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="3b2fb-169">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="3b2fb-170">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="3b2fb-170">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="3b2fb-171">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="3b2fb-171">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="3b2fb-172">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="3b2fb-172">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
