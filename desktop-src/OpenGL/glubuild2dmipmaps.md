---
title: función gluBuild2DMipmaps (GLU. h)
description: La función gluBuild2DMipmaps crea mapas de bits 2D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- gluBuild2DMipmaps (función) OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996093"
---
# <a name="glubuild2dmipmaps-function"></a><span data-ttu-id="f4fa5-104">gluBuild2DMipmaps función)</span><span class="sxs-lookup"><span data-stu-id="f4fa5-104">gluBuild2DMipmaps function</span></span>

<span data-ttu-id="f4fa5-105">La función **gluBuild2DMipmaps** crea mapas de bits 2D.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-105">The **gluBuild2DMipmaps** function creates 2-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4fa5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4fa5-106">Syntax</span></span>


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="f4fa5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4fa5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4fa5-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="f4fa5-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fa5-109">Textura de destino.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-109">The target texture.</span></span> <span data-ttu-id="f4fa5-110">Debe ser la \_ textura de GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="f4fa5-111">*components*</span><span class="sxs-lookup"><span data-stu-id="f4fa5-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fa5-112">El número de componentes de color de la textura.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-112">The number of color components in the texture.</span></span> <span data-ttu-id="f4fa5-113">Debe ser 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="f4fa5-114">*width*</span><span class="sxs-lookup"><span data-stu-id="f4fa5-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fa5-115">Ancho de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="f4fa5-116">*height*</span><span class="sxs-lookup"><span data-stu-id="f4fa5-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fa5-117">Alto de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-117">The height of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="f4fa5-118">*format*</span><span class="sxs-lookup"><span data-stu-id="f4fa5-118">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fa5-119">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-119">The format of the pixel data.</span></span> <span data-ttu-id="f4fa5-120">Debe ser uno de los siguientes: GL \_ color \_ index, GL \_ rojo, GL \_ Green, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, \_ luminancia de GL o luminancia de contabilidad general \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f4fa5-120">Must be one of the following: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="f4fa5-121">*type*</span><span class="sxs-lookup"><span data-stu-id="f4fa5-121">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fa5-122">El tipo de datos para los *datos*.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-122">The data type for *data*.</span></span> <span data-ttu-id="f4fa5-123">Debe ser uno de los siguientes: \_ bytes sin signo de libro \_ de contabilidad, \_ bytes de contabilidad, mapa de bits de GL \_ , GL \_ sin signo \_ corto, GL \_ Short, libro de contabilidad \_ sin signo \_ \_ \_ de contab.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-123">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="f4fa5-124">*data*</span><span class="sxs-lookup"><span data-stu-id="f4fa5-124">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fa5-125">Puntero a los datos de la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-125">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4fa5-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4fa5-126">Return value</span></span>

<span data-ttu-id="f4fa5-127">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4fa5-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4fa5-128">Remarks</span></span>

<span data-ttu-id="f4fa5-129">La función **gluBuild2DMipmaps** obtiene la imagen de entrada y genera todas las imágenes de mipmap (mediante [**gluScaleImage**](gluscaleimage.md)), por lo que la imagen de entrada se puede usar como imagen de textura de mipmapped.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-129">The **gluBuild2DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="f4fa5-130">Para cargar cada una de las imágenes, llame a [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="f4fa5-130">To load each of the images, call [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="f4fa5-131">Si las dimensiones de la imagen de entrada no son potencias de dos, la imagen se escala para que el ancho y el alto sean potencias de dos antes de que se generen los mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-131">If the dimensions of the input image are not powers of two, then the image is scaled so that both the width and height are powers of two before the mipmaps are generated.</span></span>

<span data-ttu-id="f4fa5-132">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-132">A return value of zero indicates success.</span></span> <span data-ttu-id="f4fa5-133">De lo contrario, se devuelve un código de error GLU (vea [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="f4fa5-133">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="f4fa5-134">Para obtener una descripción de los valores aceptables para el parámetro *Format* , vea **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-134">For a description of the acceptable values for the *format* parameter, see **glTexImage2D**.</span></span> <span data-ttu-id="f4fa5-135">Para obtener una descripción de los valores aceptables para el *tipo*, vea [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="f4fa5-135">For a description of the acceptable values for *type*, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4fa5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4fa5-136">Requirements</span></span>



| <span data-ttu-id="f4fa5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4fa5-137">Requirement</span></span> | <span data-ttu-id="f4fa5-138">Value</span><span class="sxs-lookup"><span data-stu-id="f4fa5-138">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f4fa5-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4fa5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f4fa5-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f4fa5-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f4fa5-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4fa5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f4fa5-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4fa5-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f4fa5-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4fa5-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4fa5-144"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4fa5-144"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f4fa5-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4fa5-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4fa5-146"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4fa5-146"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f4fa5-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4fa5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4fa5-148"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4fa5-148"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4fa5-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4fa5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4fa5-150">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="f4fa5-150">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="f4fa5-151">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="f4fa5-151">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="f4fa5-152">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="f4fa5-152">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="f4fa5-153">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="f4fa5-153">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





