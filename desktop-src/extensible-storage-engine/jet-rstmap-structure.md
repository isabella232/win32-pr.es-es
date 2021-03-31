---
description: 'Más información acerca de: estructura de JET_RSTMAP'
title: Estructura de JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809067"
---
# <a name="jet_rstmap-structure"></a><span data-ttu-id="ec5b3-103">Estructura de JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="ec5b3-103">JET_RSTMAP Structure</span></span>


<span data-ttu-id="ec5b3-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ec5b3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstmap-structure"></a><span data-ttu-id="ec5b3-105">Estructura de JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="ec5b3-105">JET_RSTMAP Structure</span></span>

<span data-ttu-id="ec5b3-106">La estructura **JET_RSTMAP** habilita la reasignación de las rutas de acceso de archivos de base de datos que se almacenan en los registros de transacciones durante la recuperación, cuando las funciones [JetInit](./jetinit-function.md) y [JetExternalRestore](./jetexternalrestore-function.md) las utilizan.</span><span class="sxs-lookup"><span data-stu-id="ec5b3-106">The **JET_RSTMAP** structure enables the remapping of database file paths that are stored in the transaction logs during recovery, when used by the [JetInit](./jetinit-function.md) and [JetExternalRestore](./jetexternalrestore-function.md) functions.</span></span> <span data-ttu-id="ec5b3-107">Esto permite que las bases de datos se muevan cuando estén sin conexión o cuando se restauren desde la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ec5b3-107">This enables the databases to be moved when offline or when restored from backup.</span></span>

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a><span data-ttu-id="ec5b3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec5b3-108">Members</span></span>

<span data-ttu-id="ec5b3-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="ec5b3-109">**szDatabaseName**</span></span>

<span data-ttu-id="ec5b3-110">La ruta de acceso absoluta actual de una base de datos que está asociada a los registros de transacciones que se reproducen durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="ec5b3-110">The current absolute path of a database that is associated with the transaction logs that are replayed during recovery.</span></span>

<span data-ttu-id="ec5b3-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="ec5b3-111">**szNewDatabaseName**</span></span>

<span data-ttu-id="ec5b3-112">Nueva ruta de acceso absoluta para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ec5b3-112">The new absolute path for the database.</span></span>

### <a name="requirements"></a><span data-ttu-id="ec5b3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec5b3-113">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec5b3-114"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ec5b3-114"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ec5b3-115">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ec5b3-115">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec5b3-116"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ec5b3-116"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ec5b3-117">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ec5b3-117">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec5b3-118"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ec5b3-118"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ec5b3-119">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="ec5b3-119">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec5b3-120"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ec5b3-120"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ec5b3-121">Se implementa como <strong>JET_RSTMAP_W</strong> (Unicode) y <strong>JET_RSTMAP_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ec5b3-121">Implemented as <strong>JET_RSTMAP_W</strong> (Unicode) and <strong>JET_RSTMAP_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ec5b3-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ec5b3-122">See Also</span></span>

[<span data-ttu-id="ec5b3-123">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="ec5b3-123">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="ec5b3-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="ec5b3-124">JetInit</span></span>](./jetinit-function.md)
