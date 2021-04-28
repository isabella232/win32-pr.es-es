---
description: 'Image_V0_Load clase : esta clase es la clase de tipo de evento para los eventos de carga de imágenes. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Image_V0_Load clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106523"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="2d340-104">Image \_ V0 \_ Load (clase)</span><span class="sxs-lookup"><span data-stu-id="2d340-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="2d340-105">Esta clase es la clase de tipo de evento para los eventos de carga de imágenes.</span><span class="sxs-lookup"><span data-stu-id="2d340-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="2d340-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="2d340-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d340-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d340-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="2d340-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d340-108">Members</span></span>

<span data-ttu-id="2d340-109">La **clase Load de Image \_ V0 \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d340-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="2d340-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d340-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d340-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d340-111">Properties</span></span>

<span data-ttu-id="2d340-112">La **clase Load de Image \_ V0 \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2d340-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d340-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="2d340-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d340-114">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="2d340-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d340-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d340-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d340-116">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="2d340-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2d340-117">Dirección base de la aplicación en la que se carga la imagen.</span><span class="sxs-lookup"><span data-stu-id="2d340-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="2d340-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="2d340-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d340-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2d340-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d340-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d340-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d340-121">Calificadores: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="2d340-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="2d340-122">Nombre de archivo y extensión del archivo DLL o la imagen ejecutable que se cargará.</span><span class="sxs-lookup"><span data-stu-id="2d340-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="2d340-123">ModuleSize</span><span class="sxs-lookup"><span data-stu-id="2d340-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d340-124">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="2d340-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d340-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d340-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d340-126">Calificadores: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="2d340-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2d340-127">Tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2d340-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d340-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d340-128">Requirements</span></span>



| <span data-ttu-id="2d340-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d340-129">Requirement</span></span> | <span data-ttu-id="2d340-130">Valor</span><span class="sxs-lookup"><span data-stu-id="2d340-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2d340-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d340-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2d340-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2d340-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2d340-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d340-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2d340-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2d340-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2d340-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2d340-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d340-136">**Imagen \_ V0**</span><span class="sxs-lookup"><span data-stu-id="2d340-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




