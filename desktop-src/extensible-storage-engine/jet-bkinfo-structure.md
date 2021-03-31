---
description: 'Más información acerca de: estructura de JET_BKINFO'
title: Estructura de JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278676"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="480b9-103">Estructura de JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="480b9-103">JET_BKINFO Structure</span></span>


<span data-ttu-id="480b9-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="480b9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bkinfo-structure"></a><span data-ttu-id="480b9-105">Estructura de JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="480b9-105">JET_BKINFO Structure</span></span>

<span data-ttu-id="480b9-106">La estructura **JET_BKINFO** contiene una colección de datos acerca de un evento de copia de seguridad específico.</span><span class="sxs-lookup"><span data-stu-id="480b9-106">The **JET_BKINFO** structure holds a collection of data about a specific backup event.</span></span>

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a><span data-ttu-id="480b9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="480b9-107">Members</span></span>

<span data-ttu-id="480b9-108">**lgposMark**</span><span class="sxs-lookup"><span data-stu-id="480b9-108">**lgposMark**</span></span>

<span data-ttu-id="480b9-109">El ID. de esta copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="480b9-109">The ID of this backup.</span></span>

<span data-ttu-id="480b9-110">**logtimeMark**</span><span class="sxs-lookup"><span data-stu-id="480b9-110">**logtimeMark**</span></span>

<span data-ttu-id="480b9-111">Hora de este evento de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="480b9-111">The time of this backup event.</span></span>

<span data-ttu-id="480b9-112">**bklogtimeMark**</span><span class="sxs-lookup"><span data-stu-id="480b9-112">**bklogtimeMark**</span></span>

<span data-ttu-id="480b9-113">Hora de este evento de copia de seguridad, con bits adicionales para indicar una copia de seguridad de instantánea.</span><span class="sxs-lookup"><span data-stu-id="480b9-113">The time of this backup event, with additional bits to indicate a snapshot backup.</span></span>

<span data-ttu-id="480b9-114">**Windows Vista: bklogtimeMark** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="480b9-114">**Windows Vista:  bklogtimeMark** is introduced in Windows Vista.</span></span>

<span data-ttu-id="480b9-115">**genLow**</span><span class="sxs-lookup"><span data-stu-id="480b9-115">**genLow**</span></span>

<span data-ttu-id="480b9-116">Número de generación de registro bajo asociado a este evento de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="480b9-116">The low log generation number associated with this backup event.</span></span>

<span data-ttu-id="480b9-117">**genHigh**</span><span class="sxs-lookup"><span data-stu-id="480b9-117">**genHigh**</span></span>

<span data-ttu-id="480b9-118">Número de generación de registro alto asociado a este evento de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="480b9-118">The high log generation number associated with this backup event.</span></span>

### <a name="remarks"></a><span data-ttu-id="480b9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="480b9-119">Remarks</span></span>

<span data-ttu-id="480b9-120">Esta estructura se utiliza dentro de la estructura [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) para representar datos sobre el evento de copia de seguridad de base de datos.</span><span class="sxs-lookup"><span data-stu-id="480b9-120">This structure is used inside the [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) structure to represent data about the database backup event.</span></span>

### <a name="requirements"></a><span data-ttu-id="480b9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="480b9-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="480b9-122"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="480b9-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="480b9-123">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="480b9-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="480b9-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="480b9-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="480b9-125">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="480b9-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="480b9-126"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="480b9-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="480b9-127">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="480b9-127">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="480b9-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="480b9-128">See Also</span></span>

[<span data-ttu-id="480b9-129">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="480b9-129">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="480b9-130">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="480b9-130">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="480b9-131">JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="480b9-131">JET_BKLOGTIME</span></span>](./jet-bklogtime-structure.md)  
[<span data-ttu-id="480b9-132">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="480b9-132">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
