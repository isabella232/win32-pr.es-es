---
title: función glTexSubImage1D (GL. h)
description: La función glTexSubImage1D especifica una parte de una imagen de textura de una dimensión existente. No se puede definir una textura nueva con glTexSubImage1D.
ms.assetid: e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac
keywords:
- glTexSubImage1D (función) OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe5510221b738a81f428f9e982a2f9bb2c23588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801627"
---
# <a name="gltexsubimage1d-function"></a><span data-ttu-id="66d7a-105">glTexSubImage1D función)</span><span class="sxs-lookup"><span data-stu-id="66d7a-105">glTexSubImage1D function</span></span>

<span data-ttu-id="66d7a-106">La función **glTexSubImage1D** especifica una parte de una imagen de textura de una dimensión existente.</span><span class="sxs-lookup"><span data-stu-id="66d7a-106">The **glTexSubImage1D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="66d7a-107">No se puede definir una textura nueva con **glTexSubImage1D**.</span><span class="sxs-lookup"><span data-stu-id="66d7a-107">You cannot define a new texture with **glTexSubImage1D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d7a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66d7a-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage1D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="66d7a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66d7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d7a-110">*Destino*</span><span class="sxs-lookup"><span data-stu-id="66d7a-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="66d7a-111">Textura de destino.</span><span class="sxs-lookup"><span data-stu-id="66d7a-111">The target texture.</span></span> <span data-ttu-id="66d7a-112">Debe ser la \_ textura de GL \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="66d7a-112">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="66d7a-113">*level*</span><span class="sxs-lookup"><span data-stu-id="66d7a-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="66d7a-114">El número de nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="66d7a-114">The level-of-detail number.</span></span> <span data-ttu-id="66d7a-115">El nivel 0 es la imagen base.</span><span class="sxs-lookup"><span data-stu-id="66d7a-115">Level 0 is the base image.</span></span> <span data-ttu-id="66d7a-116">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="66d7a-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="66d7a-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="66d7a-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="66d7a-118">Desplazamiento textura en la dirección *x* dentro de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="66d7a-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="66d7a-119">*width*</span><span class="sxs-lookup"><span data-stu-id="66d7a-119">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="66d7a-120">Ancho de la subimagen de textura.</span><span class="sxs-lookup"><span data-stu-id="66d7a-120">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="66d7a-121">*format*</span><span class="sxs-lookup"><span data-stu-id="66d7a-121">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="66d7a-122">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="66d7a-122">The format of the pixel data.</span></span> <span data-ttu-id="66d7a-123">Este parámetro puede suponer uno de los siguientes valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="66d7a-123">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="66d7a-124">Value</span><span class="sxs-lookup"><span data-stu-id="66d7a-124">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="66d7a-125">Significado</span><span class="sxs-lookup"><span data-stu-id="66d7a-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="66d7a-126"><dt>**\_Índice de color de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-126"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="66d7a-127">Cada elemento es un valor único, un índice de color.</span><span class="sxs-lookup"><span data-stu-id="66d7a-127">Each element is a single value, a color index.</span></span> <span data-ttu-id="66d7a-128">Se convierte en un formato de punto fijo (con un número no especificado de 0 bits a la derecha del punto binario), desplazado a la izquierda o a la derecha, según el valor y el signo del turno del índice de contabilidad \_ \_ y se agrega al desplazamiento del índice de GL \_ \_ (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="66d7a-128">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="66d7a-129">El índice resultante se convierte en un conjunto de componentes de color mediante el uso de la asignación de píxeles de GL \_ \_ \_ i \_ a \_ R, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ G, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ B y \_ la asignación de píxeles de GL \_ \_ \_ a \_ una tabla, y se ha fijado en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="66d7a-129">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="66d7a-130"><dt>**\_rojo GL**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-130"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="66d7a-131">Cada elemento es un componente rojo único.</span><span class="sxs-lookup"><span data-stu-id="66d7a-131">Each element is a single red component.</span></span> <span data-ttu-id="66d7a-132">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para verde y azul, y 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="66d7a-132">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="66d7a-133">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="66d7a-133">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="66d7a-134"><dt>**\_verde GL**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-134"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="66d7a-135">Cada elemento es un único componente verde.</span><span class="sxs-lookup"><span data-stu-id="66d7a-135">Each element is a single green component.</span></span> <span data-ttu-id="66d7a-136">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y azul, y 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="66d7a-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="66d7a-137">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="66d7a-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="66d7a-138"><dt>**\_azul GL**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-138"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="66d7a-139">Cada elemento es un único componente azul.</span><span class="sxs-lookup"><span data-stu-id="66d7a-139">Each element is a single blue component.</span></span> <span data-ttu-id="66d7a-140">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y verde, y 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="66d7a-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="66d7a-141">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="66d7a-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="66d7a-142"><dt>**libro \_ de contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-142"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="66d7a-143">Cada elemento es un único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="66d7a-143">Each element is a single alpha component.</span></span> <span data-ttu-id="66d7a-144">Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="66d7a-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="66d7a-145">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="66d7a-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="66d7a-146"><dt>**RGB de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-146"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="66d7a-147">Cada elemento es un triple RGB.</span><span class="sxs-lookup"><span data-stu-id="66d7a-147">Each element is an RGB triple.</span></span> <span data-ttu-id="66d7a-148">Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="66d7a-148">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="66d7a-149">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="66d7a-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="66d7a-150"><dt>**el \_ RGBA de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-150"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="66d7a-151">Cada elemento es un elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="66d7a-151">Each element is a complete RGBA element.</span></span> <span data-ttu-id="66d7a-152">Se convierte al formato de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="66d7a-152">It is converted to floating point format.</span></span> <span data-ttu-id="66d7a-153">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="66d7a-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="66d7a-154"><dt>**luminancia del libro de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-154"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="66d7a-155">Cada elemento es un valor de luminancia único.</span><span class="sxs-lookup"><span data-stu-id="66d7a-155">Each element is a single luminance value.</span></span> <span data-ttu-id="66d7a-156">Se convierte al formato de punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul, y la Asociación de 1,0 para alpha.</span><span class="sxs-lookup"><span data-stu-id="66d7a-156">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="66d7a-157">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="66d7a-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="66d7a-158"><dt>**alfa de luminancia de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-158"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="66d7a-159">Cada elemento es un par de luminancia/alfa.</span><span class="sxs-lookup"><span data-stu-id="66d7a-159">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="66d7a-160">Se convierte al formato de punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="66d7a-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="66d7a-161">Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="66d7a-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="66d7a-162">*type*</span><span class="sxs-lookup"><span data-stu-id="66d7a-162">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="66d7a-163">El tipo de datos de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="66d7a-163">The data type of the pixel data.</span></span> <span data-ttu-id="66d7a-164">Se aceptan los siguientes valores simbólicos: \_ byte sin signo \_ de libro de contabilidad, \_ bytes de contabilidad, \_ mapa de bits de GL, GL \_ sin signo \_ corto, GL \_ corto, libro de contabilidad \_ sin signo de GL \_ , GL \_ int y contabilidad \_ flotante.</span><span class="sxs-lookup"><span data-stu-id="66d7a-164">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="66d7a-165">*píxeles*</span><span class="sxs-lookup"><span data-stu-id="66d7a-165">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="66d7a-166">Puntero a los datos de la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="66d7a-166">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d7a-167">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66d7a-167">Return value</span></span>

<span data-ttu-id="66d7a-168">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="66d7a-168">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66d7a-169">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="66d7a-169">Error codes</span></span>

<span data-ttu-id="66d7a-170">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="66d7a-170">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="66d7a-171">Nombre</span><span class="sxs-lookup"><span data-stu-id="66d7a-171">Name</span></span>                                                                                                  | <span data-ttu-id="66d7a-172">Significado</span><span class="sxs-lookup"><span data-stu-id="66d7a-172">Meaning</span></span>                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66d7a-173"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-173"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="66d7a-174">el *destino* no era la textura de GL \_ \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="66d7a-174">*target* was not GL\_TEXTURE\_1D.</span></span><br/>                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="66d7a-175"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-175"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="66d7a-176">el *formato* no era una constante aceptada.</span><span class="sxs-lookup"><span data-stu-id="66d7a-176">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="66d7a-177"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="66d7a-178">el *tipo* no era una constante aceptada.</span><span class="sxs-lookup"><span data-stu-id="66d7a-178">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="66d7a-179"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="66d7a-180">el *tipo* era un \_ mapa de bits de contabilidad y el *formato* no era un índice de color de GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="66d7a-180">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="66d7a-181"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-181"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="66d7a-182">el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* era el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="66d7a-182">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="66d7a-183"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-183"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="66d7a-184">*xoffset* era menor que *b* o el   +  *ancho* de desplazamiento era mayor que *WB*, donde *w* es el \_ ancho de la textura GL \_ y *b* es el ancho del borde de la \_ textura GL \_ de la imagen de textura que se está modificando.</span><span class="sxs-lookup"><span data-stu-id="66d7a-184">*xoffset* was less than *b*, or *offset* + *width* was greater than *wb*, where *w* is the GL\_TEXTURE\_WIDTH, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span><br/> <span data-ttu-id="66d7a-185">Tenga en cuenta que *w* incluye dos veces el ancho del borde.</span><span class="sxs-lookup"><span data-stu-id="66d7a-185">Note that *w* includes twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="66d7a-186"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-186"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="66d7a-187">el *ancho* era menor que *b*, donde *b* es el ancho del borde de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="66d7a-187">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="66d7a-188"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-188"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="66d7a-189">*Border* no era cero o 1.</span><span class="sxs-lookup"><span data-stu-id="66d7a-189">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="66d7a-190"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-190"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="66d7a-191">Una operación **glTexImage1D** anterior no definió la matriz texure.</span><span class="sxs-lookup"><span data-stu-id="66d7a-191">The texure array was not defined by a previous **glTexImage1D** operation.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="66d7a-192"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="66d7a-193">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="66d7a-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="66d7a-194">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66d7a-194">Remarks</span></span>

<span data-ttu-id="66d7a-195">La texturización unidimensional para un primitivo se habilita mediante [**glEnable**](glenable.md) y **glDisable** con el argumento GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="66d7a-195">One-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_1D.</span></span> <span data-ttu-id="66d7a-196">Durante la texturización, parte de una imagen de textura especificada se asigna a cada primitiva habilitada.</span><span class="sxs-lookup"><span data-stu-id="66d7a-196">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="66d7a-197">La función **glTexSubImage1D** se usa para especificar una subimagen contigua de una imagen de textura de una dimensión existente para la texturización.</span><span class="sxs-lookup"><span data-stu-id="66d7a-197">You use the **glTexSubImage1D** function to specify a contiguous sub-image of an existing one-dimensional texture image for texturing.</span></span>

<span data-ttu-id="66d7a-198">Los textura a los que se hace referencia en *píxeles* reemplazan una región de la matriz de textura existente por índices *x* de *xoffset* y *xoffset* + (*ancho* 1), ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="66d7a-198">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive.</span></span> <span data-ttu-id="66d7a-199">Esta región no puede incluir ningún textura fuera del intervalo de la matriz de textura originalmente especificada.</span><span class="sxs-lookup"><span data-stu-id="66d7a-199">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="66d7a-200">Especificar una subimagen con un *ancho* de cero no tiene ningún efecto y no genera ningún error.</span><span class="sxs-lookup"><span data-stu-id="66d7a-200">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="66d7a-201">La texturización no tiene ningún efecto en el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="66d7a-201">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="66d7a-202">En general, las imágenes de textura se pueden representar con los mismos formatos de datos que los píxeles de un comando [**glDrawPixels**](gldrawpixels.md) , excepto en que \_ no se puede usar el índice de estarcido de GL \_ y el componente de profundidad de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="66d7a-202">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="66d7a-203">Los modos [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="66d7a-203">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="66d7a-204">Las siguientes funciones recuperan información relacionada con **glTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="66d7a-204">The following functions retrieve information related to **glTexSubImage1D**:</span></span>

[<span data-ttu-id="66d7a-205">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="66d7a-205">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="66d7a-206">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="66d7a-206">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="66d7a-207">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d7a-207">Requirements</span></span>



| <span data-ttu-id="66d7a-208">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d7a-208">Requirement</span></span> | <span data-ttu-id="66d7a-209">Value</span><span class="sxs-lookup"><span data-stu-id="66d7a-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66d7a-210">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d7a-210">Minimum supported client</span></span><br/> | <span data-ttu-id="66d7a-211">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="66d7a-211">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="66d7a-212">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d7a-212">Minimum supported server</span></span><br/> | <span data-ttu-id="66d7a-213">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66d7a-213">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66d7a-214">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66d7a-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d7a-215"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-215"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="66d7a-216">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66d7a-216">Library</span></span><br/>                  | <dl> <span data-ttu-id="66d7a-217"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-217"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="66d7a-218">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66d7a-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66d7a-219"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66d7a-219"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d7a-220">Vea también</span><span class="sxs-lookup"><span data-stu-id="66d7a-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d7a-221">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="66d7a-221">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="66d7a-222">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="66d7a-222">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="66d7a-223">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="66d7a-223">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="66d7a-224">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="66d7a-224">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="66d7a-225">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="66d7a-225">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="66d7a-226">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="66d7a-226">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="66d7a-227">**glFog**</span><span class="sxs-lookup"><span data-stu-id="66d7a-227">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="66d7a-228">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="66d7a-228">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="66d7a-229">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="66d7a-229">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="66d7a-230">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="66d7a-230">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="66d7a-231">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="66d7a-231">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="66d7a-232">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="66d7a-232">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="66d7a-233">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="66d7a-233">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="66d7a-234">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="66d7a-234">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="66d7a-235">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="66d7a-235">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="66d7a-236">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="66d7a-236">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="66d7a-237">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="66d7a-237">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





