---
description: Esta clase es la clase de tipo de evento para los eventos de imagen. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Image_Load (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544894"
---
# <a name="image_load-class"></a><span data-ttu-id="af9da-104">Clase de carga de imagen \_</span><span class="sxs-lookup"><span data-stu-id="af9da-104">Image\_Load class</span></span>

<span data-ttu-id="af9da-105">Esta clase es la clase de tipo de evento para los eventos de imagen.</span><span class="sxs-lookup"><span data-stu-id="af9da-105">This class is the event type class for image events.</span></span>

<span data-ttu-id="af9da-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="af9da-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af9da-107">Syntax</span></span>

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="af9da-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="af9da-108">Members</span></span>

<span data-ttu-id="af9da-109">La clase de **\_ carga** de la imagen tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="af9da-109">The **Image\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="af9da-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af9da-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af9da-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af9da-111">Properties</span></span>

<span data-ttu-id="af9da-112">La clase de **\_ carga** de la imagen tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="af9da-112">The **Image\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af9da-113">DefaultBase</span><span class="sxs-lookup"><span data-stu-id="af9da-113">DefaultBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-116">Calificadores: WmiDataId (7), puntero</span><span class="sxs-lookup"><span data-stu-id="af9da-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="af9da-117">Dirección base predeterminada.</span><span class="sxs-lookup"><span data-stu-id="af9da-117">Default base address.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-118">FileName</span><span class="sxs-lookup"><span data-stu-id="af9da-118">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="af9da-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-121">Calificadores: WmiDataId (12), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="af9da-121">Qualifiers: WmiDataId(12), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="af9da-122">Nombre de archivo y extensión del archivo DLL o la imagen ejecutable.</span><span class="sxs-lookup"><span data-stu-id="af9da-122">File name and extension of the DLL or executable image.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-123">ImageBase</span><span class="sxs-lookup"><span data-stu-id="af9da-123">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-126">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="af9da-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="af9da-127">Dirección base de la aplicación en la que se carga la imagen.</span><span class="sxs-lookup"><span data-stu-id="af9da-127">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-128">ImageCheckSum</span><span class="sxs-lookup"><span data-stu-id="af9da-128">ImageCheckSum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-131">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="af9da-131">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="af9da-132">Suma de comprobación de imagen.</span><span class="sxs-lookup"><span data-stu-id="af9da-132">Image check sum.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-133">ImageSize</span><span class="sxs-lookup"><span data-stu-id="af9da-133">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-136">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="af9da-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="af9da-137">Tamaño de la imagen que se está cargando.</span><span class="sxs-lookup"><span data-stu-id="af9da-137">Size of the image being loaded.</span></span>

<span data-ttu-id="af9da-138">Al utilizar esta propiedad, el tamaño del tipo de datos de esta propiedad es realmente \_ t.</span><span class="sxs-lookup"><span data-stu-id="af9da-138">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="af9da-139">El calificador de puntero se usa para determinar si el tamaño \_ t es de 4 bytes o de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="af9da-139">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-140">ProcessId</span><span class="sxs-lookup"><span data-stu-id="af9da-140">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-143">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="af9da-143">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="af9da-144">Identifica el proceso en el que se carga la imagen.</span><span class="sxs-lookup"><span data-stu-id="af9da-144">Identifies the process into which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-145">Reserved0</span><span class="sxs-lookup"><span data-stu-id="af9da-145">Reserved0</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-148">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="af9da-148">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="af9da-149">Reservado.</span><span class="sxs-lookup"><span data-stu-id="af9da-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-150">Reserved1</span><span class="sxs-lookup"><span data-stu-id="af9da-150">Reserved1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-153">Calificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="af9da-153">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="af9da-154">Reservado.</span><span class="sxs-lookup"><span data-stu-id="af9da-154">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-155">Reserved2</span><span class="sxs-lookup"><span data-stu-id="af9da-155">Reserved2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-156">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-158">Calificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="af9da-158">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="af9da-159">Reservado.</span><span class="sxs-lookup"><span data-stu-id="af9da-159">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-160">Reserved3</span><span class="sxs-lookup"><span data-stu-id="af9da-160">Reserved3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-161">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-163">Calificadores: WmiDataId (10)</span><span class="sxs-lookup"><span data-stu-id="af9da-163">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="af9da-164">Reservado.</span><span class="sxs-lookup"><span data-stu-id="af9da-164">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-165">Reserved4</span><span class="sxs-lookup"><span data-stu-id="af9da-165">Reserved4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-166">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-168">Calificadores: WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="af9da-168">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="af9da-169">Reservado.</span><span class="sxs-lookup"><span data-stu-id="af9da-169">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="af9da-170">TimeDateStamp</span><span class="sxs-lookup"><span data-stu-id="af9da-170">TimeDateStamp</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af9da-171">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af9da-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af9da-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af9da-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af9da-173">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="af9da-173">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="af9da-174">Fecha y hora en que se cargó o descargó la imagen.</span><span class="sxs-lookup"><span data-stu-id="af9da-174">Time and date that the image was loaded or unloaded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af9da-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af9da-175">Remarks</span></span>

<span data-ttu-id="af9da-176">Los eventos DCStart y DCEnd enumeran todas las imágenes cargadas al principio y al final del seguimiento, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="af9da-176">The DCStart and DCEnd events enumerate all loaded images at the beginning and end of the trace, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9da-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af9da-177">Requirements</span></span>



| <span data-ttu-id="af9da-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="af9da-178">Requirement</span></span> | <span data-ttu-id="af9da-179">Value</span><span class="sxs-lookup"><span data-stu-id="af9da-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af9da-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af9da-180">Minimum supported client</span></span><br/> | <span data-ttu-id="af9da-181">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af9da-181">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af9da-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af9da-182">Minimum supported server</span></span><br/> | <span data-ttu-id="af9da-183">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="af9da-183">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af9da-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="af9da-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9da-185">**Imagen**</span><span class="sxs-lookup"><span data-stu-id="af9da-185">**Image**</span></span>](image.md)
</dt> <dt>

[<span data-ttu-id="af9da-186">**Imagen \_ v0**</span><span class="sxs-lookup"><span data-stu-id="af9da-186">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="af9da-187">**Imagen \_ v1**</span><span class="sxs-lookup"><span data-stu-id="af9da-187">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




