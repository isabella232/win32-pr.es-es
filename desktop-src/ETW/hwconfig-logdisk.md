---
description: La \_ clase HWConfig LogDisk es la clase de tipo de evento para los eventos de configuración de disco lógico. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: HWConfig_LogDisk (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546539"
---
# <a name="hwconfig_logdisk-class"></a><span data-ttu-id="7164e-104">HWConfig \_ LogDisk (clase)</span><span class="sxs-lookup"><span data-stu-id="7164e-104">HWConfig\_LogDisk class</span></span>

<span data-ttu-id="7164e-105">La clase **HWConfig \_ LogDisk** es la clase de tipo de evento para los eventos de configuración de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="7164e-105">The **HWConfig\_LogDisk** class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="7164e-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="7164e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7164e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7164e-107">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a><span data-ttu-id="7164e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7164e-108">Members</span></span>

<span data-ttu-id="7164e-109">La clase **HWConfig \_ LogDisk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7164e-109">The **HWConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="7164e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7164e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7164e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7164e-111">Properties</span></span>

<span data-ttu-id="7164e-112">La clase **HWConfig \_ LogDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7164e-112">The **HWConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7164e-113">Númerodedisco corresponde</span><span class="sxs-lookup"><span data-stu-id="7164e-113">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7164e-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7164e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7164e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7164e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7164e-116">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="7164e-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="7164e-117">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="7164e-117">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="7164e-118">Pad</span><span class="sxs-lookup"><span data-stu-id="7164e-118">Pad</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7164e-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7164e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7164e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7164e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7164e-121">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="7164e-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="7164e-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7164e-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7164e-123">PartitionSize</span><span class="sxs-lookup"><span data-stu-id="7164e-123">PartitionSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7164e-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7164e-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7164e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7164e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7164e-126">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="7164e-126">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="7164e-127">Tamaño total de la partición, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7164e-127">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7164e-128">StartOffset</span><span class="sxs-lookup"><span data-stu-id="7164e-128">StartOffset</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7164e-129">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7164e-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7164e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7164e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7164e-131">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="7164e-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="7164e-132">Desplazamiento inicial (en bytes) de la partición desde el principio del disco.</span><span class="sxs-lookup"><span data-stu-id="7164e-132">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7164e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7164e-133">Requirements</span></span>



| <span data-ttu-id="7164e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7164e-134">Requirement</span></span> | <span data-ttu-id="7164e-135">Value</span><span class="sxs-lookup"><span data-stu-id="7164e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="7164e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7164e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7164e-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7164e-137">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7164e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7164e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7164e-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7164e-139">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="7164e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7164e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7164e-141">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="7164e-141">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




