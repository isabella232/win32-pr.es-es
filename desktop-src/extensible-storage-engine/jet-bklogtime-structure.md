---
description: 'Más información acerca de: estructura de JET_BKLOGTIME'
title: Estructura de JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697532"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="3c19f-103">Estructura de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="3c19f-103">JET_BKLOGTIME Structure</span></span>


<span data-ttu-id="3c19f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3c19f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bklogtime-structure"></a><span data-ttu-id="3c19f-105">Estructura de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="3c19f-105">JET_BKLOGTIME Structure</span></span>

<span data-ttu-id="3c19f-106">La estructura **JET_BKLOGTIME** contiene los elementos de fecha y hora de un evento.</span><span class="sxs-lookup"><span data-stu-id="3c19f-106">The **JET_BKLOGTIME** structure holds the date and time elements of an event.</span></span> <span data-ttu-id="3c19f-107">Es una extensión de [JET_LOGTIME](./jet-logtime-structure.md).</span><span class="sxs-lookup"><span data-stu-id="3c19f-107">It is an extension of [JET_LOGTIME](./jet-logtime-structure.md).</span></span>

<span data-ttu-id="3c19f-108">**Windows Vista: JET_BKLOGTIME** se incorpora en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3c19f-108">**Windows Vista:  JET_BKLOGTIME** is introduced in Windows Vista.</span></span>

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a><span data-ttu-id="3c19f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c19f-109">Members</span></span>

<span data-ttu-id="3c19f-110">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="3c19f-110">**bSeconds**</span></span>

<span data-ttu-id="3c19f-111">La hora del evento en segundos.</span><span class="sxs-lookup"><span data-stu-id="3c19f-111">The time of the event in seconds.</span></span> <span data-ttu-id="3c19f-112">Puede ser 0 (cero) a 60.</span><span class="sxs-lookup"><span data-stu-id="3c19f-112">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="3c19f-113">se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".</span><span class="sxs-lookup"><span data-stu-id="3c19f-113">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="3c19f-114">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="3c19f-114">**bMinutes**</span></span>

<span data-ttu-id="3c19f-115">La hora del evento en minutos.</span><span class="sxs-lookup"><span data-stu-id="3c19f-115">The time of the event in minutes.</span></span> <span data-ttu-id="3c19f-116">Puede ser 0 (cero) a 60.</span><span class="sxs-lookup"><span data-stu-id="3c19f-116">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="3c19f-117">se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".</span><span class="sxs-lookup"><span data-stu-id="3c19f-117">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="3c19f-118">**bHours**</span><span class="sxs-lookup"><span data-stu-id="3c19f-118">**bHours**</span></span>

<span data-ttu-id="3c19f-119">La hora del evento en horas.</span><span class="sxs-lookup"><span data-stu-id="3c19f-119">The time of the event in hours.</span></span> <span data-ttu-id="3c19f-120">Puede ser 0 (cero) a 24.</span><span class="sxs-lookup"><span data-stu-id="3c19f-120">This can be 0 (zero) to 24.</span></span> <span data-ttu-id="3c19f-121">se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".</span><span class="sxs-lookup"><span data-stu-id="3c19f-121">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="3c19f-122">**bDay**</span><span class="sxs-lookup"><span data-stu-id="3c19f-122">**bDay**</span></span>

<span data-ttu-id="3c19f-123">Día del mes del evento.</span><span class="sxs-lookup"><span data-stu-id="3c19f-123">The day of the month of the event.</span></span> <span data-ttu-id="3c19f-124">Puede ser 0 (cero) a 31.</span><span class="sxs-lookup"><span data-stu-id="3c19f-124">This can be 0 (zero) to 31.</span></span> <span data-ttu-id="3c19f-125">se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".</span><span class="sxs-lookup"><span data-stu-id="3c19f-125">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="3c19f-126">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="3c19f-126">**bMonth**</span></span>

<span data-ttu-id="3c19f-127">Mes del año del evento.</span><span class="sxs-lookup"><span data-stu-id="3c19f-127">The month of the year of the event.</span></span> <span data-ttu-id="3c19f-128">Puede ser 0 (cero) a 12.</span><span class="sxs-lookup"><span data-stu-id="3c19f-128">This can be 0 (zero) to 12.</span></span> <span data-ttu-id="3c19f-129">se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".</span><span class="sxs-lookup"><span data-stu-id="3c19f-129">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="3c19f-130">**bYear**</span><span class="sxs-lookup"><span data-stu-id="3c19f-130">**bYear**</span></span>

<span data-ttu-id="3c19f-131">Año (desplazamiento por 1900) del evento.</span><span class="sxs-lookup"><span data-stu-id="3c19f-131">The year (offset by 1900) of the event.</span></span> <span data-ttu-id="3c19f-132">Para lograr el año real, agregue 1900 a este valor.</span><span class="sxs-lookup"><span data-stu-id="3c19f-132">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="3c19f-133">se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".</span><span class="sxs-lookup"><span data-stu-id="3c19f-133">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="3c19f-134">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="3c19f-134">**bFiller1**</span></span>

<span data-ttu-id="3c19f-135">Este campo debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="3c19f-135">This field should be ignored.</span></span>

<span data-ttu-id="3c19f-136">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="3c19f-136">**fTimeIsUTC**</span></span>

<span data-ttu-id="3c19f-137">La hora está en formato UTC.</span><span class="sxs-lookup"><span data-stu-id="3c19f-137">The time is in UTC format.</span></span>

<span data-ttu-id="3c19f-138">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="3c19f-138">**fUnused**</span></span>

<span data-ttu-id="3c19f-139">Este campo debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="3c19f-139">This field should be ignored.</span></span>

<span data-ttu-id="3c19f-140">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="3c19f-140">**bFiller2**</span></span>

<span data-ttu-id="3c19f-141">Este campo debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="3c19f-141">This field should be ignored.</span></span>

<span data-ttu-id="3c19f-142">**fOSSnapshot**</span><span class="sxs-lookup"><span data-stu-id="3c19f-142">**fOSSnapshot**</span></span>

<span data-ttu-id="3c19f-143">Si este evento es una copia de seguridad, esta marca contiene uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="3c19f-143">If this event is a backup, this flag contains one of the following possible values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c19f-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="3c19f-144">Name</span></span></p></th>
<th><p><span data-ttu-id="3c19f-145">Value</span><span class="sxs-lookup"><span data-stu-id="3c19f-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c19f-146">copia de seguridad de streaming</span><span class="sxs-lookup"><span data-stu-id="3c19f-146">streaming backup</span></span></p></td>
<td><p><span data-ttu-id="3c19f-147">0 (cero)</span><span class="sxs-lookup"><span data-stu-id="3c19f-147">0 (zero)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c19f-148">copia de seguridad de instantánea</span><span class="sxs-lookup"><span data-stu-id="3c19f-148">snapshot backup</span></span></p></td>
<td><p><span data-ttu-id="3c19f-149">1</span><span class="sxs-lookup"><span data-stu-id="3c19f-149">1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3c19f-150">**fReserved**</span><span class="sxs-lookup"><span data-stu-id="3c19f-150">**fReserved**</span></span>

<span data-ttu-id="3c19f-151">Este campo debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="3c19f-151">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="3c19f-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c19f-152">Remarks</span></span>

<span data-ttu-id="3c19f-153">Esta estructura se utiliza al depurar.</span><span class="sxs-lookup"><span data-stu-id="3c19f-153">This structure is used when debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="3c19f-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c19f-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c19f-155"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3c19f-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3c19f-156">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3c19f-156">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c19f-157"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3c19f-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3c19f-158">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3c19f-158">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c19f-159"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3c19f-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3c19f-160">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="3c19f-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3c19f-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3c19f-161">See Also</span></span>

[<span data-ttu-id="3c19f-162">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="3c19f-162">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="3c19f-163">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="3c19f-163">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
