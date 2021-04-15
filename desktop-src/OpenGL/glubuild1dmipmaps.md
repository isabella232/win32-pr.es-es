---
title: función gluBuild1DMipmaps (GLU. h)
description: La función gluBuild1DMipmaps crea mapas de bits 1D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- gluBuild1DMipmaps (función) OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676690"
---
# <a name="glubuild1dmipmaps-function"></a><span data-ttu-id="85cc8-104">gluBuild1DMipmaps función)</span><span class="sxs-lookup"><span data-stu-id="85cc8-104">gluBuild1DMipmaps function</span></span>

<span data-ttu-id="85cc8-105">La función **gluBuild1DMipmaps** crea mapas de bits 1D.</span><span class="sxs-lookup"><span data-stu-id="85cc8-105">The **gluBuild1DMipmaps** function creates 1-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="85cc8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85cc8-106">Syntax</span></span>


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="85cc8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85cc8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85cc8-108">*Destino*</span><span class="sxs-lookup"><span data-stu-id="85cc8-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="85cc8-109">Textura de destino.</span><span class="sxs-lookup"><span data-stu-id="85cc8-109">The target texture.</span></span> <span data-ttu-id="85cc8-110">Debe ser la \_ textura de GL \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="85cc8-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="85cc8-111">*components*</span><span class="sxs-lookup"><span data-stu-id="85cc8-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="85cc8-112">El número de componentes de color de la textura.</span><span class="sxs-lookup"><span data-stu-id="85cc8-112">The number of color components in the texture.</span></span> <span data-ttu-id="85cc8-113">Debe ser 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="85cc8-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="85cc8-114">*width*</span><span class="sxs-lookup"><span data-stu-id="85cc8-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="85cc8-115">Ancho de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="85cc8-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="85cc8-116">*format*</span><span class="sxs-lookup"><span data-stu-id="85cc8-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="85cc8-117">Formato de los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85cc8-117">The format of the pixel data.</span></span> <span data-ttu-id="85cc8-118">Los valores siguientes son válidos: GL \_ color \_ index, GL \_ rojo, GL \_ Green, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, \_ luminancia de GL o luminancia de contabilidad general \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="85cc8-118">The following values are valid: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="85cc8-119">*type*</span><span class="sxs-lookup"><span data-stu-id="85cc8-119">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="85cc8-120">El tipo de datos para los *datos*.</span><span class="sxs-lookup"><span data-stu-id="85cc8-120">The data type for *data*.</span></span> <span data-ttu-id="85cc8-121">Los valores siguientes son válidos: libro de \_ \_ bytes sin signo de GL, \_ bytes de contabilidad, mapa de bits de GL \_ , libro de contabilidad \_ inferior sin signo corto \_ , GL \_ Short, contabilidad de \_ tipo int sin signo, \_ GL \_ int o GL \_ flotante.</span><span class="sxs-lookup"><span data-stu-id="85cc8-121">The following values are valid: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="85cc8-122">*data*</span><span class="sxs-lookup"><span data-stu-id="85cc8-122">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="85cc8-123">Puntero a los datos de la imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="85cc8-123">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85cc8-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85cc8-124">Return value</span></span>

<span data-ttu-id="85cc8-125">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="85cc8-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85cc8-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85cc8-126">Remarks</span></span>

<span data-ttu-id="85cc8-127">La función **gluBuild1DMipmaps** obtiene la imagen de entrada y genera todas las imágenes de mipmap (mediante [**gluScaleImage**](gluscaleimage.md)) para que la imagen de entrada se pueda usar como imagen de textura de mipmapped.</span><span class="sxs-lookup"><span data-stu-id="85cc8-127">The **gluBuild1DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so that the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="85cc8-128">A continuación, se llama a la función [**glTexImage1D**](glteximage1d.md) para cargar cada una de las imágenes.</span><span class="sxs-lookup"><span data-stu-id="85cc8-128">The [**glTexImage1D**](glteximage1d.md) function is then called to load each of the images.</span></span> <span data-ttu-id="85cc8-129">Si el ancho de la imagen de entrada no es una potencia de dos, la imagen se escala a la potencia más cercana de dos antes de que se generen los mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="85cc8-129">If the width of the input image is not a power of two, then the image is scaled to the nearest power of two before the mipmaps are generated.</span></span>

<span data-ttu-id="85cc8-130">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="85cc8-130">A return value of zero indicates success.</span></span> <span data-ttu-id="85cc8-131">De lo contrario, se devuelve un código de error GLU (vea [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="85cc8-131">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="85cc8-132">Para obtener una descripción de los valores aceptables para el parámetro *Format* , vea **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="85cc8-132">For a description of the acceptable values for the *format* parameter, see **glTexImage1D**.</span></span> <span data-ttu-id="85cc8-133">Para obtener una descripción de los valores aceptables para el parámetro de *tipo* , vea [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="85cc8-133">For a description of the acceptable values for the *type* parameter, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85cc8-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85cc8-134">Requirements</span></span>



| <span data-ttu-id="85cc8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="85cc8-135">Requirement</span></span> | <span data-ttu-id="85cc8-136">Value</span><span class="sxs-lookup"><span data-stu-id="85cc8-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="85cc8-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85cc8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="85cc8-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="85cc8-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="85cc8-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85cc8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="85cc8-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85cc8-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="85cc8-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85cc8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="85cc8-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="85cc8-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="85cc8-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85cc8-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="85cc8-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85cc8-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="85cc8-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85cc8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85cc8-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85cc8-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85cc8-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="85cc8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85cc8-148">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="85cc8-148">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="85cc8-149">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="85cc8-149">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="85cc8-150">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="85cc8-150">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="85cc8-151">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="85cc8-151">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





