---
description: Contiene información sobre un procesador.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Estructura de PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360696"
---
# <a name="processor_power_information-structure"></a><span data-ttu-id="6855b-103">Estructura de información de \_ energía del procesador \_</span><span class="sxs-lookup"><span data-stu-id="6855b-103">PROCESSOR\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="6855b-104">Contiene información sobre un procesador.</span><span class="sxs-lookup"><span data-stu-id="6855b-104">Contains information about a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="6855b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6855b-105">Syntax</span></span>


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="6855b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6855b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6855b-107">**Number**</span><span class="sxs-lookup"><span data-stu-id="6855b-107">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="6855b-108">El número de procesador del sistema.</span><span class="sxs-lookup"><span data-stu-id="6855b-108">The system processor number.</span></span>

</dd> <dt>

<span data-ttu-id="6855b-109">**MaxMhz**</span><span class="sxs-lookup"><span data-stu-id="6855b-109">**MaxMhz**</span></span>
</dt> <dd>

<span data-ttu-id="6855b-110">La frecuencia de reloj máxima especificada del procesador del sistema, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="6855b-110">The maximum specified clock frequency of the system processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="6855b-111">**CurrentMhz**</span><span class="sxs-lookup"><span data-stu-id="6855b-111">**CurrentMhz**</span></span>
</dt> <dd>

<span data-ttu-id="6855b-112">Frecuencia del reloj del procesador, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="6855b-112">The processor clock frequency, in megahertz.</span></span> <span data-ttu-id="6855b-113">Este número es la frecuencia máxima del reloj del procesador multiplicada por la limitación actual del procesador.</span><span class="sxs-lookup"><span data-stu-id="6855b-113">This number is the maximum specified processor clock frequency multiplied by the current processor throttle.</span></span>

</dd> <dt>

<span data-ttu-id="6855b-114">**MhzLimit**</span><span class="sxs-lookup"><span data-stu-id="6855b-114">**MhzLimit**</span></span>
</dt> <dd>

<span data-ttu-id="6855b-115">Límite de la frecuencia del reloj del procesador, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="6855b-115">The limit on the processor clock frequency, in megahertz.</span></span> <span data-ttu-id="6855b-116">Este número es la frecuencia de reloj de procesador máxima especificada multiplicada por el límite de aceleración térmica del procesador actual.</span><span class="sxs-lookup"><span data-stu-id="6855b-116">This number is the maximum specified processor clock frequency multiplied by the current processor thermal throttle limit.</span></span>

</dd> <dt>

<span data-ttu-id="6855b-117">**MaxIdleState**</span><span class="sxs-lookup"><span data-stu-id="6855b-117">**MaxIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="6855b-118">El estado de inactividad máximo de este procesador.</span><span class="sxs-lookup"><span data-stu-id="6855b-118">The maximum idle state of this processor.</span></span>

</dd> <dt>

<span data-ttu-id="6855b-119">**CurrentIdleState**</span><span class="sxs-lookup"><span data-stu-id="6855b-119">**CurrentIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="6855b-120">Estado de inactividad actual de este procesador.</span><span class="sxs-lookup"><span data-stu-id="6855b-120">The current idle state of this processor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6855b-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6855b-121">Remarks</span></span>

<span data-ttu-id="6855b-122">Tenga en cuenta que esta definición de estructura se omitió accidentalmente en Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="6855b-122">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="6855b-123">Este error se corregirá en el futuro.</span><span class="sxs-lookup"><span data-stu-id="6855b-123">This error will be corrected in the future.</span></span> <span data-ttu-id="6855b-124">Mientras tanto, para compilar la aplicación, incluya la definición de la estructura contenida en este tema en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="6855b-124">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6855b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6855b-125">Requirements</span></span>



| <span data-ttu-id="6855b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6855b-126">Requirement</span></span> | <span data-ttu-id="6855b-127">Value</span><span class="sxs-lookup"><span data-stu-id="6855b-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6855b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6855b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6855b-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6855b-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6855b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6855b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6855b-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6855b-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6855b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6855b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6855b-133">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="6855b-133">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




