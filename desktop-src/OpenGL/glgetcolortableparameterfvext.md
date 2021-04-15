---
title: función glGetColorTableParameterfvEXT (GL. h)
description: Las funciones glGetColorTableParameterfvEXT y glGetColorTableParameterivEXT obtienen parámetros de paleta de las tablas de color. | función glGetColorTableParameterfvEXT (GL. h)
ms.assetid: e78051aa-4233-413c-8838-0741b54eab0e
keywords:
- glGetColorTableParameterfvEXT (función) OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterfvEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533ca0c847548fa1de4518079ca6e49d15b6830f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424255"
---
# <a name="glgetcolortableparameterfvext-function"></a><span data-ttu-id="c6a43-105">glGetColorTableParameterfvEXT función)</span><span class="sxs-lookup"><span data-stu-id="c6a43-105">glGetColorTableParameterfvEXT function</span></span>

<span data-ttu-id="c6a43-106">Las funciones **glGetColorTableParameterfvEXT** y [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) obtienen parámetros de paleta de las tablas de color.</span><span class="sxs-lookup"><span data-stu-id="c6a43-106">The **glGetColorTableParameterfvEXT** and [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) functions get palette parameters from color tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a43-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6a43-107">Syntax</span></span>


```C++
void WINAPI glGetColorTableParameterfvEXT(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="c6a43-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6a43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a43-109">*Destino*</span><span class="sxs-lookup"><span data-stu-id="c6a43-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a43-110">Textura de destino de la paleta para la que desea obtener datos de parámetros.</span><span class="sxs-lookup"><span data-stu-id="c6a43-110">The target texture of the palette for which you want parameter data.</span></span> <span data-ttu-id="c6a43-111">Debe ser la textura \_ 1D, textura \_ 2D, \_ textura de proxy \_ 1D o \_ textura de proxy \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="c6a43-111">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="c6a43-112">*PName*</span><span class="sxs-lookup"><span data-stu-id="c6a43-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a43-113">Constante simbólica para el tipo de los datos de parámetro de la paleta a los que apuntan los *parámetros.*</span><span class="sxs-lookup"><span data-stu-id="c6a43-113">A symbolic constant for the type of palette parameter data pointed to by *params*.</span></span>

<span data-ttu-id="c6a43-114">A continuación se indican las constantes simbólicas aceptadas y su significado.</span><span class="sxs-lookup"><span data-stu-id="c6a43-114">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="c6a43-115">Value</span><span class="sxs-lookup"><span data-stu-id="c6a43-115">Value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="c6a43-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c6a43-116">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <span data-ttu-id="c6a43-117"><dt>**\_ \_ ext formato de tabla de color de \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a43-117"><dt>**GL\_COLOR\_TABLE\_FORMAT\_EXT**</dt></span></span> </dl>              | <span data-ttu-id="c6a43-118">Devuelve el formato interno especificado por la llamada más reciente a [**glColorTableEXT**](glcolortableext.md) o el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c6a43-118">Return the internal format specified by the most recent call to [**glColorTableEXT**](glcolortableext.md) or the default value.</span></span><br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <span data-ttu-id="c6a43-119"><dt>**\_ \_ ext ancho de tabla de color de \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a43-119"><dt>**GL\_COLOR\_TABLE\_WIDTH\_EXT**</dt></span></span> </dl>                 | <span data-ttu-id="c6a43-120">Devuelve el ancho de la paleta actual.</span><span class="sxs-lookup"><span data-stu-id="c6a43-120">Return the width of the current palette.</span></span><br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <span data-ttu-id="c6a43-121"><dt>**\_tamaño rojo de la tabla de colores GL \_ \_ \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a43-121"><dt>**GL\_COLOR\_TABLE\_RED\_SIZE\_EXT**</dt></span></span> </dl>       | <span data-ttu-id="c6a43-122">Devuelve el tamaño real utilizado internamente para almacenar el componente rojo de los datos de la paleta.</span><span class="sxs-lookup"><span data-stu-id="c6a43-122">Return the actual size used internally to store the red component of the palette data.</span></span><br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <span data-ttu-id="c6a43-123"><dt>**\_ \_ \_ tamaño verde de tabla \_ de \_ colores de contabilidad general**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a43-123"><dt>**GL\_COLOR\_TABLE\_GREEN\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="c6a43-124">Devuelve el tamaño real utilizado internamente para almacenar el componente verde de los datos de la paleta.</span><span class="sxs-lookup"><span data-stu-id="c6a43-124">Return the actual size used internally to store the green component of the palette data.</span></span><br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <span data-ttu-id="c6a43-125"><dt>**tamaño azul de la tabla de colores de GL \_ \_ \_ \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a43-125"><dt>**GL\_COLOR\_TABLE\_BLUE\_SIZE\_EXT**</dt></span></span> </dl>    | <span data-ttu-id="c6a43-126">Devuelve el tamaño real utilizado internamente para almacenar el componente azul de los datos de la paleta.</span><span class="sxs-lookup"><span data-stu-id="c6a43-126">Return the actual size used internally to store the blue component of the palette data.</span></span><br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <span data-ttu-id="c6a43-127"><dt>**tabla de colores de contabilidad de \_ \_ \_ \_ tamaño alfa \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a43-127"><dt>**GL\_COLOR\_TABLE\_ALPHA\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="c6a43-128">Devuelve el tamaño real utilizado internamente para almacenar el componente alfa de los datos de la paleta.</span><span class="sxs-lookup"><span data-stu-id="c6a43-128">Return the actual size used internally to store the alpha component of the palette data.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="c6a43-129">*params*</span><span class="sxs-lookup"><span data-stu-id="c6a43-129">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a43-130">Apunta a los datos de parámetro de la tabla de colores especificados por el parámetro *PName* .</span><span class="sxs-lookup"><span data-stu-id="c6a43-130">Points to the color table parameter data specified by the *pname* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6a43-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6a43-131">Return value</span></span>

<span data-ttu-id="c6a43-132">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c6a43-132">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a43-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6a43-133">Remarks</span></span>

<span data-ttu-id="c6a43-134">Las funciones **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT** se usan para recuperar datos de parámetros específicos de las tablas de color establecidas con [**glColorTableEXT**](glcolortableext.md) para las paletas de texturas de destino.</span><span class="sxs-lookup"><span data-stu-id="c6a43-134">You use the **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** functions to retrieve specific parameter data from color tables set with [**glColorTableEXT**](glcolortableext.md) for targeted texture palettes.</span></span> <span data-ttu-id="c6a43-135">También puede usar estas funciones para determinar el número de entradas de la tabla de colores que devuelve **glGetColorTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="c6a43-135">Also you can use these functions to determine the number of color table entries that **glGetColorTableEXT** returns.</span></span>

<span data-ttu-id="c6a43-136">Cuando el parámetro de *destino* es \_ GL \_ proxy Texture \_ 1D o GL \_ proxy \_ Texture \_ 2D, y la implementación no admite los valores especificados para el *formato* o el *ancho*, **glColorTableEXT** puede generar un error al crear la tabla de colores solicitada.</span><span class="sxs-lookup"><span data-stu-id="c6a43-136">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="c6a43-137">En este caso, la tabla de colores está vacía y todos los parámetros recuperados serán cero.</span><span class="sxs-lookup"><span data-stu-id="c6a43-137">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="c6a43-138">Puede determinar si OpenGL admite un formato y un tamaño de tabla de colores determinados mediante una llamada a **glColorTableEXT** con un destino de proxy y, a continuación, llamar a **glGetColorTableParameterivEXT** o **glGetColorTableParameterfvEXT** para determinar si el parámetro de ancho coincide con el establecido por **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="c6a43-138">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="c6a43-139">Si el ancho recuperado es cero, se produce un error en la solicitud de tabla de colores por **glColorTable** .</span><span class="sxs-lookup"><span data-stu-id="c6a43-139">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="c6a43-140">Si el ancho recuperado no es cero, puede llamar a **glColorTable** con el destino real con la textura \_ 1D o textura \_ 2D para establecer la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="c6a43-140">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

<span data-ttu-id="c6a43-141">Las funciones **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT** son funciones de extensión que no forman parte de la biblioteca estándar de OpenGL, pero que forman parte de la extensión de textura de paleta de GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c6a43-141">The **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** functions are extension functions that are not part of the standard OpenGL library but are part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="c6a43-142">Para comprobar si la implementación de OpenGL es compatible con **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT**, llame a [**glGetString**](glgetstring.md)**(** extensiones de GL \_ **)**.</span><span class="sxs-lookup"><span data-stu-id="c6a43-142">To check whether your implementation of OpenGL supports **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT**, call [**glGetString**](glgetstring.md)**(** GL\_EXTENSIONS **)**.</span></span> <span data-ttu-id="c6a43-143">Si devuelve la \_ \_ textura de paleta ext \_ de GL, se admiten **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT** .</span><span class="sxs-lookup"><span data-stu-id="c6a43-143">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** are supported.</span></span> <span data-ttu-id="c6a43-144">Para obtener la dirección de la función de una función de extensión, llame a [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="c6a43-144">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a43-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6a43-145">Requirements</span></span>



| <span data-ttu-id="c6a43-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a43-146">Requirement</span></span> | <span data-ttu-id="c6a43-147">Value</span><span class="sxs-lookup"><span data-stu-id="c6a43-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c6a43-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6a43-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a43-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c6a43-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="c6a43-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6a43-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a43-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6a43-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c6a43-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6a43-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6a43-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6a43-153"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a43-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6a43-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a43-155">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="c6a43-155">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="c6a43-156">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="c6a43-156">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="c6a43-157">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="c6a43-157">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="c6a43-158">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="c6a43-158">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="c6a43-159">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c6a43-159">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





