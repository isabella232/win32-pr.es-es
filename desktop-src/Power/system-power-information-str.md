---
description: Contiene información sobre la inactividad del sistema.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Estructura de SYSTEM_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001948"
---
# <a name="system_power_information-structure"></a><span data-ttu-id="c24a9-103">Estructura de información de \_ energía del sistema \_</span><span class="sxs-lookup"><span data-stu-id="c24a9-103">SYSTEM\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="c24a9-104">Contiene información sobre la inactividad del sistema.</span><span class="sxs-lookup"><span data-stu-id="c24a9-104">Contains information about the idleness of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c24a9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c24a9-105">Syntax</span></span>


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="c24a9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c24a9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c24a9-107">**MaxIdlenessAllowed**</span><span class="sxs-lookup"><span data-stu-id="c24a9-107">**MaxIdlenessAllowed**</span></span>
</dt> <dd>

<span data-ttu-id="c24a9-108">La inactividad en la que se considera que el sistema está inactivo y el tiempo de espera de inactividad comienza el recuento, expresado en forma de porcentaje.</span><span class="sxs-lookup"><span data-stu-id="c24a9-108">The idleness at which the system is considered idle and the idle time-out begins counting, expressed as a percentage.</span></span> <span data-ttu-id="c24a9-109">Si se coloca debajo de este número, se cancela el temporizador.</span><span class="sxs-lookup"><span data-stu-id="c24a9-109">Dropping below this number causes the timer to be canceled.</span></span>

</dd> <dt>

<span data-ttu-id="c24a9-110">**Inactividad**</span><span class="sxs-lookup"><span data-stu-id="c24a9-110">**Idleness**</span></span>
</dt> <dd>

<span data-ttu-id="c24a9-111">Nivel de inactividad actual, expresado como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="c24a9-111">The current idle level, expressed as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="c24a9-112">**TimeRemaining**</span><span class="sxs-lookup"><span data-stu-id="c24a9-112">**TimeRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="c24a9-113">Tiempo restante en el temporizador de inactividad, en segundos.</span><span class="sxs-lookup"><span data-stu-id="c24a9-113">The time remaining in the idle timer, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c24a9-114">**CoolingMode**</span><span class="sxs-lookup"><span data-stu-id="c24a9-114">**CoolingMode**</span></span>
</dt> <dd>

<span data-ttu-id="c24a9-115">El modo de refrigeración del sistema actual.</span><span class="sxs-lookup"><span data-stu-id="c24a9-115">The current system cooling mode.</span></span> <span data-ttu-id="c24a9-116">Este miembro debe tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c24a9-116">This member must one of the following values.</span></span>



| <span data-ttu-id="c24a9-117">Value</span><span class="sxs-lookup"><span data-stu-id="c24a9-117">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="c24a9-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c24a9-118">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <span data-ttu-id="c24a9-119"><dt>**Pedido de compra \_ TZ \_ activo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c24a9-119"><dt>**PO\_TZ\_ACTIVE**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="c24a9-120">El sistema está actualmente en modo de enfriamiento activo.</span><span class="sxs-lookup"><span data-stu-id="c24a9-120">The system is currently in Active cooling mode.</span></span><br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <span data-ttu-id="c24a9-121"><dt>**Pedido de compra \_ \_ \_ Modo no válido de TZ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c24a9-121"><dt>**PO\_TZ\_INVALID\_MODE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="c24a9-122">El sistema no admite la limitación de la CPU o no hay ninguna zona térmica definida en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c24a9-122">The system does not support CPU throttling, or there is no thermal zone defined in the system.</span></span><br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <span data-ttu-id="c24a9-123"><dt>**Pedido de compra \_ TZ \_ pasivo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c24a9-123"><dt>**PO\_TZ\_PASSIVE**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="c24a9-124">El sistema está actualmente en modo de enfriamiento pasivo.</span><span class="sxs-lookup"><span data-stu-id="c24a9-124">The system is currently in Passive cooling mode.</span></span><br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c24a9-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c24a9-125">Remarks</span></span>

<span data-ttu-id="c24a9-126">Tenga en cuenta que esta definición de estructura se omitió accidentalmente en Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="c24a9-126">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="c24a9-127">Este error se corregirá en el futuro.</span><span class="sxs-lookup"><span data-stu-id="c24a9-127">This error will be corrected in the future.</span></span> <span data-ttu-id="c24a9-128">Mientras tanto, para compilar la aplicación, incluya la definición de la estructura contenida en este tema en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="c24a9-128">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c24a9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c24a9-129">Requirements</span></span>



| <span data-ttu-id="c24a9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c24a9-130">Requirement</span></span> | <span data-ttu-id="c24a9-131">Value</span><span class="sxs-lookup"><span data-stu-id="c24a9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c24a9-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c24a9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c24a9-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c24a9-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c24a9-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c24a9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c24a9-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c24a9-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c24a9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c24a9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c24a9-137">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="c24a9-137">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




