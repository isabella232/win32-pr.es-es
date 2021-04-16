---
description: El \_ tipo de \_ enumeración de tipos de análisis de vídeo de WPD \_ describe cómo se codifican los campos de un archivo de vídeo.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Enumeración WPD_VIDEO_SCAN_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649534"
---
# <a name="wpd_video_scan_types-enumeration"></a><span data-ttu-id="509b3-103">\_ \_ Enumeración de tipos de análisis de vídeo de WPD \_</span><span class="sxs-lookup"><span data-stu-id="509b3-103">WPD\_VIDEO\_SCAN\_TYPES enumeration</span></span>

<span data-ttu-id="509b3-104">El tipo de enumeración de tipos de análisis de vídeo de WPD describe cómo se codifican los campos de un archivo de vídeo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="509b3-104">The **WPD\_VIDEO\_SCAN\_TYPES** enumeration type describes how the fields in a video file are encoded.</span></span>

## <a name="syntax"></a><span data-ttu-id="509b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="509b3-105">Syntax</span></span>


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="509b3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="509b3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="509b3-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**tipo de examen de vídeo de WPD sin \_ \_ \_ \_ usar**</span><span class="sxs-lookup"><span data-stu-id="509b3-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD\_VIDEO\_SCAN\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="509b3-108">El tipo de examen no se ha definido para este archivo de vídeo o no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="509b3-108">The scan type has not been defined for this video file, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="509b3-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**tipo de examen de vídeo de WPD \_ \_ \_ \_ progresiva**</span><span class="sxs-lookup"><span data-stu-id="509b3-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="509b3-110">Un archivo de vídeo de análisis progresivo.</span><span class="sxs-lookup"><span data-stu-id="509b3-110">A progressive scan video file.</span></span>

</dd> <dt>

<span data-ttu-id="509b3-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**campo de tipo de examen de vídeo de WPD \_ \_ \_ \_ \_ entrelazado \_ superior \_ primero**</span><span class="sxs-lookup"><span data-stu-id="509b3-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="509b3-112">Un archivo de vídeo intercalado en el que se dibujan primero los campos alternativos y el campo superior (con la línea 1).</span><span class="sxs-lookup"><span data-stu-id="509b3-112">An interleaved video file where the fields alternate and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="509b3-113">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="509b3-113">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="509b3-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**campo de tipo de examen de vídeo de WPD \_ \_ \_ \_ \_ entrelazado \_ inferior \_ primero**</span><span class="sxs-lookup"><span data-stu-id="509b3-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="509b3-115">Un archivo de vídeo intercalado en el que se dibujan primero los campos alternativos y el campo inferior (con la línea 2).</span><span class="sxs-lookup"><span data-stu-id="509b3-115">An interleaved video file where the fields alternate and the lower field (with line 2) is drawn first.</span></span> <span data-ttu-id="509b3-116">Para obtener más información, vea la sección comentarios que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="509b3-116">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="509b3-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**campo de tipo de examen de vídeo de WPD \_ \_ \_ \_ \_ único \_ \_ primero superior**</span><span class="sxs-lookup"><span data-stu-id="509b3-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="509b3-118">Un archivo de vídeo intercalado en el que los campos se envían como muestras contiguas y el campo superior (con la línea 1) se dibuja primero.</span><span class="sxs-lookup"><span data-stu-id="509b3-118">An interleaved video file where the fields are sent as contiguous samples and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="509b3-119">Para obtener más información, vea la sección comentarios que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="509b3-119">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="509b3-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**campo de tipo de examen de vídeo de WPD \_ \_ \_ \_ \_ único \_ inferior \_ primero**</span><span class="sxs-lookup"><span data-stu-id="509b3-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="509b3-121">Un archivo de vídeo intercalado en el que los campos se envían como muestras contiguas y el campo inferior (con la línea 2) se envía primero.</span><span class="sxs-lookup"><span data-stu-id="509b3-121">An interleaved video file where the fields are sent as contiguous samples and the lower field (with line 2) is sent first.</span></span>

</dd> <dt>

<span data-ttu-id="509b3-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**tipo de escaneo de vídeo de WPD \_ \_ \_ \_ mezclado \_ entrelazado**</span><span class="sxs-lookup"><span data-stu-id="509b3-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE**</span></span>
</dt> <dd>

<span data-ttu-id="509b3-123">Un archivo de vídeo con una combinación de modos de entrelazado.</span><span class="sxs-lookup"><span data-stu-id="509b3-123">A video file with a mix of interlacing modes.</span></span>

</dd> <dt>

<span data-ttu-id="509b3-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_ \_ \_ tipo \_ de escaneo de vídeo de WPD mezclado \_ entrelazado \_ y \_ progresivo**</span><span class="sxs-lookup"><span data-stu-id="509b3-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE\_AND\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="509b3-125">Un archivo de vídeo con una combinación de modos entrelazados y progresivos.</span><span class="sxs-lookup"><span data-stu-id="509b3-125">A video file with a mix of interlaced and progressive modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="509b3-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="509b3-126">Remarks</span></span>

<span data-ttu-id="509b3-127">Esta enumeración se usa en la propiedad [tipo de examen de vídeo de WPD \_ \_ \_ ](properties-and-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="509b3-127">This enumeration is used by the [WPD\_VIDEO\_SCAN\_TYPE](properties-and-attributes.md) property.</span></span>

<span data-ttu-id="509b3-128">Hay dos tipos de formatos de archivo intercalados que se especifican mediante esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="509b3-128">There are two types of interleaved file formats that are specified by this enumeration.</span></span> <span data-ttu-id="509b3-129">**WPD \_ El \_ campo de tipo de examen de vídeo \_ \_ \_ intercalado** se refiere a un formato de archivo en el que se entregan fotogramas, ya que se han analizado los campos alternativos y los datos aparecen línea por línea, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="509b3-129">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED** refers to a file format where frames are delivered as they were scanned fields alternate and data goes line by line, as shown here:</span></span>

<span data-ttu-id="509b3-130">**Fotograma 1**</span><span class="sxs-lookup"><span data-stu-id="509b3-130">**Frame 1**</span></span>

<span data-ttu-id="509b3-131">Campo 1: línea 1</span><span class="sxs-lookup"><span data-stu-id="509b3-131">Field 1: Line 1</span></span>

<span data-ttu-id="509b3-132">Campo 2: línea 1</span><span class="sxs-lookup"><span data-stu-id="509b3-132">Field 2: Line 1</span></span>

<span data-ttu-id="509b3-133">Campo 1: línea 2</span><span class="sxs-lookup"><span data-stu-id="509b3-133">Field 1: Line 2</span></span>

<span data-ttu-id="509b3-134">Campo 2: línea 2</span><span class="sxs-lookup"><span data-stu-id="509b3-134">Field 2: Line 2</span></span>

<span data-ttu-id="509b3-135">Campo 1: línea 3</span><span class="sxs-lookup"><span data-stu-id="509b3-135">Field 1: Line 3</span></span>

<span data-ttu-id="509b3-136">Campo 2: línea 3</span><span class="sxs-lookup"><span data-stu-id="509b3-136">Field 2: Line 3</span></span>

<span data-ttu-id="509b3-137">...</span><span class="sxs-lookup"><span data-stu-id="509b3-137">...</span></span>

<span data-ttu-id="509b3-138">**WPD \_ Campo de tipo de examen de vídeo \_ \_ \_ \_ único** hace referencia a un formato de archivo donde cada campo se almacena en un único bloque de líneas de análisis y los campos se almacenan secuencialmente, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="509b3-138">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE** refers to a file format where each field is stored in a single block of scan lines, and fields are stored sequentially, as shown here:</span></span>

<span data-ttu-id="509b3-139">**Fotograma 1**</span><span class="sxs-lookup"><span data-stu-id="509b3-139">**Frame 1**</span></span>

<span data-ttu-id="509b3-140">Campo 1: línea 1</span><span class="sxs-lookup"><span data-stu-id="509b3-140">Field 1: Line 1</span></span>

<span data-ttu-id="509b3-141">Campo 1: línea 2</span><span class="sxs-lookup"><span data-stu-id="509b3-141">Field 1: Line 2</span></span>

<span data-ttu-id="509b3-142">Campo 1: línea 3</span><span class="sxs-lookup"><span data-stu-id="509b3-142">Field 1: Line 3</span></span>

<span data-ttu-id="509b3-143">...</span><span class="sxs-lookup"><span data-stu-id="509b3-143">...</span></span>

<span data-ttu-id="509b3-144">Seguido de</span><span class="sxs-lookup"><span data-stu-id="509b3-144">Followed by</span></span>

<span data-ttu-id="509b3-145">Campo 2: línea 1</span><span class="sxs-lookup"><span data-stu-id="509b3-145">Field 2: Line 1</span></span>

<span data-ttu-id="509b3-146">Campo 2: línea 2</span><span class="sxs-lookup"><span data-stu-id="509b3-146">Field 2: Line 2</span></span>

<span data-ttu-id="509b3-147">Campo 2: línea 3</span><span class="sxs-lookup"><span data-stu-id="509b3-147">Field 2: Line 3</span></span>

<span data-ttu-id="509b3-148">...</span><span class="sxs-lookup"><span data-stu-id="509b3-148">...</span></span>

## <a name="requirements"></a><span data-ttu-id="509b3-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="509b3-149">Requirements</span></span>



| <span data-ttu-id="509b3-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="509b3-150">Requirement</span></span> | <span data-ttu-id="509b3-151">Value</span><span class="sxs-lookup"><span data-stu-id="509b3-151">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="509b3-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="509b3-152">Header</span></span><br/> | <dl> <span data-ttu-id="509b3-153"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="509b3-153"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="509b3-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="509b3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="509b3-155">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="509b3-155">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




