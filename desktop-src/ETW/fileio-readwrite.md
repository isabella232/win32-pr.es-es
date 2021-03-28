---
description: Esta clase es la clase de tipo de evento para los eventos de lectura y escritura de archivos. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: FileIo_ReadWrite (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985843"
---
# <a name="fileio_readwrite-class"></a><span data-ttu-id="29946-104">FileIo \_ ReadWrite (clase)</span><span class="sxs-lookup"><span data-stu-id="29946-104">FileIo\_ReadWrite class</span></span>

<span data-ttu-id="29946-105">Esta clase es la clase de tipo de evento para los eventos de lectura y escritura de archivos.</span><span class="sxs-lookup"><span data-stu-id="29946-105">This class is the event type class for file read and write events.</span></span>

<span data-ttu-id="29946-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="29946-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="29946-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29946-107">Syntax</span></span>

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a><span data-ttu-id="29946-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="29946-108">Members</span></span>

<span data-ttu-id="29946-109">La clase **FileIo \_ ReadWrite** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="29946-109">The **FileIo\_ReadWrite** class has these types of members:</span></span>

-   [<span data-ttu-id="29946-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29946-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29946-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29946-111">Properties</span></span>

<span data-ttu-id="29946-112">La clase **FileIo \_ ReadWrite** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="29946-112">The **FileIo\_ReadWrite** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29946-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="29946-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29946-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29946-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29946-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29946-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29946-116">Calificadores: WmiDataId (5), puntero</span><span class="sxs-lookup"><span data-stu-id="29946-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="29946-117">Para determinar el nombre de archivo, haga coincidir el valor de esta propiedad con la propiedad **FileObject** de un evento de [**\_ nombre FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="29946-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="29946-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="29946-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29946-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29946-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29946-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29946-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29946-121">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="29946-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="29946-122">Identificador que se puede utilizar para correlacionar las operaciones con la misma instancia de objeto de archivo abierta entre los eventos de creación y cierre de archivo.</span><span class="sxs-lookup"><span data-stu-id="29946-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="29946-123">**IoFlags**</span><span class="sxs-lookup"><span data-stu-id="29946-123">**IoFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29946-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29946-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29946-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29946-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29946-126">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="29946-126">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="29946-127">Marcas de paquete de solicitud de e/s especificadas para esta operación.</span><span class="sxs-lookup"><span data-stu-id="29946-127">IO request packet flags specified for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="29946-128">**IoSize**</span><span class="sxs-lookup"><span data-stu-id="29946-128">**IoSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29946-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29946-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29946-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29946-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29946-131">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="29946-131">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="29946-132">Número de bytes solicitados.</span><span class="sxs-lookup"><span data-stu-id="29946-132">Number of bytes requested.</span></span>

</dd> <dt>

<span data-ttu-id="29946-133">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="29946-133">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29946-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29946-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29946-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29946-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29946-136">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="29946-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="29946-137">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="29946-137">IO request packet.</span></span> <span data-ttu-id="29946-138">Esta propiedad identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="29946-138">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="29946-139">**Offset**</span><span class="sxs-lookup"><span data-stu-id="29946-139">**Offset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29946-140">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="29946-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="29946-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29946-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29946-142">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="29946-142">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="29946-143">Desplazamiento del archivo de inicio para la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="29946-143">Starting file offset for the requested operation.</span></span>

</dd> <dt>

<span data-ttu-id="29946-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="29946-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29946-145">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29946-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29946-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29946-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29946-147">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="29946-147">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="29946-148">Identificador de subproceso del subproceso que está realizando la operación.</span><span class="sxs-lookup"><span data-stu-id="29946-148">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29946-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29946-149">Requirements</span></span>



| <span data-ttu-id="29946-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="29946-150">Requirement</span></span> | <span data-ttu-id="29946-151">Value</span><span class="sxs-lookup"><span data-stu-id="29946-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="29946-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29946-152">Minimum supported client</span></span><br/> | <span data-ttu-id="29946-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="29946-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="29946-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29946-154">Minimum supported server</span></span><br/> | <span data-ttu-id="29946-155">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="29946-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29946-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="29946-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29946-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="29946-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




