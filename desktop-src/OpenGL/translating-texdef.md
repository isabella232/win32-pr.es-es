---
title: Traducción de texdef
description: El ejemplo de código siguiente es una definición de textura de la contabilidad de IRIS
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Migración de la contabilidad de IRIS, textura
- portabilidad de IRIS GL, textura
- trasladar a OpenGL desde IRIS GL, textura
- Exportación de OpenGL desde IRIS GL, textura
- textura
- Migración de la contabilidad de IRIS, texdef
- portabilidad de IRIS GL, texdef
- migración a OpenGL desde IRIS GL, texdef
- Exportación de OpenGL desde IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903807"
---
# <a name="translating-texdef"></a><span data-ttu-id="88805-113">Traducción de texdef</span><span class="sxs-lookup"><span data-stu-id="88805-113">Translating texdef</span></span>

<span data-ttu-id="88805-114">El siguiente ejemplo de código es una definición de textura de GL de IRIS:</span><span class="sxs-lookup"><span data-stu-id="88805-114">The following code example is an IRIS GL texture definition:</span></span>


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



<span data-ttu-id="88805-115">En el ejemplo anterior, **texdef** especifica el \_ filtro de punto TX como el filtro de ampliación y reducción, y TX \_ REPEAT como mecanismo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="88805-115">In the preceding example, **texdef** specifies the TX\_POINT filter as both the magnification and the minimizing filter, and TX\_REPEAT as the wrapping mechanism.</span></span> <span data-ttu-id="88805-116">También especifica la imagen de textura: **granito \_ Texture**.</span><span class="sxs-lookup"><span data-stu-id="88805-116">It also specifies the texture image: **granite\_texture**.</span></span>

<span data-ttu-id="88805-117">En OpenGL, [**glTexImage**](glteximage1d.md) especifica la imagen y [glTexParameter](gltexparameter-functions.md) establece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="88805-117">In OpenGL, [**glTexImage**](glteximage1d.md) specifies the image and [glTexParameter](gltexparameter-functions.md) sets the property.</span></span> <span data-ttu-id="88805-118">Para traducir las definiciones de textura de la contabilidad de IRIS, reemplace la función **textdef** por **glTexImage** y una o varias llamadas a **glTexParameter**.</span><span class="sxs-lookup"><span data-stu-id="88805-118">To translate IRIS GL texture definitions, replace the **textdef** function with **glTexImage** and one or more calls to **glTexParameter**.</span></span>

<span data-ttu-id="88805-119">El código de GL del IRIS anterior tiene este aspecto cuando se traduce a OpenGL:</span><span class="sxs-lookup"><span data-stu-id="88805-119">The preceding IRIS GL code looks like this when translated to OpenGL:</span></span>


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



<span data-ttu-id="88805-120">En la tabla siguiente se enumeran los parámetros de textura de la contabilidad de IRIS y sus parámetros de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="88805-120">The following table lists the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="88805-121">Parámetro de textura de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="88805-121">IRIS GL texture parameter</span></span> | <span data-ttu-id="88805-122">Parámetro de textura OpenGL</span><span class="sxs-lookup"><span data-stu-id="88805-122">OpenGL texture parameter</span></span>                                  |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="88805-123">TX \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="88805-123">TX\_MINFILTER</span></span>             | <span data-ttu-id="88805-124">\_ \_ filtro mínimo de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="88805-124">GL\_TEXTURE\_MIN\_FILTER</span></span>                                  |
| <span data-ttu-id="88805-125">TX \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="88805-125">TX\_MAGFILTER</span></span>             | <span data-ttu-id="88805-126">\_filtro de textura de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="88805-126">GL\_TEXTURE\_MAG\_FILTER</span></span>                                  |
| <span data-ttu-id="88805-127">\_encapsulado de TX \_ , encapsulado de TX \_</span><span class="sxs-lookup"><span data-stu-id="88805-127">TX\_WRAP, TX\_WRAP\_S</span></span>     | <span data-ttu-id="88805-128">\_ajuste de textura de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="88805-128">GL\_TEXTURE\_WRAP\_S</span></span>                                      |
| <span data-ttu-id="88805-129">\_encapsulado TX, \_ encapsulado de TX \_ T</span><span class="sxs-lookup"><span data-stu-id="88805-129">TX\_WRAP, TX\_WRAP\_T</span></span>     | <span data-ttu-id="88805-130">\_color de \_ \_ borde de textura de TGL de ajuste \_ de \_ textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="88805-130">GL\_TEXTURE\_WRAP\_TGL\_TEXTURE\_BORDER\_COLOR</span></span><br/> |



 

<span data-ttu-id="88805-131">En la tabla siguiente se enumeran los posibles valores de los parámetros de textura GL de IRIS y sus parámetros de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="88805-131">The following table lists the possible values of the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="88805-132">Parámetro de textura de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="88805-132">IRIS GL texture parameter</span></span> | <span data-ttu-id="88805-133">Parámetro de textura OpenGL</span><span class="sxs-lookup"><span data-stu-id="88805-133">OpenGL texture parameter</span></span>     |
|---------------------------|------------------------------|
| <span data-ttu-id="88805-134">punto de transmisión \_</span><span class="sxs-lookup"><span data-stu-id="88805-134">TX\_POINT</span></span>                 | <span data-ttu-id="88805-135">libro de contabilidad \_ más próximo</span><span class="sxs-lookup"><span data-stu-id="88805-135">GL\_NEAREST</span></span>                  |
| <span data-ttu-id="88805-136">TX \_ BIlineal</span><span class="sxs-lookup"><span data-stu-id="88805-136">TX\_BILINEAR</span></span>              | <span data-ttu-id="88805-137">CONTABILIDAD \_ lineal</span><span class="sxs-lookup"><span data-stu-id="88805-137">GL\_LINEAR</span></span>                   |
| <span data-ttu-id="88805-138">\_punto de MIPMAP de TX \_</span><span class="sxs-lookup"><span data-stu-id="88805-138">TX\_MIPMAP\_POINT</span></span>         | <span data-ttu-id="88805-139">\_MIP más cercano de GL \_ \_ más cercano</span><span class="sxs-lookup"><span data-stu-id="88805-139">GL\_NEAREST\_MIPMAP\_NEAREST</span></span> |
| <span data-ttu-id="88805-140">fotoline MIP de TX \_ \_</span><span class="sxs-lookup"><span data-stu-id="88805-140">TX\_MIPMAP\_BILINEAR</span></span>      | <span data-ttu-id="88805-141">\_MIP lineal de GL \_ \_ más cercano</span><span class="sxs-lookup"><span data-stu-id="88805-141">GL\_LINEAR\_MIPMAP\_NEAREST</span></span>  |
| <span data-ttu-id="88805-142">\_MIP \_ lineal de TX</span><span class="sxs-lookup"><span data-stu-id="88805-142">TX\_MIPMAP\_LINEAR</span></span>        | <span data-ttu-id="88805-143">el \_ \_ MIP \_ lineal más cercano de contabilidad</span><span class="sxs-lookup"><span data-stu-id="88805-143">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>  |
| <span data-ttu-id="88805-144">TX \_ TRIlineal</span><span class="sxs-lookup"><span data-stu-id="88805-144">TX\_TRILINEAR</span></span>             | <span data-ttu-id="88805-145">MIP lineal de contabilidad general \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="88805-145">GL\_LINEAR\_MIPMAP\_LINEAR</span></span>   |



 

 

 





