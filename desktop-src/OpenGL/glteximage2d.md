---
title: función glTexImage2D (GL. h)
description: La función glTexImage2D especifica una imagen de textura bidimensional.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- glTexImage2D (función) OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666089"
---
# <a name="glteximage2d-function"></a><span data-ttu-id="08dc9-104">glTexImage2D función)</span><span class="sxs-lookup"><span data-stu-id="08dc9-104">glTexImage2D function</span></span>

<span data-ttu-id="08dc9-105">La función **glTexImage2D** especifica una imagen de textura bidimensional.</span><span class="sxs-lookup"><span data-stu-id="08dc9-105">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="08dc9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08dc9-106">Syntax</span></span>


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="08dc9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08dc9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08dc9-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="08dc9-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-109">Textura de destino.</span><span class="sxs-lookup"><span data-stu-id="08dc9-109">The target texture.</span></span> <span data-ttu-id="08dc9-110">Debe ser la \_ textura de GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="08dc9-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="08dc9-111">*level*</span><span class="sxs-lookup"><span data-stu-id="08dc9-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-112">El número de nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="08dc9-112">The level-of-detail number.</span></span> <span data-ttu-id="08dc9-113">El nivel 0 es el nivel de la imagen base.</span><span class="sxs-lookup"><span data-stu-id="08dc9-113">Level 0 is the base image level.</span></span> <span data-ttu-id="08dc9-114">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="08dc9-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="08dc9-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="08dc9-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-116">El número de componentes de color de la textura.</span><span class="sxs-lookup"><span data-stu-id="08dc9-116">The number of color components in the texture.</span></span> <span data-ttu-id="08dc9-117">Debe ser 1, 2, 3 o 4, o una de las siguientes constantes simbólicas: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ luminancia, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ luminancia \_ Alpha, GL LUMINANCE4 ALPHA4, GL LUMINANCE6 ALPHA2, GL \_ \_ \_ \_ \_ LUMINANCE8 \_ ALPHA8, GL LUMINANCE12 \_ \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ Intensity, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ R3 \_ G3 \_ B2, GL \_ RGB, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL RGB16, cont. \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ RGBA2, GL RGBA4, GL RGB5, GL RGBA8, GL RGB10, GL RGBA12, GL RGBA16 o GL.</span><span class="sxs-lookup"><span data-stu-id="08dc9-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_R3\_G3\_B2, GL\_RGB, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="08dc9-118">*width*</span><span class="sxs-lookup"><span data-stu-id="08dc9-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-119">Ancho de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="08dc9-119">The width of the texture image.</span></span> <span data-ttu-id="08dc9-120">Debe ser 2 *n* + 2 (*borde*) para algún entero *n*.</span><span class="sxs-lookup"><span data-stu-id="08dc9-120">Must be 2 *n* + 2(*border*) for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="08dc9-121">*height*</span><span class="sxs-lookup"><span data-stu-id="08dc9-121">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-122">Alto de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="08dc9-122">The height of the texture image.</span></span> <span data-ttu-id="08dc9-123">Debe ser 2 *<sup>m</sup>* + 2 (*borde*) para algún entero *m*.</span><span class="sxs-lookup"><span data-stu-id="08dc9-123">Must be 2 *<sup>m</sup>* + 2(*border*) for some integer *m*.</span></span>

</dd> <dt>

<span data-ttu-id="08dc9-124">*PDA*</span><span class="sxs-lookup"><span data-stu-id="08dc9-124">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-125">Ancho del borde.</span><span class="sxs-lookup"><span data-stu-id="08dc9-125">The width of the border.</span></span> <span data-ttu-id="08dc9-126">Debe ser 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="08dc9-126">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="08dc9-127">*format*</span><span class="sxs-lookup"><span data-stu-id="08dc9-127">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-128">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="08dc9-128">The format of the pixel data.</span></span> <span data-ttu-id="08dc9-129">Puede suponer uno de los nueve valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="08dc9-129">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="08dc9-130">Value</span><span class="sxs-lookup"><span data-stu-id="08dc9-130">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="08dc9-131">Significado</span><span class="sxs-lookup"><span data-stu-id="08dc9-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="08dc9-132"><dt>**\_Índice de color de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-132"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="08dc9-133">Cada elemento es un valor único, un índice de color.</span><span class="sxs-lookup"><span data-stu-id="08dc9-133">Each element is a single value, a color index.</span></span> <span data-ttu-id="08dc9-134">Se convierte en un punto fijo (con un número sin especificar de 0 bits a la derecha del punto binario), desplazado a la izquierda o a la derecha en función del valor y el signo del turno del índice de contabilidad \_ \_ y se agrega al desplazamiento del índice de contabilidad \_ \_ (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="08dc9-134">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="08dc9-135">El índice resultante se convierte en un conjunto de componentes de color mediante el uso de la asignación de píxeles de GL \_ \_ \_ i \_ a \_ R, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ G, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ B y \_ la asignación de píxeles de GL \_ \_ \_ a \_ una tabla, y se ha fijado en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="08dc9-135">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="08dc9-136"><dt>**\_rojo GL**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-136"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="08dc9-137">Cada elemento es un componente rojo único.</span><span class="sxs-lookup"><span data-stu-id="08dc9-137">Each element is a single red component.</span></span> <span data-ttu-id="08dc9-138">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para verde y azul, y 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="08dc9-138">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="08dc9-139">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="08dc9-139">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="08dc9-140"><dt>**\_verde GL**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-140"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="08dc9-141">Cada elemento es un único componente verde.</span><span class="sxs-lookup"><span data-stu-id="08dc9-141">Each element is a single green component.</span></span> <span data-ttu-id="08dc9-142">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y azul, y 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="08dc9-142">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="08dc9-143">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="08dc9-143">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="08dc9-144"><dt>**\_azul GL**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-144"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="08dc9-145">Cada elemento es un único componente azul.</span><span class="sxs-lookup"><span data-stu-id="08dc9-145">Each element is a single blue component.</span></span> <span data-ttu-id="08dc9-146">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y verde, y 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="08dc9-146">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="08dc9-147">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="08dc9-147">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="08dc9-148"><dt>**libro \_ de contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-148"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="08dc9-149">Cada elemento es un componente rojo único.</span><span class="sxs-lookup"><span data-stu-id="08dc9-149">Each element is a single red component.</span></span> <span data-ttu-id="08dc9-150">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="08dc9-150">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="08dc9-151">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="08dc9-151">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="08dc9-152"><dt>**RGB de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-152"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="08dc9-153">Cada elemento es un triple RGB.</span><span class="sxs-lookup"><span data-stu-id="08dc9-153">Each element is an RGB triple.</span></span> <span data-ttu-id="08dc9-154">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="08dc9-154">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="08dc9-155">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="08dc9-155">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="08dc9-156"><dt>**el \_ RGBA de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-156"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="08dc9-157">Cada elemento es un elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="08dc9-157">Each element is a complete RGBA element.</span></span> <span data-ttu-id="08dc9-158">Se convierte en punto flotante.</span><span class="sxs-lookup"><span data-stu-id="08dc9-158">It is converted to floating point.</span></span> <span data-ttu-id="08dc9-159">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="08dc9-159">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="08dc9-160"><dt>**GL \_ BGR \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-160"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="08dc9-161">Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.</span><span class="sxs-lookup"><span data-stu-id="08dc9-161">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="08dc9-162">GL \_ BGR \_ ext proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="08dc9-162">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="08dc9-163">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="08dc9-163">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="08dc9-164"><dt>**\_ext BGRA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-164"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="08dc9-165">Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.</span><span class="sxs-lookup"><span data-stu-id="08dc9-165">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span> <span data-ttu-id="08dc9-166">GL \_ BGRA \_ ext proporciona un formato que coincide con el diseño de memoria de mapas de bits independientes del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="08dc9-166">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="08dc9-167">Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="08dc9-167">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="08dc9-168"><dt>**luminancia del libro de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-168"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="08dc9-169">Cada elemento es un valor de luminancia único.</span><span class="sxs-lookup"><span data-stu-id="08dc9-169">Each element is a single luminance value.</span></span> <span data-ttu-id="08dc9-170">Se convierte en punto flotante y, a continuación, se monta en un elemento RGBA replicando el valor de luminancia tres veces para rojo, verde y azul, y adjuntando 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="08dc9-170">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="08dc9-171">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="08dc9-171">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="08dc9-172"><dt>**alfa de luminancia de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-172"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="08dc9-173">Cada elemento es un par de luminancia/alfa.</span><span class="sxs-lookup"><span data-stu-id="08dc9-173">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="08dc9-174">Se convierte en punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="08dc9-174">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="08dc9-175">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="08dc9-175">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="08dc9-176">*type*</span><span class="sxs-lookup"><span data-stu-id="08dc9-176">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-177">El tipo de datos de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="08dc9-177">The data type of the pixel data.</span></span> <span data-ttu-id="08dc9-178">Se aceptan los siguientes valores simbólicos: \_ byte sin signo \_ de libro de contabilidad, \_ bytes de contabilidad, \_ mapa de bits de GL, GL \_ sin signo \_ corto, GL \_ corto, libro de contabilidad \_ sin signo de GL \_ , GL \_ int y contabilidad \_ flotante.</span><span class="sxs-lookup"><span data-stu-id="08dc9-178">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="08dc9-179">*píxeles*</span><span class="sxs-lookup"><span data-stu-id="08dc9-179">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc9-180">Puntero a los datos de la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="08dc9-180">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08dc9-181">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08dc9-181">Return value</span></span>

<span data-ttu-id="08dc9-182">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="08dc9-182">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="08dc9-183">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="08dc9-183">Error codes</span></span>

<span data-ttu-id="08dc9-184">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="08dc9-184">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="08dc9-185">Nombre</span><span class="sxs-lookup"><span data-stu-id="08dc9-185">Name</span></span>                                                                                                  | <span data-ttu-id="08dc9-186">Significado</span><span class="sxs-lookup"><span data-stu-id="08dc9-186">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08dc9-187"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="08dc9-188">el *destino* no era \_ 2D Texture \_ .</span><span class="sxs-lookup"><span data-stu-id="08dc9-188">*target* was not an GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="08dc9-189"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-189"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="08dc9-190">el *formato* no era una constante de *formato* aceptada.</span><span class="sxs-lookup"><span data-stu-id="08dc9-190">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="08dc9-191">Solo se aceptan constantes de formato que no sean el \_ componente de índice de estarcido \_ de GL y de profundidad de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="08dc9-191">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="08dc9-192">Vea la descripción del parámetro *Format* para obtener una lista de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="08dc9-192">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="08dc9-193"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="08dc9-194">el *tipo* no era una constante de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="08dc9-194">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="08dc9-195"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-195"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="08dc9-196">el *tipo* era un \_ mapa de bits de contabilidad y el *formato* no era un índice de color de GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="08dc9-196">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="08dc9-197"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="08dc9-198">el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* era el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="08dc9-198">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="08dc9-199"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="08dc9-200">*internalformat* no era 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="08dc9-200">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="08dc9-201"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="08dc9-202">el *ancho* o alto era menor que cero o mayor que 2 + \_ tamaño máximo de textura de GL \_ \_ , o no se pudo representar como 2 *n* + 2 (borde) para algún valor entero de *n*.</span><span class="sxs-lookup"><span data-stu-id="08dc9-202">*width* or height was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="08dc9-203"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-203"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="08dc9-204">el *borde* no era 0 ni 1.</span><span class="sxs-lookup"><span data-stu-id="08dc9-204">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="08dc9-205"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-205"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="08dc9-206">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="08dc9-206">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="08dc9-207">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08dc9-207">Remarks</span></span>

<span data-ttu-id="08dc9-208">La función **glTexImage2D** especifica una imagen de textura bidimensional.</span><span class="sxs-lookup"><span data-stu-id="08dc9-208">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span> <span data-ttu-id="08dc9-209">La texturización asigna una parte de una *imagen de textura* especificada en cada primitiva gráfica para la que está habilitada la texturización.</span><span class="sxs-lookup"><span data-stu-id="08dc9-209">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="08dc9-210">La texturización bidimensional está habilitada y deshabilitada mediante [**glEnable**](glenable.md) y **glDisable** con la textura de GL de argumento \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="08dc9-210">Two-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="08dc9-211">Las imágenes de textura se definen con **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="08dc9-211">Texture images are defined with **glTexImage2D**.</span></span> <span data-ttu-id="08dc9-212">Los argumentos describen los parámetros de la imagen de textura, como el alto, el ancho, el ancho del borde, el número de nivel de detalle (vea [**glTexParameter**](gltexparameter-functions.md)) y el número de componentes de color proporcionados.</span><span class="sxs-lookup"><span data-stu-id="08dc9-212">The arguments describe the parameters of the texture image, such as height, width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="08dc9-213">Los tres últimos argumentos describen el modo en que se representa la imagen en la memoria.</span><span class="sxs-lookup"><span data-stu-id="08dc9-213">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="08dc9-214">Estos argumentos son idénticos a los formatos de píxel usados para [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="08dc9-214">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="08dc9-215">Los datos se leen desde *píxeles* como una secuencia de bytes con signo o sin signo, breves o largos o valores de punto flotante de precisión sencilla, dependiendo del *tipo*.</span><span class="sxs-lookup"><span data-stu-id="08dc9-215">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="08dc9-216">Estos valores se agrupan en conjuntos de uno, dos, tres o cuatro valores, según el *formato*, para formar elementos.</span><span class="sxs-lookup"><span data-stu-id="08dc9-216">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="08dc9-217">Si el *tipo* es \_ un mapa de bits de contabilidad, los datos se consideran una cadena de bytes sin signo (y el *formato* debe ser índice de color de GL \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="08dc9-217">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="08dc9-218">Cada byte de datos se trata como elementos de 8 1 bits, con una ordenación de bits determinada por GL \_ unpack \_ LSB \_ primero (consulte [**glPixelStore**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="08dc9-218">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span> <span data-ttu-id="08dc9-219">Consulte [**glDrawPixels**](gldrawpixels.md) para obtener una descripción de los valores aceptables para el parámetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="08dc9-219">Please see [**glDrawPixels**](gldrawpixels.md) for a description of the acceptable values for the *type* parameter.</span></span>

<span data-ttu-id="08dc9-220">Una imagen de textura puede tener hasta cuatro componentes por elemento de textura, dependiendo de *los componentes*.</span><span class="sxs-lookup"><span data-stu-id="08dc9-220">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="08dc9-221">Una imagen de textura de un componente usa solo el componente rojo del color RGBA extraído de los *píxeles*.</span><span class="sxs-lookup"><span data-stu-id="08dc9-221">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="08dc9-222">Una imagen de dos componentes utiliza los valores R y A.</span><span class="sxs-lookup"><span data-stu-id="08dc9-222">A two-component image uses the R and A values.</span></span> <span data-ttu-id="08dc9-223">Una imagen de tres componentes utiliza los valores R, G y B.</span><span class="sxs-lookup"><span data-stu-id="08dc9-223">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="08dc9-224">Una imagen de cuatro componentes usa todos los componentes RGBA.</span><span class="sxs-lookup"><span data-stu-id="08dc9-224">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="08dc9-225">La texturización no tiene ningún efecto en el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="08dc9-225">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="08dc9-226">La imagen de textura se puede representar con los mismos formatos de datos que los píxeles de un comando **glDrawPixels** , excepto en que \_ no se puede usar el índice de estarcido de GL \_ y el componente de profundidad de libro de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="08dc9-226">The texture image can be represented by the same data formats as the pixels in a **glDrawPixels** command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="08dc9-227">Los modos [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="08dc9-227">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="08dc9-228">Una imagen de textura con alto o ancho cero indica la textura nula.</span><span class="sxs-lookup"><span data-stu-id="08dc9-228">A texture image with zero height or width indicates the null texture.</span></span> <span data-ttu-id="08dc9-229">Si se especifica la textura null para el nivel de detalle 0, es como si se hubiera deshabilitado la texturización.</span><span class="sxs-lookup"><span data-stu-id="08dc9-229">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="08dc9-230">Las siguientes funciones recuperan información relacionada con **glTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="08dc9-230">The following functions retrieve information related to **glTexImage2D**:</span></span>

[<span data-ttu-id="08dc9-231">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="08dc9-231">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="08dc9-232">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 2D</span><span class="sxs-lookup"><span data-stu-id="08dc9-232">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="08dc9-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08dc9-233">Requirements</span></span>



| <span data-ttu-id="08dc9-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="08dc9-234">Requirement</span></span> | <span data-ttu-id="08dc9-235">Value</span><span class="sxs-lookup"><span data-stu-id="08dc9-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08dc9-236">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08dc9-236">Minimum supported client</span></span><br/> | <span data-ttu-id="08dc9-237">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="08dc9-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="08dc9-238">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08dc9-238">Minimum supported server</span></span><br/> | <span data-ttu-id="08dc9-239">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08dc9-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08dc9-240">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08dc9-240">Header</span></span><br/>                   | <dl> <span data-ttu-id="08dc9-241"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-241"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="08dc9-242">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08dc9-242">Library</span></span><br/>                  | <dl> <span data-ttu-id="08dc9-243"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-243"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="08dc9-244">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08dc9-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08dc9-245"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08dc9-245"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08dc9-246">Vea también</span><span class="sxs-lookup"><span data-stu-id="08dc9-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08dc9-247">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="08dc9-247">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="08dc9-248">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="08dc9-248">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="08dc9-249">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="08dc9-249">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="08dc9-250">**glFog**</span><span class="sxs-lookup"><span data-stu-id="08dc9-250">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="08dc9-251">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="08dc9-251">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="08dc9-252">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="08dc9-252">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="08dc9-253">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="08dc9-253">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="08dc9-254">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="08dc9-254">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="08dc9-255">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="08dc9-255">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="08dc9-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="08dc9-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="08dc9-257">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="08dc9-257">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





