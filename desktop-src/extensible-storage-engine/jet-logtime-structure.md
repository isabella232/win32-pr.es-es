---
description: 'Más información acerca de: estructura de JET_LOGTIME'
title: Estructura de JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821591"
---
# <a name="jet_logtime-structure"></a><span data-ttu-id="30880-103">Estructura de JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="30880-103">JET_LOGTIME Structure</span></span>


<span data-ttu-id="30880-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="30880-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_logtime-structure"></a><span data-ttu-id="30880-105">Estructura de JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="30880-105">JET_LOGTIME Structure</span></span>

<span data-ttu-id="30880-106">La estructura **JET_LOGTIME** contiene elementos de la fecha y hora de un evento.</span><span class="sxs-lookup"><span data-stu-id="30880-106">The **JET_LOGTIME** structure holds elements of the date and time of an event.</span></span>

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a><span data-ttu-id="30880-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="30880-107">Members</span></span>

<span data-ttu-id="30880-108">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="30880-108">**bSeconds**</span></span>

<span data-ttu-id="30880-109">La hora del evento en segundos.</span><span class="sxs-lookup"><span data-stu-id="30880-109">The time of the event in seconds.</span></span> <span data-ttu-id="30880-110">Este valor puede ser de 0 a 59.</span><span class="sxs-lookup"><span data-stu-id="30880-110">This value can be 0 to 59.</span></span> <span data-ttu-id="30880-111">se usa 0 cuando la estructura es NULL.</span><span class="sxs-lookup"><span data-stu-id="30880-111">0 is used when the structure is null.</span></span>

<span data-ttu-id="30880-112">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="30880-112">**bMinutes**</span></span>

<span data-ttu-id="30880-113">La hora del evento en minutos.</span><span class="sxs-lookup"><span data-stu-id="30880-113">The time of the event in minutes.</span></span> <span data-ttu-id="30880-114">Este valor puede ser de 0 a 59.</span><span class="sxs-lookup"><span data-stu-id="30880-114">This value can be 0 to 59.</span></span> <span data-ttu-id="30880-115">se usa 0 cuando la estructura es NULL.</span><span class="sxs-lookup"><span data-stu-id="30880-115">0 is used when the structure is null.</span></span>

<span data-ttu-id="30880-116">**bHours**</span><span class="sxs-lookup"><span data-stu-id="30880-116">**bHours**</span></span>

<span data-ttu-id="30880-117">La hora del evento en horas.</span><span class="sxs-lookup"><span data-stu-id="30880-117">The time of the event in hours.</span></span> <span data-ttu-id="30880-118">Este valor puede ser de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="30880-118">This value can be 0 to 23.</span></span> <span data-ttu-id="30880-119">se usa 0 cuando la estructura es NULL.</span><span class="sxs-lookup"><span data-stu-id="30880-119">0 is used when the structure is null.</span></span>

<span data-ttu-id="30880-120">**bDay**</span><span class="sxs-lookup"><span data-stu-id="30880-120">**bDay**</span></span>

<span data-ttu-id="30880-121">Día del mes del evento.</span><span class="sxs-lookup"><span data-stu-id="30880-121">The day of the month of the event.</span></span> <span data-ttu-id="30880-122">Este valor puede ser de 0 a 31.</span><span class="sxs-lookup"><span data-stu-id="30880-122">This value can be 0 to 31.</span></span> <span data-ttu-id="30880-123">se usa 0 cuando la estructura es NULL.</span><span class="sxs-lookup"><span data-stu-id="30880-123">0 is used when the structure is null.</span></span>

<span data-ttu-id="30880-124">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="30880-124">**bMonth**</span></span>

<span data-ttu-id="30880-125">Mes del año del evento.</span><span class="sxs-lookup"><span data-stu-id="30880-125">The month of the year of the event.</span></span> <span data-ttu-id="30880-126">Este valor puede ser de 0 a 12.</span><span class="sxs-lookup"><span data-stu-id="30880-126">This value can be 0 to 12.</span></span> <span data-ttu-id="30880-127">se usa 0 cuando la estructura es NULL.</span><span class="sxs-lookup"><span data-stu-id="30880-127">0 is used when the structure is null.</span></span>

<span data-ttu-id="30880-128">**bYear**</span><span class="sxs-lookup"><span data-stu-id="30880-128">**bYear**</span></span>

<span data-ttu-id="30880-129">Año del evento (desplazamiento por 1900).</span><span class="sxs-lookup"><span data-stu-id="30880-129">The year of the event (offset by 1900).</span></span> <span data-ttu-id="30880-130">Para lograr el año real, agregue 1900 a este valor.</span><span class="sxs-lookup"><span data-stu-id="30880-130">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="30880-131">se usa 0 cuando la estructura es NULL.</span><span class="sxs-lookup"><span data-stu-id="30880-131">0 is used when the structure is null.</span></span>

<span data-ttu-id="30880-132">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="30880-132">**bFiller1**</span></span>

<span data-ttu-id="30880-133">Este campo debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="30880-133">This field should be ignored.</span></span>

<span data-ttu-id="30880-134">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="30880-134">**fTimeIsUTC**</span></span>

<span data-ttu-id="30880-135">La hora está en formato UTC.</span><span class="sxs-lookup"><span data-stu-id="30880-135">The time is in UTC format.</span></span>

<span data-ttu-id="30880-136">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="30880-136">**fUnused**</span></span>

<span data-ttu-id="30880-137">Este campo debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="30880-137">This field should be ignored.</span></span>

<span data-ttu-id="30880-138">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="30880-138">**bFiller2**</span></span>

<span data-ttu-id="30880-139">Este campo debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="30880-139">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="30880-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30880-140">Remarks</span></span>

<span data-ttu-id="30880-141">Esta estructura está pensada principalmente para el uso en la depuración.</span><span class="sxs-lookup"><span data-stu-id="30880-141">This structure is meant primarily for usage in debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="30880-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30880-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30880-143"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="30880-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="30880-144">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="30880-144">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30880-145"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="30880-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="30880-146">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="30880-146">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30880-147"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="30880-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="30880-148">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="30880-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="30880-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="30880-149">See Also</span></span>

[<span data-ttu-id="30880-150">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="30880-150">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
