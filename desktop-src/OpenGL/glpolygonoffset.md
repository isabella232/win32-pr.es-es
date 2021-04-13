---
title: función glPolygonOffset (GL. h)
description: La función glPolygonOffset establece la escala y las unidades que usa OpenGL para calcular los valores de profundidad.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glPolygonOffset (función) OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422390"
---
# <a name="glpolygonoffset-function"></a><span data-ttu-id="2ea99-104">glPolygonOffset función)</span><span class="sxs-lookup"><span data-stu-id="2ea99-104">glPolygonOffset function</span></span>

<span data-ttu-id="2ea99-105">La función **glPolygonOffset** establece la escala y las unidades que usa OpenGL para calcular los valores de profundidad.</span><span class="sxs-lookup"><span data-stu-id="2ea99-105">The **glPolygonOffset** function sets the scale and units OpenGL uses to calculate depth values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea99-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ea99-106">Syntax</span></span>


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a><span data-ttu-id="2ea99-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ea99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ea99-108">*diez*</span><span class="sxs-lookup"><span data-stu-id="2ea99-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="2ea99-109">Especifica un factor de escala que se usa para crear un desplazamiento de profundidad variable para cada polígono.</span><span class="sxs-lookup"><span data-stu-id="2ea99-109">Specifies a scale factor that is used to create a variable depth offset for each polygon.</span></span> <span data-ttu-id="2ea99-110">El valor inicial es cero.</span><span class="sxs-lookup"><span data-stu-id="2ea99-110">The initial value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="2ea99-111">*participa*</span><span class="sxs-lookup"><span data-stu-id="2ea99-111">*units*</span></span> 
</dt> <dd>

<span data-ttu-id="2ea99-112">Especifica un valor que se multiplica por un valor específico de la implementación para crear un desplazamiento de profundidad constante.</span><span class="sxs-lookup"><span data-stu-id="2ea99-112">Specifies a value that is multiplied by an implementation-specific value to create a constant depth offset.</span></span> <span data-ttu-id="2ea99-113">El valor inicial es 0.</span><span class="sxs-lookup"><span data-stu-id="2ea99-113">The initial value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ea99-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ea99-114">Return value</span></span>

<span data-ttu-id="2ea99-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2ea99-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ea99-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2ea99-116">Error codes</span></span>

<span data-ttu-id="2ea99-117">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="2ea99-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2ea99-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ea99-118">Name</span></span>                                                                                                  | <span data-ttu-id="2ea99-119">Significado</span><span class="sxs-lookup"><span data-stu-id="2ea99-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ea99-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ea99-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2ea99-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2ea99-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2ea99-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ea99-122">Remarks</span></span>

<span data-ttu-id="2ea99-123">Cuando \_ se habilita el desplazamiento de polígono de GL \_ , el valor de profundidad de cada fragmento se desplazará después de que se interpola a partir de los valores de profundidad de los vértices adecuados.</span><span class="sxs-lookup"><span data-stu-id="2ea99-123">When GL\_POLYGON\_OFFSET is enabled, each fragment's depth value will be offset after it is interpolated from the depth values of the appropriate vertices.</span></span> <span data-ttu-id="2ea99-124">El valor del desplazamiento es *factor* \* ? z + r \* *unidades*, donde? z es una medida del cambio en profundidad en relación con el área de la pantalla del polígono y r es el valor más pequeño que se garantiza para generar un desplazamiento que se pueda resolver para una implementación determinada.</span><span class="sxs-lookup"><span data-stu-id="2ea99-124">The value of the offset is *factor* \* ?z + r \**units*, where ?z is a measurement of the change in depth relative to the screen area of the polygon, and r is the smallest value that is guaranteed to produce a resolvable offset for a given implementation.</span></span> <span data-ttu-id="2ea99-125">El desplazamiento se agrega antes de que se realice la prueba de profundidad y antes de que el valor se escriba en el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="2ea99-125">The offset is added before the depth test is performed and before the value is written into the depth buffer.</span></span>

<span data-ttu-id="2ea99-126">La función **glPolygonOffset** es útil para representar imágenes de línea oculta, para aplicar marcas a superficies y para representar sólidos con bordes resaltados.</span><span class="sxs-lookup"><span data-stu-id="2ea99-126">The **glPolygonOffset** function is useful for rendering hidden-line images, for applying decals to surfaces, and for rendering solids with highlighted edges.</span></span>

<span data-ttu-id="2ea99-127">La función **glPolygonOffset** no tiene ningún efecto en las coordenadas de profundidad colocadas en el búfer de comentarios.</span><span class="sxs-lookup"><span data-stu-id="2ea99-127">The **glPolygonOffset** function has no effect on depth coordinates placed in the feedback buffer.</span></span> <span data-ttu-id="2ea99-128">Tampoco tiene ningún efecto en la selección.</span><span class="sxs-lookup"><span data-stu-id="2ea99-128">It also has no effect on selection.</span></span>

<span data-ttu-id="2ea99-129">Las siguientes funciones recuperan información relacionada con **glPolygonOffset**:</span><span class="sxs-lookup"><span data-stu-id="2ea99-129">The following functions retrieve information related to **glPolygonOffset**:</span></span>

-   <span data-ttu-id="2ea99-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ el \_ factor de desplazamiento de polígono de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="2ea99-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_FACTOR</span></span>
-   <span data-ttu-id="2ea99-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con unidades de \_ desplazamiento de polígono de argumento \_ \_</span><span class="sxs-lookup"><span data-stu-id="2ea99-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_UNITS</span></span>
-   <span data-ttu-id="2ea99-132">[**glIsEnabled**](glisenabled.md) con argumento de \_ desplazamiento de polígono de contabilidad de argumentos \_ \_</span><span class="sxs-lookup"><span data-stu-id="2ea99-132">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_FILL</span></span>
-   <span data-ttu-id="2ea99-133">[**glIsEnabled**](glisenabled.md) con el argumento \_ de \_ línea de desplazamiento de polígono de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="2ea99-133">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_LINE</span></span>
-   <span data-ttu-id="2ea99-134">[**glIsEnabled**](glisenabled.md) con el \_ punto de \_ desplazamiento de polígono de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="2ea99-134">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_POINT</span></span>

> [!Note]  
> <span data-ttu-id="2ea99-135">La función **glPolygonOffset** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2ea99-135">The **glPolygonOffset** function is only available in OpenGl version 1.1 or greater.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ea99-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ea99-136">Requirements</span></span>



| <span data-ttu-id="2ea99-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ea99-137">Requirement</span></span> | <span data-ttu-id="2ea99-138">Value</span><span class="sxs-lookup"><span data-stu-id="2ea99-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea99-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ea99-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2ea99-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2ea99-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2ea99-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ea99-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2ea99-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ea99-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ea99-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ea99-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ea99-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ea99-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2ea99-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ea99-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ea99-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ea99-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2ea99-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ea99-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ea99-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ea99-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ea99-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ea99-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ea99-150">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="2ea99-150">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="2ea99-151">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="2ea99-151">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="2ea99-152">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="2ea99-152">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="2ea99-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="2ea99-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2ea99-154">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2ea99-154">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="2ea99-155">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="2ea99-155">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="2ea99-156">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="2ea99-156">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="2ea99-157">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="2ea99-157">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





