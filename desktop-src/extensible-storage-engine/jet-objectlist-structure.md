---
description: 'Más información acerca de: estructura de JET_OBJECTLIST'
title: Estructura de JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361102"
---
# <a name="jet_objectlist-structure"></a><span data-ttu-id="173c9-103">Estructura de JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="173c9-103">JET_OBJECTLIST Structure</span></span>


<span data-ttu-id="173c9-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="173c9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectlist-structure"></a><span data-ttu-id="173c9-105">Estructura de JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="173c9-105">JET_OBJECTLIST Structure</span></span>

<span data-ttu-id="173c9-106">La estructura **JET_OBJECTLIST** atraviesa una tabla temporal que se creó con [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-106">The **JET_OBJECTLIST** structure traverses a temporary table that was created with [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span> <span data-ttu-id="173c9-107">Cada fila de la tabla temporal describe un objeto de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="173c9-107">Each row in the temporary table describes an object in the database.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a><span data-ttu-id="173c9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="173c9-108">Members</span></span>

<span data-ttu-id="173c9-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="173c9-109">**cbStruct**</span></span>

<span data-ttu-id="173c9-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="173c9-110">The size of the structure, in bytes.</span></span> <span data-ttu-id="173c9-111">La llamada a la API actualizará este campo, por lo que el llamador debe asegurarse de que este valor coincide con sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="173c9-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="173c9-112">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="173c9-112">**tableid**</span></span>

<span data-ttu-id="173c9-113">Identificador de tabla de la tabla temporal que se creó.</span><span class="sxs-lookup"><span data-stu-id="173c9-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="173c9-114">El autor de la llamada debe contener código que cierre la tabla.</span><span class="sxs-lookup"><span data-stu-id="173c9-114">The caller must contain code that will close the table.</span></span>

<span data-ttu-id="173c9-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="173c9-115">**cRecord**</span></span>

<span data-ttu-id="173c9-116">El número de registros de la tabla temporal que se creó.</span><span class="sxs-lookup"><span data-stu-id="173c9-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="173c9-117">**columnidcontainername**</span><span class="sxs-lookup"><span data-stu-id="173c9-117">**columnidcontainername**</span></span>

<span data-ttu-id="173c9-118">Identificador de columna del nombre del tipo de contenedor.</span><span class="sxs-lookup"><span data-stu-id="173c9-118">The column identifier of the name of the type of container.</span></span>

<span data-ttu-id="173c9-119">Los únicos contenedores que se admiten actualmente son tablas.</span><span class="sxs-lookup"><span data-stu-id="173c9-119">The only containers that are currently supported are tables.</span></span> <span data-ttu-id="173c9-120">Esta columna es un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-120">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="173c9-121">**columnidobjectname**</span><span class="sxs-lookup"><span data-stu-id="173c9-121">**columnidobjectname**</span></span>

<span data-ttu-id="173c9-122">Identificador de columna del nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="173c9-122">The column identifier of the name of the object.</span></span>

<span data-ttu-id="173c9-123">Esta columna es un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-123">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="173c9-124">**columnidobjtyp**</span><span class="sxs-lookup"><span data-stu-id="173c9-124">**columnidobjtyp**</span></span>

<span data-ttu-id="173c9-125">Identificador de columna del tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="173c9-125">The column identifier of the type of the object.</span></span> <span data-ttu-id="173c9-126">Los únicos contenedores que se admiten actualmente son tablas, por lo que este campo se JET_objtypTable.</span><span class="sxs-lookup"><span data-stu-id="173c9-126">The only containers that are currently supported are tables, so this field will be JET_objtypTable.</span></span>

<span data-ttu-id="173c9-127">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-127">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="173c9-128">**columniddtCreate**</span><span class="sxs-lookup"><span data-stu-id="173c9-128">**columniddtCreate**</span></span>

<span data-ttu-id="173c9-129">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="173c9-129">Obsolete.</span></span> <span data-ttu-id="173c9-130">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="173c9-130">Do not use.</span></span>

<span data-ttu-id="173c9-131">**columniddtUpdate**</span><span class="sxs-lookup"><span data-stu-id="173c9-131">**columniddtUpdate**</span></span>

<span data-ttu-id="173c9-132">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="173c9-132">Obsolete.</span></span> <span data-ttu-id="173c9-133">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="173c9-133">Do not use.</span></span>

<span data-ttu-id="173c9-134">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="173c9-134">**columnidgrbit**</span></span>

<span data-ttu-id="173c9-135">Identificador de columna del **grbits** que se aplica al objeto.</span><span class="sxs-lookup"><span data-stu-id="173c9-135">The column identifier of the **grbits** that are applicable to the object.</span></span> <span data-ttu-id="173c9-136">Para obtener una lista de los **grbits** aplicables, consulte [JET_TABLECREATE](./jet-tablecreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-136">For a list of applicable **grbits**, see [JET_TABLECREATE](./jet-tablecreate-structure.md).</span></span>

<span data-ttu-id="173c9-137">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-137">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="173c9-138">**columnidflags**</span><span class="sxs-lookup"><span data-stu-id="173c9-138">**columnidflags**</span></span>

<span data-ttu-id="173c9-139">El identificador de columna de las marcas que se aplican al objeto.</span><span class="sxs-lookup"><span data-stu-id="173c9-139">The column identifier of the flags that are applicable to the object.</span></span> <span data-ttu-id="173c9-140">Para obtener una lista de las marcas aplicables, vea [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-140">For a list of applicable flags, see [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span></span>

<span data-ttu-id="173c9-141">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-141">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="173c9-142">**columnidcRecord**</span><span class="sxs-lookup"><span data-stu-id="173c9-142">**columnidcRecord**</span></span>

<span data-ttu-id="173c9-143">El identificador de columna del número de registros que se encuentran en la tabla con el nombre en **columnidobjectname**.</span><span class="sxs-lookup"><span data-stu-id="173c9-143">The column identifier of the number of records that are present in the table that is named in **columnidobjectname**.</span></span>

<span data-ttu-id="173c9-144">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-144">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="173c9-145">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="173c9-145">**columnidcPage**</span></span>

<span data-ttu-id="173c9-146">Identificador de columna del número de páginas que utiliza el objeto.</span><span class="sxs-lookup"><span data-stu-id="173c9-146">The column identifier of the number of pages the object uses.</span></span>

<span data-ttu-id="173c9-147">Esta columna es un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="173c9-147">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="173c9-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="173c9-148">Remarks</span></span>

<span data-ttu-id="173c9-149">Cada fila de la tabla temporal corresponde a un objeto de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="173c9-149">Each row in the temporary table corresponds to an object in the database.</span></span>

<span data-ttu-id="173c9-150">Cuando se crea la tabla temporal con el parámetro *InfoLevel* en la función [JetGetObjectInfo](./jetgetobjectinfo-function.md) establecida en JET_ObjInfoListNoStats, las columnas identificadas por **columnidcRecord** y **columnidcPage** no contendrán información significativa.</span><span class="sxs-lookup"><span data-stu-id="173c9-150">When the temporary table is created with the *InfoLevel* parameter in the [JetGetObjectInfo](./jetgetobjectinfo-function.md) function set to JET_ObjInfoListNoStats, the columns identified by **columnidcRecord** and **columnidcPage** will not contain meaningful information.</span></span>

<span data-ttu-id="173c9-151">Actualmente, solo la información sobre las tablas estará en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="173c9-151">Currently, only information about tables will be in the temporary table.</span></span>

### <a name="requirements"></a><span data-ttu-id="173c9-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="173c9-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="173c9-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="173c9-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="173c9-154">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="173c9-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="173c9-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="173c9-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="173c9-156">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="173c9-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="173c9-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="173c9-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="173c9-158">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="173c9-158">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="173c9-159">Consulte también</span><span class="sxs-lookup"><span data-stu-id="173c9-159">See Also</span></span>

[<span data-ttu-id="173c9-160">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="173c9-160">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="173c9-161">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="173c9-161">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="173c9-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="173c9-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="173c9-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="173c9-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="173c9-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="173c9-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="173c9-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="173c9-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="173c9-166">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="173c9-166">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="173c9-167">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="173c9-167">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="173c9-168">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="173c9-168">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)
