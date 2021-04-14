---
title: IDWriteFactory2 CreateCustomRenderingParams, método
description: Crea un objeto de parámetros de representación con las propiedades especificadas.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Método CreateCustomRenderingParams de escritura directa
- Método CreateCustomRenderingParams de escritura directa, interfaz IDWriteFactory2
- Interfaz IDWriteFactory2 Direct Write, método CreateCustomRenderingParams
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422448"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a><span data-ttu-id="31598-106">IDWriteFactory2:: CreateCustomRenderingParams (método)</span><span class="sxs-lookup"><span data-stu-id="31598-106">IDWriteFactory2::CreateCustomRenderingParams method</span></span>

<span data-ttu-id="31598-107">Crea un objeto de parámetros de representación con las propiedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="31598-107">Creates a rendering parameters object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31598-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31598-108">Syntax</span></span>


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="31598-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31598-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31598-110">*gamma*</span><span class="sxs-lookup"><span data-stu-id="31598-110">*gamma*</span></span> 
</dt> <dd>

<span data-ttu-id="31598-111">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="31598-111">Type: **FLOAT**</span></span>

<span data-ttu-id="31598-112">El valor gamma utilizado para la corrección gamma, que debe ser mayor que cero y no puede superar 256.</span><span class="sxs-lookup"><span data-stu-id="31598-112">The gamma value used for gamma correction, which must be greater than zero and cannot exceed 256.</span></span>

</dd> <dt>

<span data-ttu-id="31598-113">*enhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="31598-113">*enhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="31598-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="31598-114">Type: **FLOAT**</span></span>

<span data-ttu-id="31598-115">La cantidad de mejoras de contraste, cero o más.</span><span class="sxs-lookup"><span data-stu-id="31598-115">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="31598-116">*grayscaleEnhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="31598-116">*grayscaleEnhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="31598-117">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="31598-117">Type: **FLOAT**</span></span>

<span data-ttu-id="31598-118">La cantidad de mejoras de contraste, cero o más.</span><span class="sxs-lookup"><span data-stu-id="31598-118">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="31598-119">*clearTypeLevel*</span><span class="sxs-lookup"><span data-stu-id="31598-119">*clearTypeLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="31598-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="31598-120">Type: **FLOAT**</span></span>

<span data-ttu-id="31598-121">El grado de nivel de ClearType, de 0,0 f (sin ClearType) a 1,0 f (completo ClearType).</span><span class="sxs-lookup"><span data-stu-id="31598-121">The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).</span></span>

</dd> <dt>

<span data-ttu-id="31598-122">*pixelGeometry*</span><span class="sxs-lookup"><span data-stu-id="31598-122">*pixelGeometry*</span></span> 
</dt> <dd>

<span data-ttu-id="31598-123">Tipo: **[ **DWRITE \_ píxel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span><span class="sxs-lookup"><span data-stu-id="31598-123">Type: **[**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span></span>

<span data-ttu-id="31598-124">Geometría de un píxel de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31598-124">The geometry of a device pixel.</span></span>

</dd> <dt>

<span data-ttu-id="31598-125">*renderingMode*</span><span class="sxs-lookup"><span data-stu-id="31598-125">*renderingMode*</span></span> 
</dt> <dd>

<span data-ttu-id="31598-126">Tipo: **[ **\_ \_ modo de representación DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span><span class="sxs-lookup"><span data-stu-id="31598-126">Type: **[**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span></span>

<span data-ttu-id="31598-127">Método de representación de glifos.</span><span class="sxs-lookup"><span data-stu-id="31598-127">Method of rendering glyphs.</span></span> <span data-ttu-id="31598-128">En la mayoría de los casos, debe ser el \_ \_ modo de representación DWRITE \_ predeterminado para usar automáticamente un modo adecuado.</span><span class="sxs-lookup"><span data-stu-id="31598-128">In most cases, this should be DWRITE\_RENDERING\_MODE\_DEFAULT to automatically use an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="31598-129">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="31598-129">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="31598-130">Tipo: **[ **DWRITE \_ \_ \_ modo de ajuste de cuadrícula**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="31598-130">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="31598-131">Cómo ajustar la cuadrícula a los contornos del glifo.</span><span class="sxs-lookup"><span data-stu-id="31598-131">How to grid fit glyph outlines.</span></span> <span data-ttu-id="31598-132">En la mayoría de los casos, debe ser DWRITE \_ cuadrícula de \_ ajuste \_ predeterminada para elegir automáticamente un modo adecuado.</span><span class="sxs-lookup"><span data-stu-id="31598-132">In most cases, this should be DWRITE\_GRID\_FIT\_DEFAULT to automatically choose an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="31598-133">*renderingParams* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31598-133">*renderingParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31598-134">Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span><span class="sxs-lookup"><span data-stu-id="31598-134">Type: **[**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span></span>

<span data-ttu-id="31598-135">Contiene el objeto de parámetros de representación recién creado o NULL en caso de error.</span><span class="sxs-lookup"><span data-stu-id="31598-135">Holds the newly created rendering parameters object, or NULL in case of failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31598-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31598-136">Return value</span></span>

<span data-ttu-id="31598-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="31598-137">Type: **HRESULT**</span></span>

<span data-ttu-id="31598-138">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="31598-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31598-139">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31598-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="31598-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31598-140">Requirements</span></span>



| <span data-ttu-id="31598-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="31598-141">Requirement</span></span> | <span data-ttu-id="31598-142">Value</span><span class="sxs-lookup"><span data-stu-id="31598-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31598-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31598-143">Minimum supported client</span></span><br/> | <span data-ttu-id="31598-144">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="31598-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="31598-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31598-145">Minimum supported server</span></span><br/> | <span data-ttu-id="31598-146">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="31598-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="31598-147">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31598-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="31598-148">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="31598-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="31598-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31598-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="31598-150"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31598-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="31598-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31598-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31598-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31598-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31598-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="31598-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31598-154">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="31598-154">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

