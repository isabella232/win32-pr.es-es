---
description: Esta clase es la clase de tipo de evento para los eventos de carga de la imagen. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Image_V0_Load (clase)
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
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984222"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="498da-104">Image \_ V0 \_ Load (clase)</span><span class="sxs-lookup"><span data-stu-id="498da-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="498da-105">Esta clase es la clase de tipo de evento para los eventos de carga de la imagen.</span><span class="sxs-lookup"><span data-stu-id="498da-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="498da-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="498da-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="498da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="498da-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="498da-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="498da-108">Members</span></span>

<span data-ttu-id="498da-109">La clase **Image \_ V0 \_ Load** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="498da-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="498da-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="498da-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="498da-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="498da-111">Properties</span></span>

<span data-ttu-id="498da-112">La clase **Image \_ V0 \_ Load** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="498da-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="498da-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="498da-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="498da-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="498da-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="498da-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="498da-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="498da-116">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="498da-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="498da-117">Dirección base de la aplicación en la que se carga la imagen.</span><span class="sxs-lookup"><span data-stu-id="498da-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="498da-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="498da-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="498da-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="498da-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="498da-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="498da-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="498da-121">Calificadores: WmiDataId (3), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="498da-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="498da-122">Nombre de archivo y extensión del archivo DLL o la imagen ejecutable que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="498da-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="498da-123">Módulos</span><span class="sxs-lookup"><span data-stu-id="498da-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="498da-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="498da-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="498da-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="498da-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="498da-126">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="498da-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="498da-127">Tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="498da-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="498da-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="498da-128">Requirements</span></span>



| <span data-ttu-id="498da-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="498da-129">Requirement</span></span> | <span data-ttu-id="498da-130">Value</span><span class="sxs-lookup"><span data-stu-id="498da-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="498da-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="498da-131">Minimum supported client</span></span><br/> | <span data-ttu-id="498da-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="498da-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="498da-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="498da-133">Minimum supported server</span></span><br/> | <span data-ttu-id="498da-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="498da-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="498da-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="498da-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="498da-136">**Imagen \_ v0**</span><span class="sxs-lookup"><span data-stu-id="498da-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




