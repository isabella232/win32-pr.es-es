---
title: función glScissor (GL. h)
description: La función glScissor define el cuadro tijeras.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glScissor (función) OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493024"
---
# <a name="glscissor-function"></a><span data-ttu-id="0842d-104">glScissor función)</span><span class="sxs-lookup"><span data-stu-id="0842d-104">glScissor function</span></span>

<span data-ttu-id="0842d-105">La función **glScissor** define el cuadro tijeras.</span><span class="sxs-lookup"><span data-stu-id="0842d-105">The **glScissor** function defines the scissor box.</span></span>

## <a name="syntax"></a><span data-ttu-id="0842d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0842d-106">Syntax</span></span>


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="0842d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0842d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0842d-108">*x*</span><span class="sxs-lookup"><span data-stu-id="0842d-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="0842d-109">La coordenada x (eje vertical) de la esquina inferior izquierda del cuadro de tijeras.</span><span class="sxs-lookup"><span data-stu-id="0842d-109">The x (vertical axis) coordinate for the lower-left corner of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="0842d-110">*y*</span><span class="sxs-lookup"><span data-stu-id="0842d-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="0842d-111">Coordenada y (eje horizontal) de la esquina inferior izquierda del cuadro de tijeras.</span><span class="sxs-lookup"><span data-stu-id="0842d-111">The y (horizontal axis) coordinate for the lower-left corner of the scissor box.</span></span> <span data-ttu-id="0842d-112">Juntos, x e y especifican la esquina inferior izquierda del cuadro de tijeras.</span><span class="sxs-lookup"><span data-stu-id="0842d-112">Together, x and y specify the lower-left corner of the scissor box.</span></span> <span data-ttu-id="0842d-113">Inicialmente (0,0).</span><span class="sxs-lookup"><span data-stu-id="0842d-113">Initially (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="0842d-114">*width*</span><span class="sxs-lookup"><span data-stu-id="0842d-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="0842d-115">Ancho del cuadro de tijera.</span><span class="sxs-lookup"><span data-stu-id="0842d-115">The width of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="0842d-116">*height*</span><span class="sxs-lookup"><span data-stu-id="0842d-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="0842d-117">Alto del cuadro de tijeras.</span><span class="sxs-lookup"><span data-stu-id="0842d-117">The height of the scissor box.</span></span> <span data-ttu-id="0842d-118">Cuando un contexto OpenGL se adjunta *primero* a una ventana, el *ancho* y el *alto* se establecen en las dimensiones de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="0842d-118">When an OpenGL context is *first* attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0842d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0842d-119">Return value</span></span>

<span data-ttu-id="0842d-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0842d-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0842d-121">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0842d-121">Error codes</span></span>

<span data-ttu-id="0842d-122">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="0842d-122">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0842d-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="0842d-123">Name</span></span>                                                                                                  | <span data-ttu-id="0842d-124">Significado</span><span class="sxs-lookup"><span data-stu-id="0842d-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0842d-125"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0842d-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="0842d-126">El *ancho* o el *alto* era negativo.</span><span class="sxs-lookup"><span data-stu-id="0842d-126">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="0842d-127"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0842d-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0842d-128">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0842d-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0842d-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0842d-129">Remarks</span></span>

<span data-ttu-id="0842d-130">La función **glScissor** define un rectángulo, denominado el cuadro tijeras, en coordenadas de ventana.</span><span class="sxs-lookup"><span data-stu-id="0842d-130">The **glScissor** function defines a rectangle, called the scissor box, in window coordinates.</span></span> <span data-ttu-id="0842d-131">Los dos primeros parámetros, *x* e *y*, especifican la esquina inferior izquierda del cuadro.</span><span class="sxs-lookup"><span data-stu-id="0842d-131">The first two parameters, *x* and *y*, specify the lower-left corner of the box.</span></span> <span data-ttu-id="0842d-132">Los parámetros de *ancho* y *alto* especifican el ancho y el alto del cuadro.</span><span class="sxs-lookup"><span data-stu-id="0842d-132">The *width* and *height* parameters specify the width and height of the box.</span></span>

<span data-ttu-id="0842d-133">La prueba de tijera está habilitada y deshabilitada mediante [**glEnable**](glenable.md) y **glDisable** con la prueba de tijeras GL de argumento \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0842d-133">The scissor test is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_SCISSOR\_TEST.</span></span> <span data-ttu-id="0842d-134">Mientras la prueba de tijeras está habilitada, solo se pueden modificar los píxeles que se encuentran dentro del cuadro de tijera.</span><span class="sxs-lookup"><span data-stu-id="0842d-134">While the scissor test is enabled, only pixels that lie within the scissor box can be modified by drawing commands.</span></span> <span data-ttu-id="0842d-135">Las coordenadas de la ventana tienen valores enteros en las esquinas compartidas de fotogramas píxeles, de modo que **glScissor**(0, 0, 1, 1) permite que solo se modifique el píxel inferior izquierdo de la ventana y **glScissor**(0,0, 0, 0) no permite la modificación en todos los píxeles de la ventana.</span><span class="sxs-lookup"><span data-stu-id="0842d-135">Window coordinates have integer values at the shared corners of framebuffer pixels, so **glScissor**(0,0,1,1) allows only the lower-left pixel in the window to be modified, and **glScissor**(0,0,0,0) disallows modification to all pixels in the window.</span></span>

<span data-ttu-id="0842d-136">Cuando la prueba de tijeras está deshabilitada, es como si el cuadro de tijeras incluye toda la ventana.</span><span class="sxs-lookup"><span data-stu-id="0842d-136">When the scissor test is disabled, it is as though the scissor box includes the entire window.</span></span>

<span data-ttu-id="0842d-137">Las siguientes funciones recuperan información relacionada con **glScissor**:</span><span class="sxs-lookup"><span data-stu-id="0842d-137">The following functions retrieve information related to **glScissor**:</span></span>

<span data-ttu-id="0842d-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) cuadro con el \_ argumento \_</span><span class="sxs-lookup"><span data-stu-id="0842d-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SCISSOR\_BOX</span></span>

<span data-ttu-id="0842d-139">[**glIsEnabled**](glisenabled.md) con argumento de la \_ prueba de tijeras GL \_</span><span class="sxs-lookup"><span data-stu-id="0842d-139">[**glIsEnabled**](glisenabled.md) with argument GL\_SCISSOR\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="0842d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0842d-140">Requirements</span></span>



| <span data-ttu-id="0842d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0842d-141">Requirement</span></span> | <span data-ttu-id="0842d-142">Value</span><span class="sxs-lookup"><span data-stu-id="0842d-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0842d-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0842d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0842d-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0842d-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0842d-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0842d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0842d-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0842d-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0842d-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0842d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="0842d-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0842d-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0842d-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0842d-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="0842d-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0842d-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0842d-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0842d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0842d-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0842d-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0842d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="0842d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0842d-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0842d-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0842d-155">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="0842d-155">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="0842d-156">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0842d-156">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0842d-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0842d-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="0842d-158">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="0842d-158">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





