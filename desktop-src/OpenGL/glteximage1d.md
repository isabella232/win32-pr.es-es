---
title: función glTexImage1D (GL. h)
description: La función glTexImage1D especifica una imagen de textura de una dimensión.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- glTexImage1D (función) OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1865d19c54b9c59654f07162d2480aa5b29c47f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079241"
---
# <a name="glteximage1d-function"></a><span data-ttu-id="46d83-104">glTexImage1D función)</span><span class="sxs-lookup"><span data-stu-id="46d83-104">glTexImage1D function</span></span>

<span data-ttu-id="46d83-105">La función **glTexImage1D** especifica una imagen de textura de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="46d83-105">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d83-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46d83-106">Syntax</span></span>


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="46d83-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46d83-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d83-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="46d83-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="46d83-109">Textura de destino.</span><span class="sxs-lookup"><span data-stu-id="46d83-109">The target texture.</span></span> <span data-ttu-id="46d83-110">Debe ser la \_ textura de GL \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="46d83-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="46d83-111">*level*</span><span class="sxs-lookup"><span data-stu-id="46d83-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="46d83-112">El número de nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="46d83-112">The level-of-detail number.</span></span> <span data-ttu-id="46d83-113">El nivel 0 es el nivel de la imagen base.</span><span class="sxs-lookup"><span data-stu-id="46d83-113">Level 0 is the base image level.</span></span> <span data-ttu-id="46d83-114">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="46d83-114">Level *n* is the *n* Th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="46d83-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="46d83-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="46d83-116">Especifica el número de componentes de color de la textura.</span><span class="sxs-lookup"><span data-stu-id="46d83-116">Specifies the number of color components in the texture.</span></span> <span data-ttu-id="46d83-117">Debe ser 1, 2, 3 o 4, o una de las siguientes constantes simbólicas: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ luminancia, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ luminancia \_ Alpha, GL LUMINANCE4 ALPHA4, GL LUMINANCE6 ALPHA2, GL \_ \_ \_ \_ \_ LUMINANCE8 \_ ALPHA8, GL LUMINANCE12 \_ \_ ALPHA4, GL LUMINANCE12 ALPHA12, GL LUMINANCE16 ALPHA16, GL, intensidad del libro de contabilidad, GL INTENSITY4, GL INTENSITY8 \_ , GL \_ \_ \_ \_ \_ \_ \_ INTENSITY12, GL INTENSITY16, GL \_ \_ RGB, GL \_ R3 \_ G3 \_ B2, GL \_ RGB4, GL \_ RGB5, GL RGB8, \_ GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, cont RGBA2, GL RGBA4 \_ \_ , GL RGB5 \_ , GL RGBA8, GL \_ \_ \_ RGB10, GL \_ RGBA12 \_ a2, GL \_ RGBA16 o GL \_ .</span><span class="sxs-lookup"><span data-stu-id="46d83-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_RGB, GL\_R3\_G3\_B2, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="46d83-118">*width*</span><span class="sxs-lookup"><span data-stu-id="46d83-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="46d83-119">Ancho de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="46d83-119">The width of the texture image.</span></span> <span data-ttu-id="46d83-120">Debe ser 2 *n* + 2 ( *borde* ) para algún entero *n*.</span><span class="sxs-lookup"><span data-stu-id="46d83-120">Must be 2 *n* + 2( *border* ) for some integer *n*.</span></span> <span data-ttu-id="46d83-121">El alto de la imagen de textura es 1.</span><span class="sxs-lookup"><span data-stu-id="46d83-121">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="46d83-122">*PDA*</span><span class="sxs-lookup"><span data-stu-id="46d83-122">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="46d83-123">Ancho del borde.</span><span class="sxs-lookup"><span data-stu-id="46d83-123">The width of the border.</span></span> <span data-ttu-id="46d83-124">Debe ser 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="46d83-124">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="46d83-125">*format*</span><span class="sxs-lookup"><span data-stu-id="46d83-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="46d83-126">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="46d83-126">The format of the pixel data.</span></span> <span data-ttu-id="46d83-127">Puede suponer uno de los nueve valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="46d83-127">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="46d83-128">Value</span><span class="sxs-lookup"><span data-stu-id="46d83-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="46d83-129">Significado</span><span class="sxs-lookup"><span data-stu-id="46d83-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="46d83-130"><dt>**\_Índice de color de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="46d83-131">Cada elemento es un valor único, un índice de color.</span><span class="sxs-lookup"><span data-stu-id="46d83-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="46d83-132">Se convierte en un punto fijo (con un número no especificado de 0 bits a la derecha del punto binario), desplazado a la izquierda o a la derecha, según el valor y el signo del cambio de índice de contabilidad \_ \_ y se agrega al desplazamiento del índice de contabilidad \_ \_ (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="46d83-132">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="46d83-133">El índice resultante se convierte en un conjunto de componentes de color mediante el uso de la asignación de píxeles de GL \_ \_ \_ i \_ a \_ R, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ G, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ B y \_ la asignación de píxeles de GL \_ \_ \_ a \_ una tabla, y se ha fijado en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="46d83-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="46d83-134"><dt>**\_rojo GL**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="46d83-135">Cada elemento es un componente rojo único.</span><span class="sxs-lookup"><span data-stu-id="46d83-135">Each element is a single red component.</span></span> <span data-ttu-id="46d83-136">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para verde y azul, y 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="46d83-136">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="46d83-137">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="46d83-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="46d83-138"><dt>**\_verde GL**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="46d83-139">Cada elemento es un único componente verde.</span><span class="sxs-lookup"><span data-stu-id="46d83-139">Each element is a single green component.</span></span> <span data-ttu-id="46d83-140">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y azul, y 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="46d83-140">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="46d83-141">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="46d83-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="46d83-142"><dt>**\_azul GL**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="46d83-143">Cada elemento es un único componente azul.</span><span class="sxs-lookup"><span data-stu-id="46d83-143">Each element is a single blue component.</span></span> <span data-ttu-id="46d83-144">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y verde, y 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="46d83-144">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="46d83-145">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="46d83-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="46d83-146"><dt>**libro \_ de contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="46d83-147">Cada elemento es un componente rojo único.</span><span class="sxs-lookup"><span data-stu-id="46d83-147">Each element is a single red component.</span></span> <span data-ttu-id="46d83-148">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="46d83-148">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="46d83-149">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="46d83-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="46d83-150"><dt>**RGB de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="46d83-151">Cada elemento es un triple RGB.</span><span class="sxs-lookup"><span data-stu-id="46d83-151">Each element is an RGB triple.</span></span> <span data-ttu-id="46d83-152">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="46d83-152">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="46d83-153">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="46d83-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="46d83-154"><dt>**el \_ RGBA de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="46d83-155">Cada elemento es un elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="46d83-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="46d83-156">Se convierte en punto flotante.</span><span class="sxs-lookup"><span data-stu-id="46d83-156">It is converted to floating point.</span></span> <span data-ttu-id="46d83-157">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="46d83-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="46d83-158"><dt>**GL \_ BGR \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-158"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="46d83-159">Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.</span><span class="sxs-lookup"><span data-stu-id="46d83-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="46d83-160">GL \_ BGR \_ ext proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="46d83-160">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="46d83-161">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="46d83-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="46d83-162"><dt>**\_ext BGRA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-162"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="46d83-163">Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.</span><span class="sxs-lookup"><span data-stu-id="46d83-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="46d83-164">GL \_ BGRA \_ ext proporciona un formato que coincide con el diseño de memoria de mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="46d83-164">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="46d83-165">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="46d83-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="46d83-166"><dt>**luminancia del libro de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-166"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="46d83-167">Cada elemento es un valor de luminancia único.</span><span class="sxs-lookup"><span data-stu-id="46d83-167">Each element is a single luminance value.</span></span> <span data-ttu-id="46d83-168">Se convierte en punto flotante y, a continuación, se monta en un elemento RGBA replicando el valor de luminancia tres veces para rojo, verde y azul, y adjuntando 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="46d83-168">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="46d83-169">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="46d83-169">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="46d83-170"><dt>**alfa de luminancia de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-170"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="46d83-171">Cada elemento es un par de luminancia/alfa.</span><span class="sxs-lookup"><span data-stu-id="46d83-171">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="46d83-172">Se convierte en punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="46d83-172">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="46d83-173">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="46d83-173">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="46d83-174">*type*</span><span class="sxs-lookup"><span data-stu-id="46d83-174">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="46d83-175">El tipo de datos de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="46d83-175">The data type of the pixel data.</span></span> <span data-ttu-id="46d83-176">Se aceptan los siguientes valores simbólicos: \_ byte sin signo \_ de libro de contabilidad, \_ bytes de contabilidad, \_ mapa de bits de GL, GL \_ sin signo \_ corto, GL \_ corto, libro de contabilidad \_ sin signo de GL \_ , GL \_ int y contabilidad \_ flotante.</span><span class="sxs-lookup"><span data-stu-id="46d83-176">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="46d83-177">*píxeles*</span><span class="sxs-lookup"><span data-stu-id="46d83-177">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="46d83-178">Puntero a los datos de la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="46d83-178">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d83-179">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46d83-179">Return value</span></span>

<span data-ttu-id="46d83-180">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="46d83-180">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="46d83-181">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="46d83-181">Error codes</span></span>

<span data-ttu-id="46d83-182">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="46d83-182">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="46d83-183">Nombre</span><span class="sxs-lookup"><span data-stu-id="46d83-183">Name</span></span>                                                                                                  | <span data-ttu-id="46d83-184">Significado</span><span class="sxs-lookup"><span data-stu-id="46d83-184">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46d83-185"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-185"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="46d83-186">el *destino* no era una \_ textura GL.</span><span class="sxs-lookup"><span data-stu-id="46d83-186">*target* was not an GL\_TEXTURE.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="46d83-187"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="46d83-188">el *formato* no era una constante de *formato* aceptada.</span><span class="sxs-lookup"><span data-stu-id="46d83-188">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="46d83-189">Solo se aceptan constantes de formato que no sean el \_ componente de índice de estarcido \_ de GL y de profundidad de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="46d83-189">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="46d83-190">Vea la descripción del parámetro *Format* para obtener una lista de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="46d83-190">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="46d83-191"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-191"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="46d83-192">el *tipo* no era una constante de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="46d83-192">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="46d83-193"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="46d83-194">el *tipo* era un \_ mapa de bits de contabilidad y el *formato* no era un índice de color de GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="46d83-194">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="46d83-195"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="46d83-196">el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* era el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="46d83-196">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="46d83-197"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="46d83-198">*internalformat* no era 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="46d83-198">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="46d83-199"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="46d83-200">el *ancho* era menor que cero o mayor que 2 + \_ tamaño máximo de textura de GL \_ \_ , o no se pudo representar como 2 *n* + 2 (borde) para algún valor entero de *n*.</span><span class="sxs-lookup"><span data-stu-id="46d83-200">*width* was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="46d83-201"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="46d83-202">el *borde* no era 0 ni 1.</span><span class="sxs-lookup"><span data-stu-id="46d83-202">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="46d83-203"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-203"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="46d83-204">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="46d83-204">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="46d83-205">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46d83-205">Remarks</span></span>

<span data-ttu-id="46d83-206">La función **glTexImage1D** especifica una imagen de textura de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="46d83-206">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span> <span data-ttu-id="46d83-207">La texturización asigna una parte de una *imagen de textura* especificada en cada primitiva gráfica para la que está habilitada la texturización.</span><span class="sxs-lookup"><span data-stu-id="46d83-207">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="46d83-208">La texturización de una dimensión está habilitada y deshabilitada mediante [**glEnable**](glenable.md) y **glDisable** con el argumento GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="46d83-208">One-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_1D.</span></span>

<span data-ttu-id="46d83-209">Las imágenes de textura se definen con **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="46d83-209">Texture images are defined with **glTexImage1D**.</span></span> <span data-ttu-id="46d83-210">Los argumentos describen los parámetros de la imagen de textura, como el ancho, el ancho del borde, el número de nivel de detalle (vea [**glTexParameter**](gltexparameter-functions.md)) y el número de componentes de color proporcionados.</span><span class="sxs-lookup"><span data-stu-id="46d83-210">The arguments describe the parameters of the texture image, such as width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="46d83-211">Los tres últimos argumentos describen el modo en que se representa la imagen en la memoria.</span><span class="sxs-lookup"><span data-stu-id="46d83-211">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="46d83-212">Estos argumentos son idénticos a los formatos de píxel usados para [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="46d83-212">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="46d83-213">Los datos se leen desde *píxeles* como una secuencia de bytes con signo o sin signo, breves o largos o valores de punto flotante de precisión sencilla, dependiendo del *tipo*.</span><span class="sxs-lookup"><span data-stu-id="46d83-213">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="46d83-214">Estos valores se agrupan en conjuntos de uno, dos, tres o cuatro valores, según el *formato*, para formar elementos.</span><span class="sxs-lookup"><span data-stu-id="46d83-214">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="46d83-215">Si el *tipo* es \_ un mapa de bits de contabilidad, los datos se consideran una cadena de bytes sin signo (y el *formato* debe ser índice de color de GL \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="46d83-215">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="46d83-216">Cada byte de datos se trata como elementos de 8 1 bits, con una ordenación de bits determinada por GL \_ unpack \_ LSB \_ primero (consulte [**glPixelStore**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="46d83-216">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span>

<span data-ttu-id="46d83-217">Una imagen de textura puede tener hasta cuatro componentes por elemento de textura, dependiendo de *los componentes*.</span><span class="sxs-lookup"><span data-stu-id="46d83-217">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="46d83-218">Una imagen de textura de un componente usa solo el componente rojo del color RGBA extraído de los *píxeles*.</span><span class="sxs-lookup"><span data-stu-id="46d83-218">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="46d83-219">Una imagen de dos componentes utiliza los valores R y A.</span><span class="sxs-lookup"><span data-stu-id="46d83-219">A two-component image uses the R and A values.</span></span> <span data-ttu-id="46d83-220">Una imagen de tres componentes utiliza los valores R, G y B.</span><span class="sxs-lookup"><span data-stu-id="46d83-220">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="46d83-221">Una imagen de cuatro componentes usa todos los componentes RGBA.</span><span class="sxs-lookup"><span data-stu-id="46d83-221">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="46d83-222">La texturización no tiene ningún efecto en el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="46d83-222">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="46d83-223">La imagen de textura se puede representar con los mismos formatos de datos que los píxeles de un comando [**glDrawPixels**](gldrawpixels.md) , excepto en que \_ no se puede usar el índice de estarcido de GL \_ y el componente de profundidad de libro de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="46d83-223">The texture image can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="46d83-224">Los modos [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="46d83-224">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="46d83-225">Una imagen de textura con ancho cero indica la textura nula.</span><span class="sxs-lookup"><span data-stu-id="46d83-225">A texture image with zero width indicates the null texture.</span></span> <span data-ttu-id="46d83-226">Si se especifica la textura null para el nivel de detalle 0, es como si se hubiera deshabilitado la texturización.</span><span class="sxs-lookup"><span data-stu-id="46d83-226">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="46d83-227">Las siguientes funciones recuperan información relacionada con **glTexImageID**:</span><span class="sxs-lookup"><span data-stu-id="46d83-227">The following functions retrieve information related to **glTexImageID**:</span></span>

[<span data-ttu-id="46d83-228">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="46d83-228">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="46d83-229">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="46d83-229">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="46d83-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46d83-230">Requirements</span></span>



| <span data-ttu-id="46d83-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="46d83-231">Requirement</span></span> | <span data-ttu-id="46d83-232">Value</span><span class="sxs-lookup"><span data-stu-id="46d83-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46d83-233">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46d83-233">Minimum supported client</span></span><br/> | <span data-ttu-id="46d83-234">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="46d83-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="46d83-235">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46d83-235">Minimum supported server</span></span><br/> | <span data-ttu-id="46d83-236">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46d83-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46d83-237">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46d83-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d83-238"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-238"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="46d83-239">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46d83-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="46d83-240"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-240"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="46d83-241">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46d83-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46d83-242"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46d83-242"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d83-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="46d83-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d83-244">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="46d83-244">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="46d83-245">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="46d83-245">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="46d83-246">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="46d83-246">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="46d83-247">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="46d83-247">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="46d83-248">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="46d83-248">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="46d83-249">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="46d83-249">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="46d83-250">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="46d83-250">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="46d83-251">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="46d83-251">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="46d83-252">**glFog**</span><span class="sxs-lookup"><span data-stu-id="46d83-252">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="46d83-253">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="46d83-253">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="46d83-254">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="46d83-254">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="46d83-255">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="46d83-255">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="46d83-256">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="46d83-256">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="46d83-257">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="46d83-257">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="46d83-258">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="46d83-258">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="46d83-259">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="46d83-259">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="46d83-260">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="46d83-260">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="46d83-261">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="46d83-261">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="46d83-262">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="46d83-262">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





