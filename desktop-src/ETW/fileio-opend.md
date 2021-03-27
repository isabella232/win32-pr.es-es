---
description: Esta clase es la clase de tipo de evento para los eventos de finalización de operación de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816262"
---
# <a name="fileio_opend-class"></a><span data-ttu-id="28d2d-104">FileIo ( \_ clase abierta)</span><span class="sxs-lookup"><span data-stu-id="28d2d-104">FileIo\_OpEnd class</span></span>

<span data-ttu-id="28d2d-105">Esta clase es la clase de tipo de evento para los eventos de finalización de operación de archivo.</span><span class="sxs-lookup"><span data-stu-id="28d2d-105">This class is the event type class for file operation end events.</span></span>

<span data-ttu-id="28d2d-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="28d2d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d2d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28d2d-107">Syntax</span></span>

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a><span data-ttu-id="28d2d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="28d2d-108">Members</span></span>

<span data-ttu-id="28d2d-109">La **clase \_ abierta FileIo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="28d2d-109">The **FileIo\_OpEnd** class has these types of members:</span></span>

-   [<span data-ttu-id="28d2d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28d2d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28d2d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28d2d-111">Properties</span></span>

<span data-ttu-id="28d2d-112">La **clase \_ abierta FileIo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="28d2d-112">The **FileIo\_OpEnd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28d2d-113">**ExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="28d2d-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28d2d-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28d2d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28d2d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="28d2d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28d2d-116">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="28d2d-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="28d2d-117">Información adicional devuelta por el sistema de archivos para la operación.</span><span class="sxs-lookup"><span data-stu-id="28d2d-117">Extra information returned by the file system for the operation.</span></span> <span data-ttu-id="28d2d-118">Por ejemplo, para una solicitud de lectura, el número real de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="28d2d-118">For example for a read request, the actual number of bytes that were read.</span></span>

</dd> <dt>

<span data-ttu-id="28d2d-119">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="28d2d-119">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28d2d-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28d2d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28d2d-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="28d2d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28d2d-122">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="28d2d-122">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="28d2d-123">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="28d2d-123">IO request packet.</span></span> <span data-ttu-id="28d2d-124">Esta propiedad identifica la actividad de e/s que está finalizando.</span><span class="sxs-lookup"><span data-stu-id="28d2d-124">This property identifies the IO activity that is ending.</span></span>

</dd> <dt>

<span data-ttu-id="28d2d-125">**NtStatus**</span><span class="sxs-lookup"><span data-stu-id="28d2d-125">**NtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28d2d-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28d2d-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28d2d-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="28d2d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28d2d-128">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="28d2d-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="28d2d-129">Valor devuelto de la operación.</span><span class="sxs-lookup"><span data-stu-id="28d2d-129">Return value from the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28d2d-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28d2d-130">Remarks</span></span>

<span data-ttu-id="28d2d-131">Los eventos [**FileIo**](fileio.md) se registran al principio de la operación.</span><span class="sxs-lookup"><span data-stu-id="28d2d-131">[**FileIo**](fileio.md) events are logged at the beginning of the operation.</span></span> <span data-ttu-id="28d2d-132">Los eventos abiertos se pueden habilitar por separado para indicar el final de esas operaciones.</span><span class="sxs-lookup"><span data-stu-id="28d2d-132">OpEnd events can be enabled separately to indicate the end of those operations.</span></span> <span data-ttu-id="28d2d-133">IRP se puede usar para poner en correlación los eventos de inicio y fin.</span><span class="sxs-lookup"><span data-stu-id="28d2d-133">Irp can be used to correlate the begin and end events.</span></span>

## <a name="requirements"></a><span data-ttu-id="28d2d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28d2d-134">Requirements</span></span>



| <span data-ttu-id="28d2d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d2d-135">Requirement</span></span> | <span data-ttu-id="28d2d-136">Value</span><span class="sxs-lookup"><span data-stu-id="28d2d-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="28d2d-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28d2d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="28d2d-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="28d2d-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="28d2d-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28d2d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="28d2d-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="28d2d-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28d2d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="28d2d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d2d-142">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="28d2d-142">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




