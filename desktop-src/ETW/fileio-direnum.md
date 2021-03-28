---
description: Esta clase es la clase de tipo de evento para los eventos de notificación de directorio de enumeración. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: FileIo_DirEnum (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984490"
---
# <a name="fileio_direnum-class"></a><span data-ttu-id="7ab20-104">\_Clase FileIo DirEnum</span><span class="sxs-lookup"><span data-stu-id="7ab20-104">FileIo\_DirEnum class</span></span>

<span data-ttu-id="7ab20-105">Esta clase es la clase de tipo de evento para los eventos de notificación de directorio de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7ab20-105">This class is the event type class for the enumerate directory and directory notification events.</span></span>

<span data-ttu-id="7ab20-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="7ab20-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab20-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ab20-107">Syntax</span></span>

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="7ab20-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ab20-108">Members</span></span>

<span data-ttu-id="7ab20-109">La clase **FileIo \_ DirEnum** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7ab20-109">The **FileIo\_DirEnum** class has these types of members:</span></span>

-   [<span data-ttu-id="7ab20-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ab20-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ab20-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ab20-111">Properties</span></span>

<span data-ttu-id="7ab20-112">La clase **FileIo \_ DirEnum** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ab20-112">The **FileIo\_DirEnum** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ab20-113">**FileIndex**</span><span class="sxs-lookup"><span data-stu-id="7ab20-113">**FileIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ab20-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ab20-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab20-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-116">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="7ab20-116">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="7ab20-117">Índice de archivo del que se va a continuar la enumeración de directorios.</span><span class="sxs-lookup"><span data-stu-id="7ab20-117">File index from which to continue directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="7ab20-118">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="7ab20-118">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ab20-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ab20-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab20-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-121">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="7ab20-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7ab20-122">Para determinar el nombre del directorio, haga coincidir el valor de esta propiedad con la propiedad **FileObject** de un evento de [**\_ nombre FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="7ab20-122">To determine the directory name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="7ab20-123">**FileName**</span><span class="sxs-lookup"><span data-stu-id="7ab20-123">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ab20-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ab20-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab20-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-126">Calificadores: WmiDataId (8), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="7ab20-126">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="7ab20-127">Patrón especificado para la enumeración de directorios.</span><span class="sxs-lookup"><span data-stu-id="7ab20-127">Pattern specified for directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="7ab20-128">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="7ab20-128">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ab20-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ab20-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab20-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-131">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="7ab20-131">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7ab20-132">Identificador que se puede utilizar para correlacionar las operaciones con la misma instancia de objeto de archivo abierta entre los eventos de creación y cierre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7ab20-132">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="7ab20-133">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="7ab20-133">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ab20-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ab20-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab20-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-136">Calificadores: WmiDataId (6), puntero</span><span class="sxs-lookup"><span data-stu-id="7ab20-136">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7ab20-137">Clase de información de enumeración de directorio solicitada.</span><span class="sxs-lookup"><span data-stu-id="7ab20-137">Requested directory enumeration information class.</span></span>

</dd> <dt>

<span data-ttu-id="7ab20-138">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="7ab20-138">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ab20-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ab20-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab20-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-141">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="7ab20-141">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7ab20-142">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="7ab20-142">IO request packet.</span></span> <span data-ttu-id="7ab20-143">Esta propiedad identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="7ab20-143">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="7ab20-144">**Duración**</span><span class="sxs-lookup"><span data-stu-id="7ab20-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ab20-145">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ab20-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab20-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-147">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="7ab20-147">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="7ab20-148">Tamaño del búfer de consulta, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7ab20-148">Size of the query buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7ab20-149">**TTID**</span><span class="sxs-lookup"><span data-stu-id="7ab20-149">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ab20-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ab20-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab20-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ab20-152">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="7ab20-152">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7ab20-153">Identificador de subproceso del subproceso que está realizando la operación.</span><span class="sxs-lookup"><span data-stu-id="7ab20-153">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ab20-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ab20-154">Remarks</span></span>

<span data-ttu-id="7ab20-155">La enumeración de directorios y los eventos de notificación de directorio se registran cuando se enumera un directorio o se envía una notificación de cambio de directorio a los agentes de escucha registrados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7ab20-155">Directory enumeration and directory notification events are recorded when a directory is enumerated or a directory change notification is sent to registered listeners, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab20-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ab20-156">Requirements</span></span>



| <span data-ttu-id="7ab20-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab20-157">Requirement</span></span> | <span data-ttu-id="7ab20-158">Value</span><span class="sxs-lookup"><span data-stu-id="7ab20-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ab20-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ab20-159">Minimum supported client</span></span><br/> | <span data-ttu-id="7ab20-160">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7ab20-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ab20-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ab20-161">Minimum supported server</span></span><br/> | <span data-ttu-id="7ab20-162">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ab20-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ab20-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ab20-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab20-164">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="7ab20-164">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




