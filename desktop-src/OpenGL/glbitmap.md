---
title: función glBitmap (GL. h)
description: La función glBitmap dibuja un mapa de bits.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glBitmap (función) OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079478"
---
# <a name="glbitmap-function"></a><span data-ttu-id="6ee41-104">glBitmap función)</span><span class="sxs-lookup"><span data-stu-id="6ee41-104">glBitmap function</span></span>

<span data-ttu-id="6ee41-105">La función **glBitmap** dibuja un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-105">The **glBitmap** function draws a bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee41-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ee41-106">Syntax</span></span>


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a><span data-ttu-id="6ee41-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ee41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee41-108">*width*</span><span class="sxs-lookup"><span data-stu-id="6ee41-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee41-109">Ancho en píxeles de la imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-109">The pixel width of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="6ee41-110">*height*</span><span class="sxs-lookup"><span data-stu-id="6ee41-110">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee41-111">Alto en píxeles de la imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-111">The pixel height of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="6ee41-112">*xorig*</span><span class="sxs-lookup"><span data-stu-id="6ee41-112">*xorig*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee41-113">Ubicación *x* del origen en la imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-113">The *x* location of the origin in the bitmap image.</span></span> <span data-ttu-id="6ee41-114">El origen se mide desde la esquina inferior izquierda del mapa de bits, con las direcciones correctas y hacia arriba que son los ejes positivos.</span><span class="sxs-lookup"><span data-stu-id="6ee41-114">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="6ee41-115">*yorig*</span><span class="sxs-lookup"><span data-stu-id="6ee41-115">*yorig*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee41-116">Ubicación *y* del origen en la imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-116">The *y* location of the origin in the bitmap image.</span></span> <span data-ttu-id="6ee41-117">El origen se mide desde la esquina inferior izquierda del mapa de bits, con las direcciones correctas y hacia arriba que son los ejes positivos.</span><span class="sxs-lookup"><span data-stu-id="6ee41-117">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="6ee41-118">*xmove*</span><span class="sxs-lookup"><span data-stu-id="6ee41-118">*xmove*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee41-119">Desplazamiento *x* que se va a agregar a la posición de la cuadrícula actual después de dibujar el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-119">The *x* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="6ee41-120">*ymove*</span><span class="sxs-lookup"><span data-stu-id="6ee41-120">*ymove*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee41-121">Desplazamiento *y* que se va a agregar a la posición de la cuadrícula actual después de dibujar el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-121">The *y* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="6ee41-122">*bitmap*</span><span class="sxs-lookup"><span data-stu-id="6ee41-122">*bitmap*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee41-123">Dirección de la imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-123">The address of the bitmap image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee41-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ee41-124">Return value</span></span>

<span data-ttu-id="6ee41-125">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6ee41-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6ee41-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6ee41-126">Error codes</span></span>

<span data-ttu-id="6ee41-127">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="6ee41-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6ee41-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="6ee41-128">Name</span></span>                                                                                                  | <span data-ttu-id="6ee41-129">Significado</span><span class="sxs-lookup"><span data-stu-id="6ee41-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ee41-130"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ee41-130"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="6ee41-131">el *ancho* o el *alto* es negativo.</span><span class="sxs-lookup"><span data-stu-id="6ee41-131">*width* or *height* is negative.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="6ee41-132"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ee41-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6ee41-133">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6ee41-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6ee41-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ee41-134">Remarks</span></span>

<span data-ttu-id="6ee41-135">Un mapa de bits es una imagen binaria.</span><span class="sxs-lookup"><span data-stu-id="6ee41-135">A bitmap is a binary image.</span></span> <span data-ttu-id="6ee41-136">Cuando se dibuja, el mapa de bits se coloca en relación con la posición de la trama actual y los píxeles de fotogramas correspondientes a 1s en el mapa de bits se escriben utilizando el color o el índice de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="6ee41-136">When drawn, the bitmap is positioned relative to the current raster position, and framebuffer pixels corresponding to 1s in the bitmap are written using the current raster color or index.</span></span> <span data-ttu-id="6ee41-137">Los píxeles de búfer de fotogramas correspondientes a ceros en el mapa de bits no se modifican.</span><span class="sxs-lookup"><span data-stu-id="6ee41-137">Frame-buffer pixels corresponding to zeros in the bitmap are not modified.</span></span>

<span data-ttu-id="6ee41-138">La imagen de mapa de bits se interpreta como los datos de imagen de la función [**glDrawPixels**](gldrawpixels.md) , con el *ancho* y el *alto* que se corresponden con los argumentos de ancho y alto de esa función, y con el *tipo* establecido en el mapa de bits de contabilidad \_ y el *formato* establecido en Índice de \_ color GL \_ .</span><span class="sxs-lookup"><span data-stu-id="6ee41-138">The bitmap image is interpreted like image data for the [**glDrawPixels**](gldrawpixels.md) function, with *width* and *height* corresponding to the width and height arguments of that function, and with *type* set to GL\_BITMAP and *format* set to GL\_COLOR\_INDEX.</span></span> <span data-ttu-id="6ee41-139">Los modos que se especifican mediante [**glPixelStore**](glpixelstore-functions.md) afectan a la interpretación de los datos de imagen de mapa de bits. los modos que se especifican con [**glPixelTransfer**](glpixeltransfer.md) no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="6ee41-139">Modes you specify using [**glPixelStore**](glpixelstore-functions.md) affect the interpretation of bitmap image data; modes you specify using [**glPixelTransfer**](glpixeltransfer.md) do not.</span></span>

<span data-ttu-id="6ee41-140">Si la posición de la trama actual no es válida, se omite **glBitmap** .</span><span class="sxs-lookup"><span data-stu-id="6ee41-140">If the current raster position is invalid, **glBitmap** is ignored.</span></span> <span data-ttu-id="6ee41-141">De lo contrario, la esquina inferior izquierda de la imagen de mapa de bits se coloca en las siguientes coordenadas de la ventana:</span><span class="sxs-lookup"><span data-stu-id="6ee41-141">Otherwise, the lower-left corner of the bitmap image is positioned at the following window coordinates:</span></span>

<span data-ttu-id="6ee41-142">*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*</span><span class="sxs-lookup"><span data-stu-id="6ee41-142">*x*<sub>w</sub> = *x*<sub>r</sub> *x*?</span></span>

<span data-ttu-id="6ee41-143">*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?</span><span class="sxs-lookup"><span data-stu-id="6ee41-143">*y*<sub>w</sub> = *y*<sub>r</sub> *y*?</span></span>

<span data-ttu-id="6ee41-144">En estas coordenadas, (*x*<sub>r</sub> , *y*<sub>r</sub> ) es la posición de la trama y (*x*?</span><span class="sxs-lookup"><span data-stu-id="6ee41-144">In these coordinates, (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the raster position, and (*x*?</span></span> <span data-ttu-id="6ee41-145">, *y*?</span><span class="sxs-lookup"><span data-stu-id="6ee41-145">, *y*?</span></span> <span data-ttu-id="6ee41-146">) es el origen del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-146">) is the bitmap origin.</span></span> <span data-ttu-id="6ee41-147">A continuación, se generan fragmentos para cada píxel correspondiente a un 1 en la imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ee41-147">Fragments are then generated for each pixel corresponding to a 1 in the bitmap image.</span></span> <span data-ttu-id="6ee41-148">Estos fragmentos se generan utilizando la coordenada *z* de rasterización actual, el color o el índice de color y las coordenadas de textura de rasterizado actuales.</span><span class="sxs-lookup"><span data-stu-id="6ee41-148">These fragments are generated using the current raster *z*-coordinate, color or color index, and current raster texture coordinates.</span></span> <span data-ttu-id="6ee41-149">A continuación, se tratan como si hubieran sido generados por un punto, línea o polígono, incluida la asignación de texturas, la luneta térmica y todas las operaciones por fragmento, como las pruebas alfa y de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6ee41-149">They are then treated just as if they had been generated by a point, line, or polygon, including texture mapping, fogging, and all per-fragment operations such as alpha and depth testing.</span></span>

<span data-ttu-id="6ee41-150">Una vez dibujado el mapa de bits, *xmove* y *ymove* desplazan las coordenadas *x* *e y* de la posición de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="6ee41-150">After the bitmap has been drawn, the *x* and *y* coordinates of the current raster position are offset by *xmove* and *ymove*.</span></span> <span data-ttu-id="6ee41-151">No se realiza ningún cambio en la coordenada *z* de la posición de la trama actual ni en las coordenadas de color, índice o textura de la trama actual.</span><span class="sxs-lookup"><span data-stu-id="6ee41-151">No change is made to the *z*-coordinate of the current raster position, or to the current raster color, index, or texture coordinates.</span></span>

<span data-ttu-id="6ee41-152">Las siguientes funciones recuperan información relacionada con la función **glBitmap** :</span><span class="sxs-lookup"><span data-stu-id="6ee41-152">The following functions retrieve information related to the **glBitmap** function:</span></span>

<span data-ttu-id="6ee41-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ posición de RASTERIZAción actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="6ee41-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

 

<span data-ttu-id="6ee41-154">**glGet** con el argumento \_ \_ color de RASTERIZAdo actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="6ee41-154">**glGet** with argument GL\_CURRENT\_RASTER\_COLOR</span></span>

 

<span data-ttu-id="6ee41-155">**glGet** con el argumento \_ \_ Índice de trama actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="6ee41-155">**glGet** with argument GL\_CURRENT\_RASTER\_INDEX</span></span>

 

<span data-ttu-id="6ee41-156">**glGet** con argumento de \_ \_ textura de RASTERIZAdo actual \_ de GL \_</span><span class="sxs-lookup"><span data-stu-id="6ee41-156">**glGet** with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>

 

<span data-ttu-id="6ee41-157">**glGet** con argumento de \_ posición de rasterizado actual de GL \_ \_ \_ válido</span><span class="sxs-lookup"><span data-stu-id="6ee41-157">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee41-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ee41-158">Requirements</span></span>



| <span data-ttu-id="6ee41-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee41-159">Requirement</span></span> | <span data-ttu-id="6ee41-160">Value</span><span class="sxs-lookup"><span data-stu-id="6ee41-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee41-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ee41-161">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee41-162">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6ee41-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6ee41-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ee41-163">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee41-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ee41-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ee41-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ee41-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ee41-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee41-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6ee41-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ee41-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ee41-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ee41-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ee41-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ee41-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee41-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ee41-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee41-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ee41-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee41-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6ee41-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6ee41-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="6ee41-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="6ee41-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6ee41-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6ee41-175">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="6ee41-175">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="6ee41-176">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="6ee41-176">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="6ee41-177">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="6ee41-177">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> </dl>

 

 





