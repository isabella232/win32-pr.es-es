---
description: Esta clase es la clase de tipo de evento que marca el principio de los eventos de lectura, escritura y vaciado de e/s de disco. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: DiskIo_TypeGroup2 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540374"
---
# <a name="diskio_typegroup2-class"></a><span data-ttu-id="b6b00-104">Desmontaje \_ TypeGroup2 (clase)</span><span class="sxs-lookup"><span data-stu-id="b6b00-104">DiskIo\_TypeGroup2 class</span></span>

<span data-ttu-id="b6b00-105">Esta clase es la clase de tipo de evento que marca el principio de los eventos de lectura, escritura y vaciado de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="b6b00-105">This class is the event type class that marks the beginning of the disk I/O read, write, and flush events.</span></span>

<span data-ttu-id="b6b00-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="b6b00-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b00-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6b00-107">Syntax</span></span>

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="b6b00-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6b00-108">Members</span></span>

<span data-ttu-id="b6b00-109">La clase **desmontaje \_ TypeGroup2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b6b00-109">The **DiskIo\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="b6b00-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6b00-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6b00-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6b00-111">Properties</span></span>

<span data-ttu-id="b6b00-112">La clase **desmontaje \_ TypeGroup2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6b00-112">The **DiskIo\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6b00-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="b6b00-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b00-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6b00-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6b00-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6b00-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b00-116">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**puntero**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b6b00-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b6b00-117">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="b6b00-117">I/O request packet.</span></span> <span data-ttu-id="b6b00-118">Esta propiedad identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="b6b00-118">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="b6b00-119">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="b6b00-119">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b00-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6b00-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6b00-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6b00-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b00-122">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="b6b00-122">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="b6b00-123">Identificador del subproceso que se emite.</span><span class="sxs-lookup"><span data-stu-id="b6b00-123">The identifier of the issuing thread.</span></span>

<span data-ttu-id="b6b00-124">**Windows server 2008 R2, Windows server 2008, Windows 7 y Windows Vista:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="b6b00-124">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6b00-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6b00-125">Requirements</span></span>



| <span data-ttu-id="b6b00-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6b00-126">Requirement</span></span> | <span data-ttu-id="b6b00-127">Value</span><span class="sxs-lookup"><span data-stu-id="b6b00-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6b00-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6b00-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b00-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b6b00-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6b00-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6b00-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b00-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6b00-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6b00-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6b00-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b00-133">**Desmontaje**</span><span class="sxs-lookup"><span data-stu-id="b6b00-133">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




