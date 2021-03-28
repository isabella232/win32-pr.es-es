---
description: Esta clase es la clase de tipo de evento para el evento de información de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: FileIo_Info (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985846"
---
# <a name="fileio_info-class"></a><span data-ttu-id="81821-104">\_Clase de información FileIo</span><span class="sxs-lookup"><span data-stu-id="81821-104">FileIo\_Info class</span></span>

<span data-ttu-id="81821-105">Esta clase es la clase de tipo de evento para el evento de información de archivo.</span><span class="sxs-lookup"><span data-stu-id="81821-105">This class is the event type class for file information event.</span></span>

<span data-ttu-id="81821-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="81821-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="81821-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81821-107">Syntax</span></span>

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a><span data-ttu-id="81821-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="81821-108">Members</span></span>

<span data-ttu-id="81821-109">La clase de **\_ información FileIo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="81821-109">The **FileIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="81821-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81821-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81821-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81821-111">Properties</span></span>

<span data-ttu-id="81821-112">La clase de **\_ información FileIo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="81821-112">The **FileIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81821-113">**ExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="81821-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81821-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81821-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81821-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81821-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81821-116">Calificadores: WmiDataId (5), puntero</span><span class="sxs-lookup"><span data-stu-id="81821-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="81821-117">En el caso de las solicitudes FileDispositionInformation, este campo contiene la disposición solicitada.</span><span class="sxs-lookup"><span data-stu-id="81821-117">For FileDispositionInformation requests, this field contains the requested disposition.</span></span> <span data-ttu-id="81821-118">En el caso de las solicitudes FileEndOfFileInformation y FileAllocationInformation, este campo contiene el tamaño de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="81821-118">For FileEndOfFileInformation and FileAllocationInformation requests, this field contains the specified file size.</span></span>

</dd> <dt>

<span data-ttu-id="81821-119">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="81821-119">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81821-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81821-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81821-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81821-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81821-122">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="81821-122">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="81821-123">Para determinar el nombre de archivo, haga coincidir el valor de esta propiedad con la propiedad **FileObject** de un evento de [**\_ nombre FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="81821-123">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="81821-124">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="81821-124">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81821-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81821-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81821-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81821-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81821-127">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="81821-127">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="81821-128">Identificador que se puede utilizar para correlacionar las operaciones con la misma instancia de objeto de archivo abierta entre los eventos de creación y cierre de archivo.</span><span class="sxs-lookup"><span data-stu-id="81821-128">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="81821-129">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="81821-129">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81821-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81821-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81821-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81821-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81821-132">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="81821-132">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="81821-133">Clase de información de archivo solicitada.</span><span class="sxs-lookup"><span data-stu-id="81821-133">Requested file information class.</span></span>

</dd> <dt>

<span data-ttu-id="81821-134">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="81821-134">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81821-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81821-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81821-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81821-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81821-137">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="81821-137">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="81821-138">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="81821-138">IO request packet.</span></span> <span data-ttu-id="81821-139">Esta propiedad identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="81821-139">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="81821-140">**TTID**</span><span class="sxs-lookup"><span data-stu-id="81821-140">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81821-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81821-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81821-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81821-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81821-143">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="81821-143">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="81821-144">Identificador de subproceso del subproceso que está realizando la operación.</span><span class="sxs-lookup"><span data-stu-id="81821-144">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81821-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81821-145">Remarks</span></span>

<span data-ttu-id="81821-146">Establecer información y eventos de información de consulta indica que los atributos de archivo se han establecido o consultado.</span><span class="sxs-lookup"><span data-stu-id="81821-146">Set information and query information events indicate that the file attributes were set or queried.</span></span> <span data-ttu-id="81821-147">Cuando se emite un comando FSCTL, se registra un evento de control del sistema de archivos (FSControl).</span><span class="sxs-lookup"><span data-stu-id="81821-147">A file system control (FSControl) event is recorded when a FSCTL command is issued.</span></span>

## <a name="requirements"></a><span data-ttu-id="81821-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81821-148">Requirements</span></span>



| <span data-ttu-id="81821-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="81821-149">Requirement</span></span> | <span data-ttu-id="81821-150">Value</span><span class="sxs-lookup"><span data-stu-id="81821-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="81821-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81821-151">Minimum supported client</span></span><br/> | <span data-ttu-id="81821-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="81821-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="81821-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81821-153">Minimum supported server</span></span><br/> | <span data-ttu-id="81821-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="81821-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81821-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="81821-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81821-156">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="81821-156">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




