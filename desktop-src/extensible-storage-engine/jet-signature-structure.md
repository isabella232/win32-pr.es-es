---
description: 'Más información acerca de: estructura de JET_SIGNATURE'
title: Estructura de JET_SIGNATURE
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696610"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="50a24-103">Estructura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="50a24-103">JET_SIGNATURE Structure</span></span>


<span data-ttu-id="50a24-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="50a24-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_signature-structure"></a><span data-ttu-id="50a24-105">Estructura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="50a24-105">JET_SIGNATURE Structure</span></span>

<span data-ttu-id="50a24-106">La estructura **JET_SIGNATURE** contiene información que identifica de forma única una base de datos.</span><span class="sxs-lookup"><span data-stu-id="50a24-106">The **JET_SIGNATURE** structure contains information that uniquely identifies a database.</span></span>

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a><span data-ttu-id="50a24-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="50a24-107">Members</span></span>

<span data-ttu-id="50a24-108">**ulRandom**</span><span class="sxs-lookup"><span data-stu-id="50a24-108">**ulRandom**</span></span>

<span data-ttu-id="50a24-109">Número asignado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="50a24-109">A randomly assigned number.</span></span>

<span data-ttu-id="50a24-110">**logtimeCreate**</span><span class="sxs-lookup"><span data-stu-id="50a24-110">**logtimeCreate**</span></span>

<span data-ttu-id="50a24-111">Se ejecuta el [JET_LOGTIME](./jet-logtime-structure.md) en el momento de [JetCreateDatabase](./jetcreatedatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="50a24-111">The [JET_LOGTIME](./jet-logtime-structure.md) at the time of [JetCreateDatabase](./jetcreatedatabase-function.md) is executed.</span></span>

<span data-ttu-id="50a24-112">**szComputerName**</span><span class="sxs-lookup"><span data-stu-id="50a24-112">**szComputerName**</span></span>

<span data-ttu-id="50a24-113">Valor de cadena opcional del nombre NetBIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="50a24-113">The optional string value of the NetBIOS name for the computer.</span></span> <span data-ttu-id="50a24-114">No se puede establecer este valor.</span><span class="sxs-lookup"><span data-stu-id="50a24-114">This value may not be set.</span></span>

### <a name="remarks"></a><span data-ttu-id="50a24-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50a24-115">Remarks</span></span>

<span data-ttu-id="50a24-116">Se puede encontrar como un elemento de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span><span class="sxs-lookup"><span data-stu-id="50a24-116">This can be found as an element of [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="50a24-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50a24-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50a24-118"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="50a24-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="50a24-119">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="50a24-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50a24-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="50a24-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="50a24-121">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="50a24-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50a24-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="50a24-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="50a24-123">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="50a24-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="50a24-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50a24-124">See Also</span></span>

[<span data-ttu-id="50a24-125">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="50a24-125">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="50a24-126">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="50a24-126">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="50a24-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="50a24-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)
