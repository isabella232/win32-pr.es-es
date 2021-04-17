---
description: Contiene la fecha de fabricación de una batería.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: BATTERY_MANUFACTURE_DATE estructura (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667223"
---
# <a name="battery_manufacture_date-structure"></a><span data-ttu-id="c4de5-103">Estructura de fecha de \_ fabricación de la batería \_</span><span class="sxs-lookup"><span data-stu-id="c4de5-103">BATTERY\_MANUFACTURE\_DATE structure</span></span>

<span data-ttu-id="c4de5-104">Contiene la fecha de fabricación de una batería.</span><span class="sxs-lookup"><span data-stu-id="c4de5-104">Contains the date of manufacture of a battery.</span></span> <span data-ttu-id="c4de5-105">La estructura de [**\_ \_ información de consulta**](battery-query-information-str.md) de la batería usa esta estructura cuando se solicita el nivel de información de BatteryManufactureDate.</span><span class="sxs-lookup"><span data-stu-id="c4de5-105">This structure is used by the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure when the BatteryManufactureDate information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4de5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4de5-106">Syntax</span></span>


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a><span data-ttu-id="c4de5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4de5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4de5-108">**Day**</span><span class="sxs-lookup"><span data-stu-id="c4de5-108">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="c4de5-109">Día del mes de fabricación, en el intervalo de 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="c4de5-109">The day of the month of manufacture, in the range 1 to 31.</span></span> <span data-ttu-id="c4de5-110">A pesar del tipo de datos, no es un valor codificado en ASCII.</span><span class="sxs-lookup"><span data-stu-id="c4de5-110">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="c4de5-111">Es un byte sin signo.</span><span class="sxs-lookup"><span data-stu-id="c4de5-111">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="c4de5-112">**Mensuales**</span><span class="sxs-lookup"><span data-stu-id="c4de5-112">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="c4de5-113">El mes de fabricación, en el intervalo de 1 (enero) a 12 (diciembre).</span><span class="sxs-lookup"><span data-stu-id="c4de5-113">The month of manufacture, in the range 1 (January) to 12 (December).</span></span> <span data-ttu-id="c4de5-114">A pesar del tipo de datos, no es un valor codificado en ASCII.</span><span class="sxs-lookup"><span data-stu-id="c4de5-114">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="c4de5-115">Es un byte sin signo.</span><span class="sxs-lookup"><span data-stu-id="c4de5-115">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="c4de5-116">**Anual**</span><span class="sxs-lookup"><span data-stu-id="c4de5-116">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="c4de5-117">Año de fabricación.</span><span class="sxs-lookup"><span data-stu-id="c4de5-117">The year of manufacture.</span></span> <span data-ttu-id="c4de5-118">Normalmente estará en el intervalo 1900-2100.</span><span class="sxs-lookup"><span data-stu-id="c4de5-118">This will typically be in the range 1900-2100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4de5-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4de5-119">Remarks</span></span>

<span data-ttu-id="c4de5-120">La fecha se codifica en el formato de calendario gregoriano o occidental.</span><span class="sxs-lookup"><span data-stu-id="c4de5-120">The date is encoded in the Gregorian or western calendar format.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4de5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4de5-121">Requirements</span></span>



| <span data-ttu-id="c4de5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4de5-122">Requirement</span></span> | <span data-ttu-id="c4de5-123">Value</span><span class="sxs-lookup"><span data-stu-id="c4de5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4de5-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4de5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4de5-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c4de5-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="c4de5-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4de5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4de5-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4de5-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="c4de5-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4de5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4de5-129"><dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="c4de5-129"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4de5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4de5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4de5-131">**\_información de consulta de la batería \_**</span><span class="sxs-lookup"><span data-stu-id="c4de5-131">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="c4de5-132">**\_información de \_ consulta de batería ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="c4de5-132">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




