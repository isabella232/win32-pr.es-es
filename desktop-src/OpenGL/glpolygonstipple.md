---
title: función glPolygonStipple (GL. h)
description: La función glPolygonStipple establece el patrón punteado de polígono.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glPolygonStipple (función) OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491128"
---
# <a name="glpolygonstipple-function"></a><span data-ttu-id="94913-104">glPolygonStipple función)</span><span class="sxs-lookup"><span data-stu-id="94913-104">glPolygonStipple function</span></span>

<span data-ttu-id="94913-105">La función **glPolygonStipple** establece el patrón punteado de polígono.</span><span class="sxs-lookup"><span data-stu-id="94913-105">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="94913-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94913-106">Syntax</span></span>


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="94913-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94913-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94913-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="94913-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="94913-109">Un puntero a un patrón punteado de 32x32 que se desempaquetará de la memoria del mismo modo que [**glDrawPixels**](gldrawpixels.md) desempaqueta los píxeles.</span><span class="sxs-lookup"><span data-stu-id="94913-109">A pointer to a 32x32 stipple pattern that will be unpacked from memory in the same way that [**glDrawPixels**](gldrawpixels.md) unpacks pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94913-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94913-110">Return value</span></span>

<span data-ttu-id="94913-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="94913-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="94913-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="94913-112">Error codes</span></span>

<span data-ttu-id="94913-113">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="94913-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="94913-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="94913-114">Name</span></span>                                                                                                  | <span data-ttu-id="94913-115">Significado</span><span class="sxs-lookup"><span data-stu-id="94913-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94913-116"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="94913-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="94913-117">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="94913-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="94913-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94913-118">Remarks</span></span>

<span data-ttu-id="94913-119">La función **glPolygonStipple** establece el patrón punteado de polígono.</span><span class="sxs-lookup"><span data-stu-id="94913-119">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span> <span data-ttu-id="94913-120">El punteado de polígonos, como el punteado de línea (vea [**glLineStipple**](gllinestipple.md)), simplifica determinados fragmentos generados por la rasterización y crea un patrón.</span><span class="sxs-lookup"><span data-stu-id="94913-120">Polygon stippling, like line stippling (see [**glLineStipple**](gllinestipple.md)), masks out certain fragments produced by rasterization, creating a pattern.</span></span> <span data-ttu-id="94913-121">El punteado es independiente del suavizado de contorno de polígono.</span><span class="sxs-lookup"><span data-stu-id="94913-121">Stippling is independent of polygon antialiasing.</span></span>

<span data-ttu-id="94913-122">El parámetro *Mask* es un puntero a un patrón punteado de 32x32 que se almacena en memoria, al igual que los datos de píxeles suministrados a **glDrawPixels** con *alto* y *ancho* iguales a 32, un *formato* de píxel del índice de color GL \_ y un \_ *tipo* de datos de mapa de bits de GL \_ .</span><span class="sxs-lookup"><span data-stu-id="94913-122">The *mask* parameter is a pointer to a 32x32 stipple pattern that is stored in memory just like the pixel data supplied to **glDrawPixels** with *height* and *width* both equal to 32, a pixel *format* of GL\_COLOR\_INDEX, and data *type* of GL\_BITMAP.</span></span> <span data-ttu-id="94913-123">Es decir, el patrón punteado se representa como una matriz 32x32 de índices de color de 1 bit empaquetados en bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="94913-123">That is, the stipple pattern is represented as a 32x32 array of 1-bit color indexes packed in unsigned bytes.</span></span> <span data-ttu-id="94913-124">Los parámetros de la función [**glPixelStore**](glpixelstore-functions.md) , como los \_ \_ bytes de intercambio \_ de libro de contabilidad y \_ unpack \_ LSB \_ en primer lugar, afectan al montaje de los bits en un patrón punteado.</span><span class="sxs-lookup"><span data-stu-id="94913-124">The [**glPixelStore**](glpixelstore-functions.md) function parameters, such as GL\_UNPACK\_SWAP\_BYTES and GL\_UNPACK\_LSB\_FIRST, affect the assembling of the bits into a stipple pattern.</span></span> <span data-ttu-id="94913-125">Sin embargo, las operaciones de transferencia de píxeles (desplazamiento, desplazamiento y mapa de píxeles) no se aplican a la imagen de punteado.</span><span class="sxs-lookup"><span data-stu-id="94913-125">Pixel transfer operations (shift, offset, and pixel map) are not applied to the stipple image, however.</span></span>

<span data-ttu-id="94913-126">El punteado de polígono está habilitado y deshabilitado con [**glEnable**](glenable.md) y **glDisable**, mediante el argumento de la contabilidad de \_ polígonos \_ .</span><span class="sxs-lookup"><span data-stu-id="94913-126">Polygon stippling is enabled and disabled with [**glEnable**](glenable.md) and **glDisable**, using argument GL\_POLYGON\_STIPPLE.</span></span> <span data-ttu-id="94913-127">Si está habilitado, se envía un fragmento de polígono rasterizado con coordenadas *x*<sub>w</sub> *e y*<sub>w</sub> a la siguiente fase de OpenGL si y solo si el bit (*x*<sub>w</sub> mod 32) de la fila (*y*<sub>w</sub> mod 32) del patrón punteado es uno.</span><span class="sxs-lookup"><span data-stu-id="94913-127">If enabled, a rasterized polygon fragment with window coordinates *x*<sub>w</sub> and *y*<sub>w</sub> is sent to the next stage of OpenGL if and only if the (*x*<sub>w</sub> mod 32)th bit in the (*y*<sub>w</sub> mod 32)th row of the stipple pattern is one.</span></span> <span data-ttu-id="94913-128">Cuando el punteado de polígono está deshabilitado, es como si el patrón punteado fuera todo.</span><span class="sxs-lookup"><span data-stu-id="94913-128">When polygon stippling is disabled, it is as if the stipple pattern were all ones.</span></span>

<span data-ttu-id="94913-129">Las siguientes funciones recuperan información relacionada con **glPolygonStipple**:</span><span class="sxs-lookup"><span data-stu-id="94913-129">The following functions retrieve information related to **glPolygonStipple**:</span></span>

[<span data-ttu-id="94913-130">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="94913-130">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)

<span data-ttu-id="94913-131">[**glIsEnabled**](glisenabled.md) con \_ argumento cont. \_</span><span class="sxs-lookup"><span data-stu-id="94913-131">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="94913-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94913-132">Requirements</span></span>



| <span data-ttu-id="94913-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="94913-133">Requirement</span></span> | <span data-ttu-id="94913-134">Value</span><span class="sxs-lookup"><span data-stu-id="94913-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94913-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94913-135">Minimum supported client</span></span><br/> | <span data-ttu-id="94913-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="94913-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94913-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94913-137">Minimum supported server</span></span><br/> | <span data-ttu-id="94913-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94913-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94913-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94913-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="94913-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="94913-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="94913-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94913-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="94913-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94913-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94913-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94913-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94913-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94913-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94913-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="94913-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94913-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="94913-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="94913-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="94913-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="94913-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="94913-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="94913-149">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="94913-149">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="94913-150">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="94913-150">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="94913-151">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="94913-151">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> </dl>

 

 





