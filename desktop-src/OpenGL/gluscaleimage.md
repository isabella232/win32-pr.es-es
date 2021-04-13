---
title: función gluScaleImage (GLU. h)
description: La función gluScaleImage escala una imagen a un tamaño arbitrario.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluScaleImage (función) OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421902"
---
# <a name="gluscaleimage-function"></a><span data-ttu-id="3c151-104">gluScaleImage función)</span><span class="sxs-lookup"><span data-stu-id="3c151-104">gluScaleImage function</span></span>

<span data-ttu-id="3c151-105">La función **gluScaleImage** escala una imagen a un tamaño arbitrario.</span><span class="sxs-lookup"><span data-stu-id="3c151-105">The **gluScaleImage** function scales an image to an arbitrary size.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c151-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c151-106">Syntax</span></span>


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a><span data-ttu-id="3c151-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c151-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c151-108">*format*</span><span class="sxs-lookup"><span data-stu-id="3c151-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-109">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="3c151-109">The format of the pixel data.</span></span> <span data-ttu-id="3c151-110">Los valores simbólicos siguientes son válidos: el \_ Índice de color \_ de GL, el \_ Índice de la galería de símbolos GL \_ , el \_ componente de profundidad de contabilidad \_ , GL \_ rojo, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ , GL BGRA ext, GL de \_ \_ Contabilidad y la luminancia de \_ GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3c151-110">The following symbolic values are valid: GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, GL\_DEPTH\_COMPONENT, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="3c151-111">*ancho*</span><span class="sxs-lookup"><span data-stu-id="3c151-111">*widthin*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-112">Ancho de la imagen de origen que se escala.</span><span class="sxs-lookup"><span data-stu-id="3c151-112">The width of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="3c151-113">*alto*</span><span class="sxs-lookup"><span data-stu-id="3c151-113">*heightin*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-114">Alto de la imagen de origen que se escala.</span><span class="sxs-lookup"><span data-stu-id="3c151-114">The height of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="3c151-115">*escribir*</span><span class="sxs-lookup"><span data-stu-id="3c151-115">*typein*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-116">El tipo de datos para los *datos*.</span><span class="sxs-lookup"><span data-stu-id="3c151-116">The data type for *datain*.</span></span> <span data-ttu-id="3c151-117">Debe ser uno de los siguientes: \_ bytes sin signo de libro \_ de contabilidad, \_ bytes de contabilidad, mapa de bits de GL \_ , GL \_ sin signo \_ corto, GL \_ Short, libro de contabilidad \_ sin signo \_ \_ \_ de contab.</span><span class="sxs-lookup"><span data-stu-id="3c151-117">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="3c151-118">*datos*</span><span class="sxs-lookup"><span data-stu-id="3c151-118">*datain*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-119">Puntero a la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="3c151-119">A pointer to the source image.</span></span>

</dd> <dt>

<span data-ttu-id="3c151-120">*widthout*</span><span class="sxs-lookup"><span data-stu-id="3c151-120">*widthout*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-121">Ancho de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="3c151-121">The width of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="3c151-122">*heightout*</span><span class="sxs-lookup"><span data-stu-id="3c151-122">*heightout*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-123">Alto de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="3c151-123">The height of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="3c151-124">*typeout*</span><span class="sxs-lookup"><span data-stu-id="3c151-124">*typeout*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-125">El tipo de datos para *dataout*.</span><span class="sxs-lookup"><span data-stu-id="3c151-125">The data type for *dataout*.</span></span> <span data-ttu-id="3c151-126">Debe ser uno de los siguientes: \_ bytes sin signo de libro \_ de contabilidad, \_ bytes de contabilidad, mapa de bits de GL \_ , GL \_ sin signo \_ corto, GL \_ Short, libro de contabilidad \_ sin signo \_ \_ \_ de contab.</span><span class="sxs-lookup"><span data-stu-id="3c151-126">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="3c151-127">*dataout*</span><span class="sxs-lookup"><span data-stu-id="3c151-127">*dataout*</span></span> 
</dt> <dd>

<span data-ttu-id="3c151-128">Puntero a la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="3c151-128">A pointer to the destination image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c151-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c151-129">Return value</span></span>

<span data-ttu-id="3c151-130">Si la función es correcta, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="3c151-130">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="3c151-131">Si se produce un error en la función, el valor devuelto es un código de error GLU (vea [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="3c151-131">If the function fails, the return value is a GLU error code (see [**gluErrorString**](gluerrorstring.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c151-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c151-132">Remarks</span></span>

<span data-ttu-id="3c151-133">La función **gluScaleImage** escala una imagen de píxeles usando los modos de almacén de píxeles adecuados para desempaquetar los datos de la imagen de origen y empaquetar los datos en la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="3c151-133">The **gluScaleImage** function scales a pixel image using the appropriate pixel store modes to unpack data from the source image and pack data into the destination image.</span></span>

<span data-ttu-id="3c151-134">Al reducir una imagen, **gluScaleImage** usa un filtro de cuadro para muestrear la imagen de origen y crear píxeles para la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="3c151-134">When shrinking an image, **gluScaleImage** uses a box filter to sample the source image and create pixels for the destination image.</span></span> <span data-ttu-id="3c151-135">Al aumentar una imagen, los píxeles de la imagen de origen se interpolan linealmente para crear la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="3c151-135">When magnifying an image, the pixels from the source image are linearly interpolated to create the destination image.</span></span>

<span data-ttu-id="3c151-136">Para obtener una descripción de los valores aceptables para los parámetros *Format*, *typeof* y *typeout* , consulte [**glReadPixels**](glreadpixels.md).</span><span class="sxs-lookup"><span data-stu-id="3c151-136">For a description of the acceptable values for the *format*, *typein*, and *typeout* parameters, see [**glReadPixels**](glreadpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c151-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c151-137">Requirements</span></span>



| <span data-ttu-id="3c151-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c151-138">Requirement</span></span> | <span data-ttu-id="3c151-139">Value</span><span class="sxs-lookup"><span data-stu-id="3c151-139">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3c151-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c151-140">Minimum supported client</span></span><br/> | <span data-ttu-id="3c151-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3c151-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3c151-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c151-142">Minimum supported server</span></span><br/> | <span data-ttu-id="3c151-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c151-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3c151-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c151-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c151-145"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-145"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="3c151-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c151-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c151-147"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-147"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c151-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c151-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c151-149"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-149"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c151-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c151-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c151-151">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="3c151-151">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="3c151-152">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="3c151-152">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="3c151-153">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="3c151-153">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="3c151-154">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="3c151-154">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="3c151-155">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="3c151-155">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> </dl>

 

 





