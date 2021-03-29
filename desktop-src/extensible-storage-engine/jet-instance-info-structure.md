---
description: 'Más información acerca de: estructura de JET_INSTANCE_INFO'
title: Estructura de JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
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
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912998"
---
# <a name="jet_instance_info-structure"></a><span data-ttu-id="ecc92-103">Estructura de JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="ecc92-103">JET_INSTANCE_INFO Structure</span></span>


<span data-ttu-id="ecc92-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ecc92-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance_info-structure"></a><span data-ttu-id="ecc92-105">Estructura de JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="ecc92-105">JET_INSTANCE_INFO Structure</span></span>

<span data-ttu-id="ecc92-106">La estructura **JET_INSTANCE_INFO** recibe información sobre la ejecución de instancias de base de datos cuando se usa con las funciones [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) y [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc92-106">The **JET_INSTANCE_INFO** structure receives information about running database instances when used with the [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) and [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) functions.</span></span>

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a><span data-ttu-id="ecc92-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ecc92-107">Members</span></span>

<span data-ttu-id="ecc92-108">**hInstanceId**</span><span class="sxs-lookup"><span data-stu-id="ecc92-108">**hInstanceId**</span></span>

<span data-ttu-id="ecc92-109">[JET_INSTANCE](./jet-instance.md) de la instancia de especificada.</span><span class="sxs-lookup"><span data-stu-id="ecc92-109">The [JET_INSTANCE](./jet-instance.md) of the given instance.</span></span>

<span data-ttu-id="ecc92-110">**szInstanceName**</span><span class="sxs-lookup"><span data-stu-id="ecc92-110">**szInstanceName**</span></span>

<span data-ttu-id="ecc92-111">Nombre de la instancia de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ecc92-111">The name of the database instance.</span></span> <span data-ttu-id="ecc92-112">Este valor puede ser **null** si la instancia de no tiene un nombre.</span><span class="sxs-lookup"><span data-stu-id="ecc92-112">This value can be **NULL** if the instance does not have a name.</span></span>

<span data-ttu-id="ecc92-113">**cDatabases**</span><span class="sxs-lookup"><span data-stu-id="ecc92-113">**cDatabases**</span></span>

<span data-ttu-id="ecc92-114">El número de bases de datos que se adjuntan a la instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="ecc92-114">The number of databases that are attached to the database instance.</span></span> <span data-ttu-id="ecc92-115">**cDatabases** también contiene el tamaño de las matrices de cadenas que se devuelven en **szDatabaseFileName**, **szDatabaseDisplayName** y **szDatabaseSLVFileName**.</span><span class="sxs-lookup"><span data-stu-id="ecc92-115">**cDatabases** also holds the size of the arrays of strings that are returned in **szDatabaseFileName**, **szDatabaseDisplayName**, and **szDatabaseSLVFileName**.</span></span>

<span data-ttu-id="ecc92-116">**szDatabaseFileName**</span><span class="sxs-lookup"><span data-stu-id="ecc92-116">**szDatabaseFileName**</span></span>

<span data-ttu-id="ecc92-117">Matriz de cadenas, cada una de las cuales contiene el nombre de archivo de una base de datos que se adjunta a la instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="ecc92-117">An array of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="ecc92-118">La matriz tiene elementos **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="ecc92-118">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="ecc92-119">**szDatabaseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="ecc92-119">**szDatabaseDisplayName**</span></span>

<span data-ttu-id="ecc92-120">Matriz de cadenas, cada una de las cuales contiene el nombre para mostrar de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="ecc92-120">An array of strings, each holding the display name of a database.</span></span> <span data-ttu-id="ecc92-121">Actualmente, la cadena puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ecc92-121">Currently the string can be NULL.</span></span> <span data-ttu-id="ecc92-122">La matriz tiene elementos **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="ecc92-122">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="ecc92-123">**szDatabaseSLVFileName**</span><span class="sxs-lookup"><span data-stu-id="ecc92-123">**szDatabaseSLVFileName**</span></span>

<span data-ttu-id="ecc92-124">Matriz de cadenas, cada una de las cuales contiene el nombre del archivo SLV que está asociado a la instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="ecc92-124">An array of strings, each holding the file name of the SLV file that is attached to the database instance.</span></span> <span data-ttu-id="ecc92-125">La matriz tiene elementos **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="ecc92-125">The array has **cDatabases** elements.</span></span> <span data-ttu-id="ecc92-126">No se admiten archivos SLV, por lo que este campo debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="ecc92-126">SLV files are not supported, so this field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="ecc92-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecc92-127">Remarks</span></span>

<span data-ttu-id="ecc92-128">Cada instancia de base de datos puede tener varias bases de datos asociadas.</span><span class="sxs-lookup"><span data-stu-id="ecc92-128">Each database instance can have several databases attached to it.</span></span>

<span data-ttu-id="ecc92-129">Para una estructura de **JET_INSTANCE_INFO** determinada, la matriz de cadenas que se devuelve para las bases de datos está en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="ecc92-129">For a given **JET_INSTANCE_INFO** structure, the array of strings that is returned for the databases are in the same order.</span></span> <span data-ttu-id="ecc92-130">Por ejemplo, "szDatabaseDisplayName \[ i \] " y "szDatabaseFileName \[ i \] " hacen referencia a la misma base de datos.</span><span class="sxs-lookup"><span data-stu-id="ecc92-130">For example, "szDatabaseDisplayName\[ i \]" and "szDatabaseFileName\[ i \]" both refer to the same database.</span></span>

### <a name="requirements"></a><span data-ttu-id="ecc92-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecc92-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecc92-132"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ecc92-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ecc92-133">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ecc92-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecc92-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ecc92-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ecc92-135">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ecc92-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecc92-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ecc92-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ecc92-137">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="ecc92-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecc92-138"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ecc92-138"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ecc92-139">Se implementa como <strong>JET_INSTANCE_INFO_W</strong> (Unicode) y <strong>JET_INSTANCE_INFO _a</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ecc92-139">Implemented as <strong>JET_INSTANCE_INFO_W</strong> (Unicode) and <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ecc92-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ecc92-140">See Also</span></span>

[<span data-ttu-id="ecc92-141">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="ecc92-141">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="ecc92-142">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ecc92-142">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ecc92-143">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="ecc92-143">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="ecc92-144">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="ecc92-144">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)
