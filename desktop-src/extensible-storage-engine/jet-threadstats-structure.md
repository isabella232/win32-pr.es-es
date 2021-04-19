---
description: 'Más información acerca de: estructura de JET_THREADSTATS'
title: Estructura de JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706894"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="61aa6-103">Estructura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="61aa6-103">JET_THREADSTATS Structure</span></span>


<span data-ttu-id="61aa6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="61aa6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_threadstats-structure"></a><span data-ttu-id="61aa6-105">Estructura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="61aa6-105">JET_THREADSTATS Structure</span></span>

<span data-ttu-id="61aa6-106">La estructura **JET_THREADSTATS** contiene estadísticas acumuladas sobre el trabajo realizado por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="61aa6-106">The **JET_THREADSTATS** structure contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="61aa6-107">Esta información se devuelve a través de [JetGetThreadStats](./jetgetthreadstats-function.md).</span><span class="sxs-lookup"><span data-stu-id="61aa6-107">This information is returned via [JetGetThreadStats](./jetgetthreadstats-function.md).</span></span>

<span data-ttu-id="61aa6-108">**Windows Vista:**  La estructura de **JET_THREADSTATS** se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61aa6-108">**Windows Vista:**  The **JET_THREADSTATS** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a><span data-ttu-id="61aa6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="61aa6-109">Members</span></span>

<span data-ttu-id="61aa6-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="61aa6-110">**cbStruct**</span></span>

<span data-ttu-id="61aa6-111">Tamaño de la estructura de **JET_THREADSTATS** devuelta, en bytes.</span><span class="sxs-lookup"><span data-stu-id="61aa6-111">The size of the returned **JET_THREADSTATS** structure, in bytes.</span></span>

<span data-ttu-id="61aa6-112">**Nota:**  La estructura de **JET_THREADSTATS** se expandirá en el futuro para que contenga más estadísticas.</span><span class="sxs-lookup"><span data-stu-id="61aa6-112">**Note**  The **JET_THREADSTATS** structure will expand in the future to contain more statistics.</span></span> <span data-ttu-id="61aa6-113">Las nuevas estadísticas se agregarán al final de la estructura y se pueden recuperar con un mayor tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="61aa6-113">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="61aa6-114">La presencia de estadísticas adicionales se puede inferir con un valor de **cbStruct** mayor.</span><span class="sxs-lookup"><span data-stu-id="61aa6-114">The presence of additional statistics can be inferred by a larger **cbStruct** value.</span></span>

<span data-ttu-id="61aa6-115">**cPageReferenced**</span><span class="sxs-lookup"><span data-stu-id="61aa6-115">**cPageReferenced**</span></span>

<span data-ttu-id="61aa6-116">Número total de páginas de base de datos visitadas por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="61aa6-116">The total number of database pages visited by the database engine on the current thread.</span></span>

<span data-ttu-id="61aa6-117">**cPageRead**</span><span class="sxs-lookup"><span data-stu-id="61aa6-117">**cPageRead**</span></span>

<span data-ttu-id="61aa6-118">Número total de páginas de base de datos capturadas desde el disco por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="61aa6-118">The total number of database pages fetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="61aa6-119">**cPagePreread**</span><span class="sxs-lookup"><span data-stu-id="61aa6-119">**cPagePreread**</span></span>

<span data-ttu-id="61aa6-120">Número total de páginas de base de datos capturadas previamente desde el disco por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="61aa6-120">The total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="61aa6-121">**cPageDirtied**</span><span class="sxs-lookup"><span data-stu-id="61aa6-121">**cPageDirtied**</span></span>

<span data-ttu-id="61aa6-122">El número total de páginas de base de datos, sin cambios no escritos, modificados por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="61aa6-122">The total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="61aa6-123">**cPageRedirtied**</span><span class="sxs-lookup"><span data-stu-id="61aa6-123">**cPageRedirtied**</span></span>

<span data-ttu-id="61aa6-124">El número total de páginas de base de datos, con cambios sin escribir, modificados por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="61aa6-124">The total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="61aa6-125">**cLogRecord**</span><span class="sxs-lookup"><span data-stu-id="61aa6-125">**cLogRecord**</span></span>

<span data-ttu-id="61aa6-126">Número total de entradas del registro de transacciones generadas por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="61aa6-126">The total number of transaction log records that have been generated by the database engine on the current thread.</span></span>

<span data-ttu-id="61aa6-127">**cbLogRecord**</span><span class="sxs-lookup"><span data-stu-id="61aa6-127">**cbLogRecord**</span></span>

<span data-ttu-id="61aa6-128">Tamaño total en bytes de las entradas del registro de transacciones generadas por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="61aa6-128">The total size in bytes of transaction log records that have been generated by the database engine on the current thread.</span></span>

### <a name="requirements"></a><span data-ttu-id="61aa6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61aa6-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61aa6-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="61aa6-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="61aa6-131">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61aa6-131">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61aa6-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="61aa6-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="61aa6-133">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="61aa6-133">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61aa6-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="61aa6-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="61aa6-135">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="61aa6-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="61aa6-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="61aa6-136">See Also</span></span>

[<span data-ttu-id="61aa6-137">JetGetThreadStats</span><span class="sxs-lookup"><span data-stu-id="61aa6-137">JetGetThreadStats</span></span>](./jetgetthreadstats-function.md)
