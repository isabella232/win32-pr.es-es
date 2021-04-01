---
title: ID2D1CommandSink1 SetPrimitiveBlend1, método
description: Establece un nuevo modo de mezcla primitivo.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- Método SetPrimitiveBlend1 Direct2D
- Método SetPrimitiveBlend1 Direct2D, interfaz ID2D1CommandSink1
- Interfaz ID2D1CommandSink1 Direct2D, método SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150226"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a><span data-ttu-id="14c63-106">ID2D1CommandSink1:: SetPrimitiveBlend1 (método)</span><span class="sxs-lookup"><span data-stu-id="14c63-106">ID2D1CommandSink1::SetPrimitiveBlend1 method</span></span>

<span data-ttu-id="14c63-107">Establece un nuevo modo de mezcla primitivo.</span><span class="sxs-lookup"><span data-stu-id="14c63-107">Sets a new primitive blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c63-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14c63-108">Syntax</span></span>


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a><span data-ttu-id="14c63-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14c63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c63-110">*primitiveBlend*</span><span class="sxs-lookup"><span data-stu-id="14c63-110">*primitiveBlend*</span></span> 
</dt> <dd>

<span data-ttu-id="14c63-111">Tipo: **[ **D2D1 \_ primitiva \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span><span class="sxs-lookup"><span data-stu-id="14c63-111">Type: **[**D2D1\_PRIMITIVE\_BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span></span>

<span data-ttu-id="14c63-112">Combinación primitiva que se aplicará a los primitivos posteriores.</span><span class="sxs-lookup"><span data-stu-id="14c63-112">The primitive blend that will apply to subsequent primitives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c63-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14c63-113">Return value</span></span>

<span data-ttu-id="14c63-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14c63-114">Type: **HRESULT**</span></span>

<span data-ttu-id="14c63-115">Si el método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="14c63-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14c63-116">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14c63-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14c63-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14c63-117">Remarks</span></span>

### <a name="blend-modes"></a><span data-ttu-id="14c63-118">Modos de fusión</span><span class="sxs-lookup"><span data-stu-id="14c63-118">Blend modes</span></span>

<span data-ttu-id="14c63-119">En la representación con alias (excepto en el modo MIN), el valor de salida O se calcula mediante la interpolación lineal del valor *Blend (S, D)* con el valor de píxel de destino, en función de la cantidad que el primitivo cubre el píxel de destino.</span><span class="sxs-lookup"><span data-stu-id="14c63-119">For aliased rendering (except for MIN mode), the output value O is computed by linearly interpolating the value *blend(S, D)* with the destination pixel value, based on the amount that the primitive covers the destination pixel.</span></span>

<span data-ttu-id="14c63-120">En la tabla siguiente se muestran los modos de mezcla primitivos para la combinación con alias y con suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="14c63-120">The table here shows the primitive blend modes for both aliased and antialiased blending.</span></span> <span data-ttu-id="14c63-121">Las ecuaciones que aparecen en la tabla usan estos elementos:</span><span class="sxs-lookup"><span data-stu-id="14c63-121">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="14c63-122">O = salida</span><span class="sxs-lookup"><span data-stu-id="14c63-122">O = Output</span></span>
-   <span data-ttu-id="14c63-123">S = origen</span><span class="sxs-lookup"><span data-stu-id="14c63-123">S = Source</span></span>
-   <span data-ttu-id="14c63-124">SA = alfa de origen</span><span class="sxs-lookup"><span data-stu-id="14c63-124">SA = Source Alpha</span></span>
-   <span data-ttu-id="14c63-125">D = destino</span><span class="sxs-lookup"><span data-stu-id="14c63-125">D = Destination</span></span>
-   <span data-ttu-id="14c63-126">DA = alfa de destino</span><span class="sxs-lookup"><span data-stu-id="14c63-126">DA = Destination Alpha</span></span>
-   <span data-ttu-id="14c63-127">C = cobertura de píxeles</span><span class="sxs-lookup"><span data-stu-id="14c63-127">C = Pixel coverage</span></span>



| <span data-ttu-id="14c63-128">Modo de mezcla primitivo</span><span class="sxs-lookup"><span data-stu-id="14c63-128">Primitive blend mode</span></span>                 | <span data-ttu-id="14c63-129">Combinación con alias</span><span class="sxs-lookup"><span data-stu-id="14c63-129">Aliased blending</span></span>                            | <span data-ttu-id="14c63-130">Mezcla suavizada</span><span class="sxs-lookup"><span data-stu-id="14c63-130">Antialiased blending</span></span>            | <span data-ttu-id="14c63-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="14c63-131">Description</span></span>                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c63-132">\_Origen de mezcla primitivo de D2D1 \_ \_ \_ sobre</span><span class="sxs-lookup"><span data-stu-id="14c63-132">D2D1\_PRIMITIVE\_BLEND\_SOURCE\_OVER</span></span> | <span data-ttu-id="14c63-133">O = (S + (1 SA) \* D) \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="14c63-133">O = (S + (1   SA) \* D) \* C + D \* (1   C)</span></span> | <span data-ttu-id="14c63-134">O = S \* C + D \* (1 SA \* C)</span><span class="sxs-lookup"><span data-stu-id="14c63-134">O = S \* C + D \*(1   SA \*C)</span></span>   | <span data-ttu-id="14c63-135">Modo de mezcla de origen a destino estándar.</span><span class="sxs-lookup"><span data-stu-id="14c63-135">The standard source-over-destination blend mode.</span></span>                                                                         |
| <span data-ttu-id="14c63-136">\_Copia de \_ Blend D2D1 primitiva \_</span><span class="sxs-lookup"><span data-stu-id="14c63-136">D2D1\_PRIMITIVE\_BLEND\_COPY</span></span>         | <span data-ttu-id="14c63-137">O = S \* C + D \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="14c63-137">O = S \* C + D \* (1   C)</span></span>                   | <span data-ttu-id="14c63-138">O = S \* C + D \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="14c63-138">O = S \* C + D \* (1   C)</span></span>       | <span data-ttu-id="14c63-139">El origen se copia en el destino; los píxeles de destino se omiten.</span><span class="sxs-lookup"><span data-stu-id="14c63-139">The source is copied to the destination; the destination pixels are ignored.</span></span>                                             |
| <span data-ttu-id="14c63-140">D2D1 \_ primitiva de \_ mezcla \_ mínima</span><span class="sxs-lookup"><span data-stu-id="14c63-140">D2D1\_PRIMITIVE\_BLEND\_MIN</span></span>          | <span data-ttu-id="14c63-141">O = min (S + 1-SA, D)</span><span class="sxs-lookup"><span data-stu-id="14c63-141">O = Min(S + 1-SA, D)</span></span>                        | <span data-ttu-id="14c63-142">O = min (S \* c + 1 SA \* C, D)</span><span class="sxs-lookup"><span data-stu-id="14c63-142">O = Min(S \* C + 1   SA \*C, D)</span></span> | <span data-ttu-id="14c63-143">Los valores de píxeles resultantes usan el mínimo de los valores de píxel de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="14c63-143">The resulting pixel values use the minimum of the source and destination pixel values.</span></span> <span data-ttu-id="14c63-144">Disponible en Windows 8 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="14c63-144">Available in Windows 8 and later.</span></span> |
| <span data-ttu-id="14c63-145">D2D1 \_ primitiva \_ Blend \_ Add</span><span class="sxs-lookup"><span data-stu-id="14c63-145">D2D1\_PRIMITIVE\_BLEND\_ADD</span></span>          | <span data-ttu-id="14c63-146">O = (S + D) \* C + d \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="14c63-146">O = (S + D) \* C + D \* (1   C)</span></span>             | <span data-ttu-id="14c63-147">O = S \* C + D</span><span class="sxs-lookup"><span data-stu-id="14c63-147">O = S \* C + D</span></span>                  | <span data-ttu-id="14c63-148">Los valores de píxeles resultantes son la suma de los valores de los píxeles de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="14c63-148">The resulting pixel values are the sum of the source and destination pixel values.</span></span> <span data-ttu-id="14c63-149">Disponible en Windows 8 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="14c63-149">Available in Windows 8 and later.</span></span>     |



 

![Ilustración de los modos de mezcla primitivos de direct2d con opacidad y fondo variables.](images/primblenddemo.png)

<span data-ttu-id="14c63-151">Ilustración de los modos de mezcla primitivos con opacidad y fondo variables.</span><span class="sxs-lookup"><span data-stu-id="14c63-151">An illustration of the primitive blend modes with varying opacity and backgrounds.</span></span>

<span data-ttu-id="14c63-152">La mezcla primitiva se aplicará a toda la primitiva dibujada en el contexto, a menos que se invalide con el parámetro *compositeMode* en la API [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .</span><span class="sxs-lookup"><span data-stu-id="14c63-152">The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the *compositeMode* parameter on the [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API.</span></span>

<span data-ttu-id="14c63-153">La mezcla primitiva se aplica al interior de cualquier primitiva dibujada en el contexto.</span><span class="sxs-lookup"><span data-stu-id="14c63-153">The primitive blend applies to the interior of any primitives drawn on the context.</span></span> <span data-ttu-id="14c63-154">En el caso de [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), lo implicará el rectángulo de imagen, el desplazamiento y la transformación universal.</span><span class="sxs-lookup"><span data-stu-id="14c63-154">In the case of [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), this will be implied by the image rectangle, offset and world transform.</span></span>

<span data-ttu-id="14c63-155">Si la mezcla primitiva es algo que no sea **D2D1 \_ primitiva \_ Blend \_** , se desactivará la representación de ClearType.</span><span class="sxs-lookup"><span data-stu-id="14c63-155">If the primitive blend is anything other than **D2D1\_PRIMITIVE\_BLEND\_OVER** then ClearType rendering will be turned off.</span></span> <span data-ttu-id="14c63-156">Si la aplicación fuerza explícitamente la representación ClearType en estos modos, el contexto de dibujo se colocará en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="14c63-156">If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state.</span></span> <span data-ttu-id="14c63-157">Se \_ \_ devolverá un estado incorrecto de D2DERR desde [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="14c63-157">D2DERR\_WRONG\_STATE will be returned from either [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span>

## <a name="requirements"></a><span data-ttu-id="14c63-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14c63-158">Requirements</span></span>



| <span data-ttu-id="14c63-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c63-159">Requirement</span></span> | <span data-ttu-id="14c63-160">Value</span><span class="sxs-lookup"><span data-stu-id="14c63-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14c63-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14c63-161">Minimum supported client</span></span><br/> | <span data-ttu-id="14c63-162">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="14c63-162">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="14c63-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14c63-163">Minimum supported server</span></span><br/> | <span data-ttu-id="14c63-164">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="14c63-164">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="14c63-165">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14c63-165">Minimum supported phone</span></span><br/>  | <span data-ttu-id="14c63-166">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="14c63-166">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14c63-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="14c63-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c63-168">**ID2D1CommandSink1**</span><span class="sxs-lookup"><span data-stu-id="14c63-168">**ID2D1CommandSink1**</span></span>](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

