---
description: Esta clase es la clase de tipo de evento para el evento de creación de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: FileIo_Create (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984491"
---
# <a name="fileio_create-class"></a><span data-ttu-id="07cc4-104">\_Clase de creación FileIo</span><span class="sxs-lookup"><span data-stu-id="07cc4-104">FileIo\_Create class</span></span>

<span data-ttu-id="07cc4-105">Esta clase es la clase de tipo de evento para el evento de creación de archivo.</span><span class="sxs-lookup"><span data-stu-id="07cc4-105">This class is the event type class for the file create event.</span></span>

<span data-ttu-id="07cc4-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="07cc4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="07cc4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07cc4-107">Syntax</span></span>

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a><span data-ttu-id="07cc4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="07cc4-108">Members</span></span>

<span data-ttu-id="07cc4-109">La clase **FileIo \_ Create** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="07cc4-109">The **FileIo\_Create** class has these types of members:</span></span>

-   [<span data-ttu-id="07cc4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="07cc4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07cc4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="07cc4-111">Properties</span></span>

<span data-ttu-id="07cc4-112">La clase **FileIo \_ Create** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="07cc4-112">The **FileIo\_Create** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07cc4-113">**CreateOptions**</span><span class="sxs-lookup"><span data-stu-id="07cc4-113">**CreateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07cc4-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07cc4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="07cc4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-116">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="07cc4-116">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="07cc4-117">Los valores que se pasan en los parámetros *CreateOptions* y *CreateDispositions* a la función [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="07cc4-117">Values passed in the *CreateOptions* and *CreateDispositions* parameters to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="07cc4-118">**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="07cc4-118">**FileAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07cc4-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07cc4-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="07cc4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-121">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="07cc4-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="07cc4-122">Valor pasado en el parámetro *FileAttributes* a la función [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="07cc4-122">Value passed in the *FileAttributes* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="07cc4-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="07cc4-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07cc4-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07cc4-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="07cc4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-126">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="07cc4-126">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="07cc4-127">Identificador que se puede utilizar para correlacionar las operaciones con la misma instancia de objeto de archivo abierta entre los eventos de creación y cierre de archivo.</span><span class="sxs-lookup"><span data-stu-id="07cc4-127">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="07cc4-128">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="07cc4-128">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07cc4-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07cc4-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="07cc4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-131">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="07cc4-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="07cc4-132">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="07cc4-132">IO request packet.</span></span> <span data-ttu-id="07cc4-133">Esta propiedad identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="07cc4-133">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="07cc4-134">**OpenPath**</span><span class="sxs-lookup"><span data-stu-id="07cc4-134">**OpenPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07cc4-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="07cc4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="07cc4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-137">Calificadores: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="07cc4-137">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="07cc4-138">Ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="07cc4-138">Path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="07cc4-139">**ShareAccess**</span><span class="sxs-lookup"><span data-stu-id="07cc4-139">**ShareAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07cc4-140">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07cc4-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="07cc4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-142">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="07cc4-142">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="07cc4-143">Valor pasado en el parámetro *ShareAccess* a la función [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="07cc4-143">Value passed in the *ShareAccess* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="07cc4-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="07cc4-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07cc4-145">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07cc4-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="07cc4-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07cc4-147">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="07cc4-147">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="07cc4-148">Identificador de subproceso del subproceso que está creando el archivo.</span><span class="sxs-lookup"><span data-stu-id="07cc4-148">Thread identifier of the thread that is creating the file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07cc4-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07cc4-149">Requirements</span></span>



| <span data-ttu-id="07cc4-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="07cc4-150">Requirement</span></span> | <span data-ttu-id="07cc4-151">Value</span><span class="sxs-lookup"><span data-stu-id="07cc4-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07cc4-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07cc4-152">Minimum supported client</span></span><br/> | <span data-ttu-id="07cc4-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="07cc4-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07cc4-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07cc4-154">Minimum supported server</span></span><br/> | <span data-ttu-id="07cc4-155">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="07cc4-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07cc4-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="07cc4-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07cc4-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="07cc4-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 
