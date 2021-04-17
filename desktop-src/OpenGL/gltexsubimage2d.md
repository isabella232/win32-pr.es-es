---
title: función glTexSubImage2D (GL. h)
description: La función glTexSubImage2D especifica una parte de una imagen de textura de una dimensión existente. No se puede definir una textura nueva con glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- glTexSubImage2D (función) OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a0a59ae9e6724386cb2f7891a14e4bf9d4c1a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665916"
---
# <a name="gltexsubimage2d-function"></a><span data-ttu-id="555ac-105">glTexSubImage2D función)</span><span class="sxs-lookup"><span data-stu-id="555ac-105">glTexSubImage2D function</span></span>

<span data-ttu-id="555ac-106">La función **glTexSubImage2D** especifica una parte de una imagen de textura de una dimensión existente.</span><span class="sxs-lookup"><span data-stu-id="555ac-106">The **glTexSubImage2D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="555ac-107">No se puede definir una textura nueva con **glTexSubImage2D**.</span><span class="sxs-lookup"><span data-stu-id="555ac-107">You cannot define a new texture with **glTexSubImage2D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="555ac-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="555ac-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="555ac-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="555ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="555ac-110">*Destino*</span><span class="sxs-lookup"><span data-stu-id="555ac-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-111">Textura de destino.</span><span class="sxs-lookup"><span data-stu-id="555ac-111">The target texture.</span></span> <span data-ttu-id="555ac-112">Debe ser la \_ textura de GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="555ac-112">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="555ac-113">*level*</span><span class="sxs-lookup"><span data-stu-id="555ac-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-114">El número de nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="555ac-114">The level-of-detail number.</span></span> <span data-ttu-id="555ac-115">El nivel 0 es la imagen base.</span><span class="sxs-lookup"><span data-stu-id="555ac-115">Level 0 is the base image.</span></span> <span data-ttu-id="555ac-116">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="555ac-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="555ac-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="555ac-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-118">Desplazamiento textura en la dirección *x* dentro de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="555ac-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="555ac-119">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="555ac-119">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-120">Desplazamiento textura en la dirección *y* dentro de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="555ac-120">A texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="555ac-121">*width*</span><span class="sxs-lookup"><span data-stu-id="555ac-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-122">Ancho de la subimagen de textura.</span><span class="sxs-lookup"><span data-stu-id="555ac-122">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="555ac-123">*height*</span><span class="sxs-lookup"><span data-stu-id="555ac-123">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-124">Alto de la subimagen de textura.</span><span class="sxs-lookup"><span data-stu-id="555ac-124">The height of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="555ac-125">*format*</span><span class="sxs-lookup"><span data-stu-id="555ac-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-126">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="555ac-126">The format of the pixel data.</span></span> <span data-ttu-id="555ac-127">Puede suponer uno de los siguientes valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="555ac-127">It can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="555ac-128">Value</span><span class="sxs-lookup"><span data-stu-id="555ac-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="555ac-129">Significado</span><span class="sxs-lookup"><span data-stu-id="555ac-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="555ac-130"><dt>**\_Índice de color de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="555ac-131">Cada elemento es un valor único, un índice de color.</span><span class="sxs-lookup"><span data-stu-id="555ac-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="555ac-132">Se convierte en un formato de punto fijo (con un número no especificado de 0 bits a la derecha del punto binario), desplazado a la izquierda o a la derecha, según el valor y el signo del turno del índice de contabilidad \_ \_ y se agrega al desplazamiento del índice de GL \_ \_ (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="555ac-132">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="555ac-133">El índice resultante se convierte en un conjunto de componentes de color mediante el uso de la asignación de píxeles de GL \_ \_ \_ i \_ a \_ R, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ G, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ B y \_ la asignación de píxeles de GL \_ \_ \_ a \_ una tabla, y se ha fijado en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="555ac-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="555ac-134"><dt>**\_rojo GL**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="555ac-135">Cada elemento es un componente rojo único.</span><span class="sxs-lookup"><span data-stu-id="555ac-135">Each element is a single red component.</span></span> <span data-ttu-id="555ac-136">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para verde y azul, y 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="555ac-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="555ac-137">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="555ac-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="555ac-138"><dt>**\_verde GL**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="555ac-139">Cada elemento es un único componente verde.</span><span class="sxs-lookup"><span data-stu-id="555ac-139">Each element is a single green component.</span></span> <span data-ttu-id="555ac-140">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y azul, y 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="555ac-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="555ac-141">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="555ac-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="555ac-142"><dt>**\_azul GL**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="555ac-143">Cada elemento es un único componente azul.</span><span class="sxs-lookup"><span data-stu-id="555ac-143">Each element is a single blue component.</span></span> <span data-ttu-id="555ac-144">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y verde, y 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="555ac-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="555ac-145">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="555ac-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="555ac-146"><dt>**libro \_ de contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="555ac-147">Cada elemento es un único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="555ac-147">Each element is a single alpha component.</span></span> <span data-ttu-id="555ac-148">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="555ac-148">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="555ac-149">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="555ac-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="555ac-150"><dt>**RGB de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="555ac-151">Cada elemento es un triple RGB.</span><span class="sxs-lookup"><span data-stu-id="555ac-151">Each element is an RGB triple.</span></span> <span data-ttu-id="555ac-152">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="555ac-152">It is converted to floating point format and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="555ac-153">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="555ac-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="555ac-154"><dt>**el \_ RGBA de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="555ac-155">Cada elemento es un elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="555ac-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="555ac-156">Se convierte en punto flotante.</span><span class="sxs-lookup"><span data-stu-id="555ac-156">It is converted to floating point.</span></span> <span data-ttu-id="555ac-157">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="555ac-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="555ac-158"><dt>**luminancia del libro de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-158"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="555ac-159">Cada elemento es un valor de luminancia único.</span><span class="sxs-lookup"><span data-stu-id="555ac-159">Each element is a single luminance value.</span></span> <span data-ttu-id="555ac-160">Se convierte al formato de punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul, y la Asociación de 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="555ac-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="555ac-161">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="555ac-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="555ac-162"><dt>**alfa de luminancia de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-162"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="555ac-163">Cada elemento es un par de luminancia/alfa.</span><span class="sxs-lookup"><span data-stu-id="555ac-163">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="555ac-164">Se convierte al formato de punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="555ac-164">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="555ac-165">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="555ac-165">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="555ac-166">*type*</span><span class="sxs-lookup"><span data-stu-id="555ac-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-167">El tipo de datos de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="555ac-167">The data type of the pixel data.</span></span> <span data-ttu-id="555ac-168">Se aceptan los siguientes valores simbólicos: \_ byte sin signo \_ de libro de contabilidad, \_ bytes de contabilidad, \_ mapa de bits de GL, GL \_ sin signo \_ corto, GL \_ corto, libro de contabilidad \_ sin signo de GL \_ , GL \_ int y contabilidad \_ flotante.</span><span class="sxs-lookup"><span data-stu-id="555ac-168">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="555ac-169">*píxeles*</span><span class="sxs-lookup"><span data-stu-id="555ac-169">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="555ac-170">Puntero a los datos de la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="555ac-170">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="555ac-171">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="555ac-171">Return value</span></span>

<span data-ttu-id="555ac-172">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="555ac-172">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="555ac-173">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="555ac-173">Error codes</span></span>

<span data-ttu-id="555ac-174">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="555ac-174">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="555ac-175">Nombre</span><span class="sxs-lookup"><span data-stu-id="555ac-175">Name</span></span>                                                                                                  | <span data-ttu-id="555ac-176">Significado</span><span class="sxs-lookup"><span data-stu-id="555ac-176">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="555ac-177"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="555ac-178">el *destino* no era \_ \_ 2D Texture 2D.</span><span class="sxs-lookup"><span data-stu-id="555ac-178">*target* was not GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="555ac-179"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="555ac-180">el *formato* no era una constante aceptada.</span><span class="sxs-lookup"><span data-stu-id="555ac-180">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="555ac-181"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-181"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="555ac-182">el *tipo* no era una constante aceptada.</span><span class="sxs-lookup"><span data-stu-id="555ac-182">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="555ac-183"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-183"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="555ac-184">el *tipo* era un \_ mapa de bits de contabilidad y el *formato* no era un índice de color de GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="555ac-184">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="555ac-185"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-185"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="555ac-186">el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* era el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="555ac-186">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="555ac-187"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-187"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="555ac-188">*xoffset* era menor que-*b*; o el ancho de *xoffset*  +   era mayor que *w*  -  *b*; o *YOFFSET* era menor que-*b*; o el alto de *YOFFSET*  +   era mayor que *h*  -  *b*, donde *w* es el ancho de la textura GL \_ \_ , *h* es el \_ alto de la textura GL \_ y *b* es el ancho del borde de la textura de contabilidad \_ \_ de la imagen de textura que se está modificando.</span><span class="sxs-lookup"><span data-stu-id="555ac-188">*xoffset* was less than -*b*; or *xoffset* + *width* was greater than *w* - *b*; or *yoffset* was less than -*b*; or *yoffset* + *height* was greater than *h* - *b*, where *w* is the GL\_TEXTURE\_WIDTH, *h* is the GL\_TEXTURE\_HEIGHT, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span> <br/> <span data-ttu-id="555ac-189">Tenga en cuenta que *w* y *h* incluyen dos veces el ancho del borde.</span><span class="sxs-lookup"><span data-stu-id="555ac-189">Note that *w* and *h* include twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="555ac-190"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-190"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="555ac-191">el *ancho* era menor que *b*, donde *b* es el ancho del borde de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="555ac-191">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="555ac-192"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-192"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="555ac-193">*Border* no era cero o 1.</span><span class="sxs-lookup"><span data-stu-id="555ac-193">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="555ac-194"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-194"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="555ac-195">Una operación **glTexImage2D** anterior no definió la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="555ac-195">The texture array was not defined by a previous **glTexImage2D** operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="555ac-196"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-196"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="555ac-197">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="555ac-197">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="555ac-198">Observaciones</span><span class="sxs-lookup"><span data-stu-id="555ac-198">Remarks</span></span>

<span data-ttu-id="555ac-199">La texturización bidimensional para un primitivo se habilita mediante [**glEnable**](glenable.md) y **glDisable** con el argumento GL \_ Texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="555ac-199">Two-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_2D.</span></span> <span data-ttu-id="555ac-200">Durante la texturización, parte de una imagen de textura especificada se asigna a cada primitiva habilitada.</span><span class="sxs-lookup"><span data-stu-id="555ac-200">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="555ac-201">La función **glTexSubImage2D** se usa para especificar una subimagen contigua de una imagen de textura bidimensional existente para la texturización.</span><span class="sxs-lookup"><span data-stu-id="555ac-201">You use the **glTexSubImage2D** function to specify a contiguous sub-image of an existing two-dimensional texture image for texturing.</span></span>

<span data-ttu-id="555ac-202">Los textura a los que se hace referencia en *píxeles* reemplazan una región de la matriz de textura existente por índices *x* de *xoffset* y *xoffset* + (*ancho* 1) índices inclusivos *e y de* *YOFFSET* y *YOFFSET* + (*alto* 1) inclusive.</span><span class="sxs-lookup"><span data-stu-id="555ac-202">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive and *y* indexes of *yoffset* and *yoffset* + (*height* 1) inclusive.</span></span> <span data-ttu-id="555ac-203">Esta región no puede incluir ningún textura fuera del intervalo de la matriz de textura originalmente especificada.</span><span class="sxs-lookup"><span data-stu-id="555ac-203">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="555ac-204">Especificar una subimagen con un *ancho* de cero no tiene ningún efecto y no genera ningún error.</span><span class="sxs-lookup"><span data-stu-id="555ac-204">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="555ac-205">La texturización no tiene ningún efecto en el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="555ac-205">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="555ac-206">En general, las imágenes de textura se pueden representar con los mismos formatos de datos que los píxeles de un comando [**glDrawPixels**](gldrawpixels.md) , excepto en que \_ no se puede usar el índice de estarcido de GL \_ y el componente de profundidad de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="555ac-206">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="555ac-207">Los modos [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="555ac-207">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="555ac-208">Las siguientes funciones recuperan información relacionada con **glTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="555ac-208">The following functions retrieve information related to **glTexSubImage2D**:</span></span>

[<span data-ttu-id="555ac-209">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="555ac-209">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="555ac-210">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 2D</span><span class="sxs-lookup"><span data-stu-id="555ac-210">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="555ac-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="555ac-211">Requirements</span></span>



| <span data-ttu-id="555ac-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="555ac-212">Requirement</span></span> | <span data-ttu-id="555ac-213">Value</span><span class="sxs-lookup"><span data-stu-id="555ac-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="555ac-214">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="555ac-214">Minimum supported client</span></span><br/> | <span data-ttu-id="555ac-215">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="555ac-215">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="555ac-216">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="555ac-216">Minimum supported server</span></span><br/> | <span data-ttu-id="555ac-217">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="555ac-217">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="555ac-218">Encabezado</span><span class="sxs-lookup"><span data-stu-id="555ac-218">Header</span></span><br/>                   | <dl> <span data-ttu-id="555ac-219"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-219"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="555ac-220">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="555ac-220">Library</span></span><br/>                  | <dl> <span data-ttu-id="555ac-221"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-221"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="555ac-222">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="555ac-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="555ac-223"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="555ac-223"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="555ac-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="555ac-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555ac-225">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="555ac-225">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="555ac-226">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="555ac-226">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="555ac-227">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="555ac-227">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="555ac-228">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="555ac-228">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="555ac-229">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="555ac-229">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="555ac-230">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="555ac-230">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="555ac-231">**glFog**</span><span class="sxs-lookup"><span data-stu-id="555ac-231">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="555ac-232">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="555ac-232">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="555ac-233">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="555ac-233">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="555ac-234">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="555ac-234">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="555ac-235">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="555ac-235">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="555ac-236">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="555ac-236">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="555ac-237">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="555ac-237">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="555ac-238">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="555ac-238">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="555ac-239">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="555ac-239">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="555ac-240">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="555ac-240">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="555ac-241">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="555ac-241">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="555ac-242">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="555ac-242">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





