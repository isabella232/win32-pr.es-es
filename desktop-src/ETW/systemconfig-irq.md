---
description: Esta clase es la clase de tipo de evento para eventos de solicitud de interrupción (IRQ). La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: SystemConfig_IRQ (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984455"
---
# <a name="systemconfig_irq-class"></a><span data-ttu-id="b2b30-104">SystemConfig ( \_ clase de IRQ)</span><span class="sxs-lookup"><span data-stu-id="b2b30-104">SystemConfig\_IRQ class</span></span>

<span data-ttu-id="b2b30-105">Esta clase es la clase de tipo de evento para eventos de solicitud de interrupción (IRQ).</span><span class="sxs-lookup"><span data-stu-id="b2b30-105">This class is the event type class for interrupt request (IRQ) events.</span></span>

<span data-ttu-id="b2b30-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="b2b30-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b30-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2b30-107">Syntax</span></span>

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a><span data-ttu-id="b2b30-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2b30-108">Members</span></span>

<span data-ttu-id="b2b30-109">La **clase \_ IRQ SystemConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b2b30-109">The **SystemConfig\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="b2b30-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2b30-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2b30-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2b30-111">Properties</span></span>

<span data-ttu-id="b2b30-112">La **clase \_ IRQ SystemConfig** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2b30-112">The **SystemConfig\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2b30-113">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="b2b30-113">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b30-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b2b30-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b30-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2b30-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b30-116">Calificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="b2b30-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="b2b30-117">Descripción del dispositivo o software que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2b30-117">Description of the device or software making the request.</span></span>

</dd> <dt>

<span data-ttu-id="b2b30-118">**DeviceDescriptionLen**</span><span class="sxs-lookup"><span data-stu-id="b2b30-118">**DeviceDescriptionLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b30-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b30-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b30-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2b30-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b30-121">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="b2b30-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="b2b30-122">Longitud, en caracteres, de la cadena en **DeviceDescription**.</span><span class="sxs-lookup"><span data-stu-id="b2b30-122">Length, in characters, of the string in **DeviceDescription**.</span></span>

</dd> <dt>

<span data-ttu-id="b2b30-123">**IRQAffinity**</span><span class="sxs-lookup"><span data-stu-id="b2b30-123">**IRQAffinity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b30-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2b30-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2b30-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2b30-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b30-126">Calificadores: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="b2b30-126">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b2b30-127">Máscara de afinidad de IRQ.</span><span class="sxs-lookup"><span data-stu-id="b2b30-127">IRQ affinity mask.</span></span> <span data-ttu-id="b2b30-128">La máscara de afinidad identifica los procesadores (o grupos de procesadores) específicos que pueden recibir la IRQ.</span><span class="sxs-lookup"><span data-stu-id="b2b30-128">The affinity mask identifies the specific processors (or groups of processors) that can receive the IRQ.</span></span>

</dd> <dt>

<span data-ttu-id="b2b30-129">**IRQNum**</span><span class="sxs-lookup"><span data-stu-id="b2b30-129">**IRQNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b30-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b30-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b30-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2b30-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b30-132">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="b2b30-132">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="b2b30-133">Número de línea de solicitud de interrupción.</span><span class="sxs-lookup"><span data-stu-id="b2b30-133">Interrupt request line number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2b30-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b30-134">Requirements</span></span>



| <span data-ttu-id="b2b30-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b30-135">Requirement</span></span> | <span data-ttu-id="b2b30-136">Value</span><span class="sxs-lookup"><span data-stu-id="b2b30-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2b30-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2b30-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b30-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b2b30-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2b30-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2b30-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b30-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2b30-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2b30-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2b30-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b30-142">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="b2b30-142">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




