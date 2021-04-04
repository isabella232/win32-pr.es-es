---
description: 'Más información acerca de: estructura de JET_CONVERT'
title: Estructura de JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908258"
---
# <a name="jet_convert-structure"></a><span data-ttu-id="1d9b6-103">Estructura de JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="1d9b6-103">JET_CONVERT Structure</span></span>


<span data-ttu-id="1d9b6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d9b6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_convert-structure"></a><span data-ttu-id="1d9b6-105">Estructura de JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="1d9b6-105">JET_CONVERT Structure</span></span>

<span data-ttu-id="1d9b6-106">La estructura **JET_CONVERT** contiene el nombre de una DLL de la versión de ese anterior que se usa para leer las bases de datos que se crean con esa versión anterior.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-106">The **JET_CONVERT** structure contains the name of an earlier ESE version DLL that is used for reading a databases that are created with that earlier version.</span></span> <span data-ttu-id="1d9b6-107">Además, se proporcionan otras marcas para controlar la naturaleza de la conversión.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-107">In addition, other flags are provided to control the nature of the conversion.</span></span>

<span data-ttu-id="1d9b6-108">**Windows Server 2003:** La característica de [JetCompact](./jetcompact-function.md) que realizó una conversión se ha quitado del producto en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-108">**Windows Server 2003:** The feature in [JetCompact](./jetcompact-function.md) that performed a conversion was removed from the product in Windows Server 2003.</span></span> <span data-ttu-id="1d9b6-109">Solo se admite en Windows 2000 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-109">It is only supported in Windows 2000 and Windows XP.</span></span>

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a><span data-ttu-id="1d9b6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d9b6-110">Members</span></span>

<span data-ttu-id="1d9b6-111">**SzOldDll**</span><span class="sxs-lookup"><span data-stu-id="1d9b6-111">**SzOldDll**</span></span>

<span data-ttu-id="1d9b6-112">El nombre, incluida la información de la ruta de acceso, a la versión anterior de la DLL de ESE.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-112">The name, including path information, to the earlier version of the ESE DLL.</span></span>

<span data-ttu-id="1d9b6-113">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="1d9b6-113">**fFlags**</span></span>

<span data-ttu-id="1d9b6-114">Reservado para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-114">Reserved for system use.</span></span>

<span data-ttu-id="1d9b6-115">**fSchemaChangesOnly**</span><span class="sxs-lookup"><span data-stu-id="1d9b6-115">**fSchemaChangesOnly**</span></span>

<span data-ttu-id="1d9b6-116">Reservado para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-116">Reserved for system use.</span></span>

### <a name="requirements"></a><span data-ttu-id="1d9b6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d9b6-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d9b6-118"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1d9b6-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1d9b6-119">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9b6-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1d9b6-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1d9b6-121">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d9b6-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1d9b6-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1d9b6-123">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-123">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d9b6-124"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1d9b6-124"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1d9b6-125">Se implementa como <strong>JET_CONVERT_W</strong> (Unicode) y <strong>JET_CONVERT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1d9b6-125">Implemented as <strong>JET_CONVERT_W</strong> (Unicode) and <strong>JET_CONVERT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1d9b6-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1d9b6-126">See Also</span></span>

[<span data-ttu-id="1d9b6-127">JetCompact</span><span class="sxs-lookup"><span data-stu-id="1d9b6-127">JetCompact</span></span>](./jetcompact-function.md)
