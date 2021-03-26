---
description: Esta clase es la clase de tipo de evento para cargar la imagen en eventos de archivo de paginación. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: PageFault_ImageLoadBacked (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985703"
---
# <a name="pagefault_imageloadbacked-class"></a><span data-ttu-id="63641-104">Errores \_ ImageLoadBacked (clase)</span><span class="sxs-lookup"><span data-stu-id="63641-104">PageFault\_ImageLoadBacked class</span></span>

<span data-ttu-id="63641-105">Esta clase es la clase de tipo de evento para cargar la imagen en eventos de archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="63641-105">This class is the event type class for image load in page file events.</span></span>

<span data-ttu-id="63641-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="63641-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="63641-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63641-107">Syntax</span></span>

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a><span data-ttu-id="63641-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="63641-108">Members</span></span>

<span data-ttu-id="63641-109">La clase **errores \_ ImageLoadBacked** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="63641-109">The **PageFault\_ImageLoadBacked** class has these types of members:</span></span>

-   [<span data-ttu-id="63641-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63641-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63641-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63641-111">Properties</span></span>

<span data-ttu-id="63641-112">La clase **errores \_ ImageLoadBacked** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="63641-112">The **PageFault\_ImageLoadBacked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63641-113">**DeviceChar**</span><span class="sxs-lookup"><span data-stu-id="63641-113">**DeviceChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63641-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63641-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63641-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63641-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63641-116">Calificadores: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="63641-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="63641-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="63641-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="63641-118">**FileChar**</span><span class="sxs-lookup"><span data-stu-id="63641-118">**FileChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63641-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63641-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63641-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63641-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63641-121">Calificadores: WmiDataId (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="63641-121">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="63641-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="63641-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="63641-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="63641-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63641-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63641-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63641-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63641-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63641-126">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="63641-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="63641-127">Haga coincidir el valor de este puntero con el valor del puntero **FileObject** en un evento de [**\_ nombre FileIo**](fileio-name.md) para determinar el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="63641-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="63641-128">**LoadFlags**</span><span class="sxs-lookup"><span data-stu-id="63641-128">**LoadFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63641-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63641-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63641-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63641-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63641-131">Calificadores: WmiDataId (4), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="63641-131">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="63641-132">Reservado.</span><span class="sxs-lookup"><span data-stu-id="63641-132">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63641-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63641-133">Remarks</span></span>

<span data-ttu-id="63641-134">El evento se registra durante la creación de una sección de imagen (por ejemplo, una carga de DLL) cuando el administrador de memoria determina que la imagen debe copiarse y ejecutarse desde el archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="63641-134">The event is logged during an image section creation (for example, a DLL load) when the memory manager determines that the image needs to be copied into and run from the page file.</span></span> <span data-ttu-id="63641-135">Normalmente, las imágenes se ejecutan desde el archivo de código fuente, pero el respaldo del archivo de paginación se puede producir cuando el administrador de memoria determina que el archivo de origen puede ser modificado de forma asincrónica por los escritores existentes o cuando el archivo de origen se encuentra en un medio extraíble o en un dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="63641-135">Typically, images are run from the source file but pagefile-backing can occur when the memory manager determines that the source file may be modified asynchronously by existing writers or when the source file is on a removable media or a remote device.</span></span>

## <a name="requirements"></a><span data-ttu-id="63641-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63641-136">Requirements</span></span>



| <span data-ttu-id="63641-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="63641-137">Requirement</span></span> | <span data-ttu-id="63641-138">Value</span><span class="sxs-lookup"><span data-stu-id="63641-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63641-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63641-139">Minimum supported client</span></span><br/> | <span data-ttu-id="63641-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63641-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63641-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63641-141">Minimum supported server</span></span><br/> | <span data-ttu-id="63641-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="63641-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63641-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="63641-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63641-144">**Errores \_ V2**</span><span class="sxs-lookup"><span data-stu-id="63641-144">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




