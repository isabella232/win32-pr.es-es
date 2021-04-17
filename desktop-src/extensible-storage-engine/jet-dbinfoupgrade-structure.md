---
description: 'Más información acerca de: estructura de JET_DBINFOUPGRADE'
title: Estructura de JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686763"
---
# <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="96a0a-103">Estructura de JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="96a0a-103">JET_DBINFOUPGRADE Structure</span></span>


<span data-ttu-id="96a0a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="96a0a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="96a0a-105">Estructura de JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="96a0a-105">JET_DBINFOUPGRADE Structure</span></span>

<span data-ttu-id="96a0a-106">La estructura **JET_DBINFOUPGRADE** contiene información sobre el estado de actualización de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="96a0a-106">The **JET_DBINFOUPGRADE** structure holds information about the upgrade status of the database.</span></span> <span data-ttu-id="96a0a-107">Este valor se recupera solo si **JET_DBINFOUPGRADE** se pasó a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="96a0a-107">This value is retrieved only if **JET_DBINFOUPGRADE** was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="96a0a-108">Esta estructura no es necesaria para las versiones actuales del sistema operativo del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="96a0a-108">This structure is not required for current operating system versions of the database engine.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a><span data-ttu-id="96a0a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="96a0a-109">Members</span></span>

<span data-ttu-id="96a0a-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="96a0a-110">**cbStruct**</span></span>

<span data-ttu-id="96a0a-111">Se establece en el tamaño de la estructura **JET_DBINFOUPGRADE** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="96a0a-111">Set to the size of the **JET_DBINFOUPGRADE** structure, in bytes.</span></span>

<span data-ttu-id="96a0a-112">**cbFilesizeLow**</span><span class="sxs-lookup"><span data-stu-id="96a0a-112">**cbFilesizeLow**</span></span>

<span data-ttu-id="96a0a-113">**Valor DWORD** inferior que refleja el tamaño actual del archivo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="96a0a-113">The low **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="96a0a-114">**cbFilesizeHigh**</span><span class="sxs-lookup"><span data-stu-id="96a0a-114">**cbFilesizeHigh**</span></span>

<span data-ttu-id="96a0a-115">**Valor DWORD** alto que refleja el tamaño actual del archivo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="96a0a-115">The high **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="96a0a-116">**cbFreeSpaceRequiredLow**</span><span class="sxs-lookup"><span data-stu-id="96a0a-116">**cbFreeSpaceRequiredLow**</span></span>

<span data-ttu-id="96a0a-117">**Valor DWORD** inferior del espacio libre en disco estimado necesario para una actualización en contexto.</span><span class="sxs-lookup"><span data-stu-id="96a0a-117">The low **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="96a0a-118">**cbFreeSpaceRequiredHigh**</span><span class="sxs-lookup"><span data-stu-id="96a0a-118">**cbFreeSpaceRequiredHigh**</span></span>

<span data-ttu-id="96a0a-119">**Valor DWORD** alto del espacio libre en disco estimado necesario para una actualización en contexto.</span><span class="sxs-lookup"><span data-stu-id="96a0a-119">The high **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="96a0a-120">**csecToUpgrade**</span><span class="sxs-lookup"><span data-stu-id="96a0a-120">**csecToUpgrade**</span></span>

<span data-ttu-id="96a0a-121">El tiempo estimado necesario para la actualización, en segundos.</span><span class="sxs-lookup"><span data-stu-id="96a0a-121">The estimated time required to upgrade, in seconds.</span></span>

<span data-ttu-id="96a0a-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="96a0a-122">**ulFlags**</span></span>

<span data-ttu-id="96a0a-123">Un campo de bits formado por cero o más de las marcas siguientes: **fUpgradable**, **fAlreadyUpgraded**.</span><span class="sxs-lookup"><span data-stu-id="96a0a-123">A bit field made of zero or more of the following flags: **fUpgradable**, **fAlreadyUpgraded**.</span></span>

<span data-ttu-id="96a0a-124">**fUpgradable**</span><span class="sxs-lookup"><span data-stu-id="96a0a-124">**fUpgradable**</span></span>

<span data-ttu-id="96a0a-125">La base de datos es actualizable.</span><span class="sxs-lookup"><span data-stu-id="96a0a-125">The database is upgradeable.</span></span>

<span data-ttu-id="96a0a-126">**fAlreadyUpgraded**</span><span class="sxs-lookup"><span data-stu-id="96a0a-126">**fAlreadyUpgraded**</span></span>

<span data-ttu-id="96a0a-127">La base de datos se actualiza al formato de base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="96a0a-127">The database is upgraded to the current database format.</span></span>

### <a name="remarks"></a><span data-ttu-id="96a0a-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96a0a-128">Remarks</span></span>

<span data-ttu-id="96a0a-129">Una **JET_DBINFOUPGRADE** estructura se rellena mediante una llamada a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="96a0a-129">A **JET_DBINFOUPGRADE** structure is populated by a call to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="96a0a-130">Si la función no se ejecuta correctamente, el contenido de la estructura es indefinido.</span><span class="sxs-lookup"><span data-stu-id="96a0a-130">If the function does not succeed, the contents of the structure are undefined.</span></span>

### <a name="requirements"></a><span data-ttu-id="96a0a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96a0a-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96a0a-132"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="96a0a-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="96a0a-133">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="96a0a-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96a0a-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="96a0a-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="96a0a-135">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="96a0a-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96a0a-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="96a0a-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="96a0a-137">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="96a0a-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="96a0a-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="96a0a-138">See Also</span></span>

[<span data-ttu-id="96a0a-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="96a0a-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="96a0a-140">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="96a0a-140">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="96a0a-141">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="96a0a-141">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="96a0a-142">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="96a0a-142">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="96a0a-143">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="96a0a-143">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="96a0a-144">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="96a0a-144">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="96a0a-145">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="96a0a-145">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="96a0a-146">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="96a0a-146">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
