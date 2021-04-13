---
title: función glAddSwapHintRectWIN (GL. h)
description: La función de devolución de llamada glAddSwapHintRectWIN especifica un conjunto de rectángulos que se van a copiar mediante SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- glAddSwapHintRectWIN (función) OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422400"
---
# <a name="gladdswaphintrectwin-function"></a><span data-ttu-id="6dbe9-104">glAddSwapHintRectWIN función)</span><span class="sxs-lookup"><span data-stu-id="6dbe9-104">glAddSwapHintRectWIN function</span></span>

<span data-ttu-id="6dbe9-105">La función de devolución de llamada **glAddSwapHintRectWIN** especifica un conjunto de rectángulos que se van a copiar mediante [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="6dbe9-105">The **glAddSwapHintRectWIN** callback function specifies a set of rectangles that are to be copied by [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span>

## <a name="syntax"></a><span data-ttu-id="6dbe9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6dbe9-106">Syntax</span></span>


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="6dbe9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6dbe9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dbe9-108">*x*</span><span class="sxs-lookup"><span data-stu-id="6dbe9-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="6dbe9-109">La coordenada *x*(en coordenadas de la ventana) de la esquina inferior izquierda del rectángulo de la región de sugerencia.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-109">The *x*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="6dbe9-110">*y*</span><span class="sxs-lookup"><span data-stu-id="6dbe9-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6dbe9-111">Coordenada *y*(en coordenadas de la ventana) de la esquina inferior izquierda del rectángulo de la región de sugerencia.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-111">The *y*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="6dbe9-112">*width*</span><span class="sxs-lookup"><span data-stu-id="6dbe9-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="6dbe9-113">Ancho del rectángulo de la región de la sugerencia.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-113">The width of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="6dbe9-114">*height*</span><span class="sxs-lookup"><span data-stu-id="6dbe9-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="6dbe9-115">Alto del rectángulo de la región de la sugerencia.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-115">The height of the hint region rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dbe9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6dbe9-116">Return value</span></span>

<span data-ttu-id="6dbe9-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dbe9-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6dbe9-118">Remarks</span></span>

<span data-ttu-id="6dbe9-119">La función **glAddSwapHintRectWIN** acelera la animación reduciendo la cantidad de repintado entre fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-119">The **glAddSwapHintRectWIN** function speeds up animation by reducing the amount of repainting between frames.</span></span> <span data-ttu-id="6dbe9-120">Con **glAddSwapHintRectWIN**, debe especificar un conjunto de áreas rectangulares que desea copiar al llamar a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="6dbe9-120">With **glAddSwapHintRectWIN**, you specify a set of rectangular areas that you want copied when you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="6dbe9-121">Cuando no se especifica ningún rectángulo con **glAddSwapHintRectWIN** antes de llamar a **SwapBuffers**, se intercambia todo el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-121">When you do not specify any rectangles with **glAddSwapHintRectWIN** before calling **SwapBuffers**, the entire framebuffer is swapped.</span></span> <span data-ttu-id="6dbe9-122">El uso de **glAddSwapHintRectWIN** para copiar solo las partes modificadas del búfer puede aumentar significativamente el rendimiento de **SwapBuffers**, especialmente cuando se implementa **SwapBuffers** en el software.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-122">Using **glAddSwapHintRectWIN** to copy only changed parts of the buffer can significantly increase the performance of **SwapBuffers**, especially when **SwapBuffers** is implemented in software.</span></span>

<span data-ttu-id="6dbe9-123">La función **glAddSwapHintRectWIN** agrega un rectángulo a la región de sugerencia.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-123">The **glAddSwapHintRectWIN** function adds a rectangle to the hint region.</span></span> <span data-ttu-id="6dbe9-124">Cuando \_ \_ se establece la marca de copia de intercambio de PFD de la estructura de formato de píxel de [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) , **SwapBuffers** usa esta región para recortar la copia del búfer de reserva en el búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-124">When the PFD\_SWAP\_COPY flag of the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel format structure is set, **SwapBuffers** uses this region to clip the copying of the back buffer to the front buffer.</span></span> <span data-ttu-id="6dbe9-125">No se especifica la \_ \_ copia de intercambio de PFD; está establecida por hardware compatible.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-125">You don't specify PFD\_SWAP\_COPY; it is set by capable hardware.</span></span> <span data-ttu-id="6dbe9-126">La región de sugerencia se borra después de cada llamada a **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-126">The hint region is cleared after each call to **SwapBuffers**.</span></span> <span data-ttu-id="6dbe9-127">Con algunas configuraciones de hardware, **SwapBuffers** puede omitir la región de sugerencia e intercambiar todo el búfer.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-127">With some hardware configurations, **SwapBuffers** can ignore the hint region and exchange the entire buffer.</span></span> <span data-ttu-id="6dbe9-128">**SwapBuffers** se implementa mediante el sistema, no por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-128">**SwapBuffers** is implemented by the system, not by the application.</span></span>

<span data-ttu-id="6dbe9-129">OpenGL mantiene una región de sugerencia independiente para cada ventana.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-129">OpenGL maintains a separate hint region for each window.</span></span> <span data-ttu-id="6dbe9-130">Cuando se llama a **glAddSwapHintRectWIN** en todos los contextos de representación asociados a una ventana, los rectángulos de la sugerencia se combinan en una sola región.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-130">When you call **glAddSwapHintRectWIN** on any rendering contexts associated with a window, the hint rectangles are combined into a single region.</span></span>

<span data-ttu-id="6dbe9-131">Llame a **glAddSwapHintRectWIN** con un rectángulo delimitador para cada objeto dibujado para un marco y para cada rectángulo desactivado para borrar los objetos de fotogramas anteriores.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-131">Call **glAddSwapHintRectWIN** with a bounding rectangle for each object drawn for a frame and for each rectangle cleared to erase previous frame objects.</span></span>

> [!Note]  
> <span data-ttu-id="6dbe9-132">La función **glAddSwapHintRectWIN** es una función de extensión que no forma parte de la biblioteca estándar de OpenGL, pero que forma parte de la extensión de sugerencia de intercambio de cont \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6dbe9-132">The **glAddSwapHintRectWIN** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_WIN\_swap\_hint extension.</span></span> <span data-ttu-id="6dbe9-133">Para comprobar si la implementación de OpenGL es compatible con **glAddSwapHintRectWIN**, llame a **glGetString**(extensiones de GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="6dbe9-133">To check whether your implementation of OpenGL supports **glAddSwapHintRectWIN**, call **glGetString**(GL\_EXTENSIONS).</span></span> <span data-ttu-id="6dbe9-134">Si devuelve la \_ sugerencia GL Win \_ swap \_ , se admite **glAddSwapHintRectWIN** .</span><span class="sxs-lookup"><span data-stu-id="6dbe9-134">If it returns GL\_WIN\_swap\_hint, **glAddSwapHintRectWIN** is supported.</span></span> <span data-ttu-id="6dbe9-135">Para obtener la dirección de una función de extensión, llame a **wglGetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="6dbe9-135">To obtain the address of an extension function, call **wglGetProcAddress**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6dbe9-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dbe9-136">Requirements</span></span>



| <span data-ttu-id="6dbe9-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dbe9-137">Requirement</span></span> | <span data-ttu-id="6dbe9-138">Value</span><span class="sxs-lookup"><span data-stu-id="6dbe9-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="6dbe9-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6dbe9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6dbe9-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6dbe9-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="6dbe9-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6dbe9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6dbe9-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6dbe9-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6dbe9-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6dbe9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dbe9-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dbe9-144"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dbe9-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="6dbe9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dbe9-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="6dbe9-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="6dbe9-147">**PIXELFORMATDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="6dbe9-147">**PIXELFORMATDESCRIPTOR**</span></span>](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[<span data-ttu-id="6dbe9-148">**SwapBuffers**</span><span class="sxs-lookup"><span data-stu-id="6dbe9-148">**SwapBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[<span data-ttu-id="6dbe9-149">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="6dbe9-149">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





