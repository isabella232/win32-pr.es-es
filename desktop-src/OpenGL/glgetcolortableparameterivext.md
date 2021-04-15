---
title: función glGetColorTableParameterivEXT (GL. h)
description: Las funciones glGetColorTableParameterfvEXT y glGetColorTableParameterivEXT obtienen parámetros de paleta de las tablas de color. | función glGetColorTableParameterivEXT (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- glGetColorTableParameterivEXT (función) OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689819"
---
# <a name="glgetcolortableparameterivext-function"></a><span data-ttu-id="f29b1-105">glGetColorTableParameterivEXT función)</span><span class="sxs-lookup"><span data-stu-id="f29b1-105">glGetColorTableParameterivEXT function</span></span>

<span data-ttu-id="f29b1-106">Las funciones [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) y **glGetColorTableParameterivEXT** obtienen parámetros de paleta de las tablas de color.</span><span class="sxs-lookup"><span data-stu-id="f29b1-106">The [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) and **glGetColorTableParameterivEXT** functions get palette parameters from color tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f29b1-107">Syntax</span></span>


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="f29b1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f29b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f29b1-109">*Destino*</span><span class="sxs-lookup"><span data-stu-id="f29b1-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="f29b1-110">Textura de destino de la paleta para la que desea obtener datos de parámetros.</span><span class="sxs-lookup"><span data-stu-id="f29b1-110">The target texture of the palette for which you want parameter data.</span></span> <span data-ttu-id="f29b1-111">Debe ser la textura \_ 1D, textura \_ 2D, \_ textura de proxy \_ 1D o \_ textura de proxy \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="f29b1-111">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="f29b1-112">*PName*</span><span class="sxs-lookup"><span data-stu-id="f29b1-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="f29b1-113">Constante simbólica para el tipo de los datos de parámetro de la paleta a los que apuntan los *parámetros.*</span><span class="sxs-lookup"><span data-stu-id="f29b1-113">A symbolic constant for the type of palette parameter data pointed to by *params*.</span></span>

<span data-ttu-id="f29b1-114">A continuación se indican las constantes simbólicas aceptadas y su significado.</span><span class="sxs-lookup"><span data-stu-id="f29b1-114">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="f29b1-115">Value</span><span class="sxs-lookup"><span data-stu-id="f29b1-115">Value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="f29b1-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f29b1-116">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <span data-ttu-id="f29b1-117"><dt>**\_ \_ ext formato de tabla de color de \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f29b1-117"><dt>**GL\_COLOR\_TABLE\_FORMAT\_EXT**</dt></span></span> </dl>              | <span data-ttu-id="f29b1-118">Devuelve el formato interno especificado por la llamada más reciente a [**glColorTableEXT**](glcolortableext.md) o el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f29b1-118">Return the internal format specified by the most recent call to [**glColorTableEXT**](glcolortableext.md) or the default value.</span></span><br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <span data-ttu-id="f29b1-119"><dt>**\_ \_ ext ancho de tabla de color de \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f29b1-119"><dt>**GL\_COLOR\_TABLE\_WIDTH\_EXT**</dt></span></span> </dl>                 | <span data-ttu-id="f29b1-120">Devuelve el ancho de la paleta actual.</span><span class="sxs-lookup"><span data-stu-id="f29b1-120">Return the width of the current palette.</span></span><br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <span data-ttu-id="f29b1-121"><dt>**\_tamaño rojo de la tabla de colores GL \_ \_ \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="f29b1-121"><dt>**GL\_COLOR\_TABLE\_RED\_SIZE\_EXT**</dt></span></span> </dl>       | <span data-ttu-id="f29b1-122">Devuelve el tamaño real utilizado internamente para almacenar el componente rojo de los datos de la paleta.</span><span class="sxs-lookup"><span data-stu-id="f29b1-122">Return the actual size used internally to store the red component of the palette data.</span></span><br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <span data-ttu-id="f29b1-123"><dt>**\_ \_ \_ tamaño verde de tabla \_ de \_ colores de contabilidad general**</dt></span><span class="sxs-lookup"><span data-stu-id="f29b1-123"><dt>**GL\_COLOR\_TABLE\_GREEN\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="f29b1-124">Devuelve el tamaño real utilizado internamente para almacenar el componente verde de los datos de la paleta.</span><span class="sxs-lookup"><span data-stu-id="f29b1-124">Return the actual size used internally to store the green component of the palette data.</span></span><br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <span data-ttu-id="f29b1-125"><dt>**tamaño azul de la tabla de colores de GL \_ \_ \_ \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="f29b1-125"><dt>**GL\_COLOR\_TABLE\_BLUE\_SIZE\_EXT**</dt></span></span> </dl>    | <span data-ttu-id="f29b1-126">Devuelve el tamaño real utilizado internamente para almacenar el componente azul de los datos de la paleta.</span><span class="sxs-lookup"><span data-stu-id="f29b1-126">Return the actual size used internally to store the blue component of the palette data.</span></span><br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <span data-ttu-id="f29b1-127"><dt>**tabla de colores de contabilidad de \_ \_ \_ \_ tamaño alfa \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="f29b1-127"><dt>**GL\_COLOR\_TABLE\_ALPHA\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="f29b1-128">Devuelve el tamaño real utilizado internamente para almacenar el componente alfa de los datos de la paleta.</span><span class="sxs-lookup"><span data-stu-id="f29b1-128">Return the actual size used internally to store the alpha component of the palette data.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="f29b1-129">*params*</span><span class="sxs-lookup"><span data-stu-id="f29b1-129">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="f29b1-130">Apunta a los datos de parámetro de la tabla de colores especificados por el parámetro *PName* .</span><span class="sxs-lookup"><span data-stu-id="f29b1-130">Points to the color table parameter data specified by the *pname* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f29b1-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f29b1-131">Return value</span></span>

<span data-ttu-id="f29b1-132">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f29b1-132">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f29b1-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f29b1-133">Remarks</span></span>

<span data-ttu-id="f29b1-134">Las funciones **glGetColorTableParameterivEXT** y [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) se usan para recuperar datos de parámetros específicos de las tablas de color establecidas con [**glColorTableEXT**](glcolortableext.md) para las paletas de texturas de destino.</span><span class="sxs-lookup"><span data-stu-id="f29b1-134">You use the **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions to retrieve specific parameter data from color tables set with [**glColorTableEXT**](glcolortableext.md) for targeted texture palettes.</span></span> <span data-ttu-id="f29b1-135">También puede usar estas funciones para determinar el número de entradas de la tabla de colores que devuelve **glGetColorTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="f29b1-135">Also you can use these functions to determine the number of color table entries that **glGetColorTableEXT** returns.</span></span>

<span data-ttu-id="f29b1-136">Cuando el parámetro de *destino* es \_ GL \_ proxy Texture \_ 1D o GL \_ proxy \_ Texture \_ 2D, y la implementación no admite los valores especificados para el *formato* o el *ancho*, **glColorTableEXT** puede generar un error al crear la tabla de colores solicitada.</span><span class="sxs-lookup"><span data-stu-id="f29b1-136">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="f29b1-137">En este caso, la tabla de colores está vacía y todos los parámetros recuperados serán cero.</span><span class="sxs-lookup"><span data-stu-id="f29b1-137">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="f29b1-138">Puede determinar si OpenGL admite un formato y un tamaño de tabla de colores determinados mediante una llamada a **glColorTableEXT** con un destino de proxy y, a continuación, llamar a **glGetColorTableParameterivEXT** o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para determinar si el parámetro de ancho coincide con el establecido por **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="f29b1-138">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling **glGetColorTableParameterivEXT** or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="f29b1-139">Si el ancho recuperado es cero, se produce un error en la solicitud de tabla de colores por **glColorTable** .</span><span class="sxs-lookup"><span data-stu-id="f29b1-139">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="f29b1-140">Si el ancho recuperado no es cero, puede llamar a **glColorTable** con el destino real con la textura \_ 1D o textura \_ 2D para establecer la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="f29b1-140">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

<span data-ttu-id="f29b1-141">Las funciones **glGetColorTableParameterivEXT** y [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) son funciones de extensión que no forman parte de la biblioteca estándar de OpenGL, pero que forman parte de la extensión de textura de paleta de GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f29b1-141">The **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions are extension functions that are not part of the standard OpenGL library but are part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="f29b1-142">Para comprobar si la implementación de OpenGL es compatible con **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT**, llame a [**glGetString**](glgetstring.md)**(** extensiones de GL \_ **)**.</span><span class="sxs-lookup"><span data-stu-id="f29b1-142">To check whether your implementation of OpenGL supports **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT**, call [**glGetString**](glgetstring.md)**(** GL\_EXTENSIONS **)**.</span></span> <span data-ttu-id="f29b1-143">Si devuelve la \_ \_ textura de paleta ext \_ de GL, se admiten **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT** .</span><span class="sxs-lookup"><span data-stu-id="f29b1-143">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** are supported.</span></span> <span data-ttu-id="f29b1-144">Para obtener la dirección de la función de una función de extensión, llame a [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="f29b1-144">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="f29b1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f29b1-145">Requirements</span></span>



| <span data-ttu-id="f29b1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f29b1-146">Requirement</span></span> | <span data-ttu-id="f29b1-147">Value</span><span class="sxs-lookup"><span data-stu-id="f29b1-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f29b1-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f29b1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f29b1-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f29b1-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="f29b1-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f29b1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f29b1-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f29b1-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f29b1-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f29b1-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="f29b1-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f29b1-153"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f29b1-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="f29b1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29b1-155">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="f29b1-155">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="f29b1-156">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="f29b1-156">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="f29b1-157">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="f29b1-157">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="f29b1-158">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="f29b1-158">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="f29b1-159">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="f29b1-159">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





