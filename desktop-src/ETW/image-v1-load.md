---
description: 'Image_V1_Load clase : esta clase es la clase de tipo de evento para los eventos de carga de imágenes. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e8a8c31cee7e45311887c16a1d10545e6a38e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106503"
---
# <a name="image_v1_load-class"></a><span data-ttu-id="20e6e-104">Image \_ V1 \_ Load (clase)</span><span class="sxs-lookup"><span data-stu-id="20e6e-104">Image\_V1\_Load class</span></span>

<span data-ttu-id="20e6e-105">Esta clase es la clase de tipo de evento para los eventos de carga de imágenes.</span><span class="sxs-lookup"><span data-stu-id="20e6e-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="20e6e-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="20e6e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="20e6e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20e6e-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="20e6e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="20e6e-108">Members</span></span>

<span data-ttu-id="20e6e-109">La **clase Load de Image \_ V1 \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="20e6e-109">The **Image\_V1\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="20e6e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20e6e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20e6e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20e6e-111">Properties</span></span>

<span data-ttu-id="20e6e-112">La **clase Load de Image \_ V1 \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="20e6e-112">The **Image\_V1\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20e6e-113">FileName</span><span class="sxs-lookup"><span data-stu-id="20e6e-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e6e-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20e6e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e6e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20e6e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e6e-116">Calificadores: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="20e6e-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="20e6e-117">Nombre de archivo y extensión del archivo DLL o la imagen ejecutable que se cargará.</span><span class="sxs-lookup"><span data-stu-id="20e6e-117">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="20e6e-118">ImageBase</span><span class="sxs-lookup"><span data-stu-id="20e6e-118">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e6e-119">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="20e6e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20e6e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20e6e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e6e-121">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="20e6e-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="20e6e-122">Dirección base de la aplicación en la que se carga la imagen.</span><span class="sxs-lookup"><span data-stu-id="20e6e-122">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="20e6e-123">ImageSize</span><span class="sxs-lookup"><span data-stu-id="20e6e-123">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e6e-124">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="20e6e-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20e6e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20e6e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e6e-126">Calificadores: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="20e6e-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="20e6e-127">Tamaño de la imagen que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="20e6e-127">Size of the image being loaded.</span></span>

<span data-ttu-id="20e6e-128">Al consumir esta propiedad, el tipo de datos de esta propiedad es realmente de tamaño \_ t.</span><span class="sxs-lookup"><span data-stu-id="20e6e-128">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="20e6e-129">El calificador Pointer se usa para determinar si el tamaño \_ t es de 4 bytes o 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="20e6e-129">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="20e6e-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="20e6e-130">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e6e-131">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="20e6e-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20e6e-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20e6e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e6e-133">Calificadores: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="20e6e-133">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="20e6e-134">Identifica el proceso en el que se carga la imagen.</span><span class="sxs-lookup"><span data-stu-id="20e6e-134">Identifies the process into which the image is loaded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20e6e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20e6e-135">Requirements</span></span>



| <span data-ttu-id="20e6e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="20e6e-136">Requirement</span></span> | <span data-ttu-id="20e6e-137">Valor</span><span class="sxs-lookup"><span data-stu-id="20e6e-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20e6e-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20e6e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="20e6e-139">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="20e6e-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="20e6e-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20e6e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="20e6e-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="20e6e-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20e6e-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="20e6e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e6e-143">**Imagen \_ V1**</span><span class="sxs-lookup"><span data-stu-id="20e6e-143">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




