---
title: IDWriteFactory2 CreateGlyphRunAnalysis, método
description: Crea un objeto de análisis de ejecución de glifos, que encapsula la información utilizada para representar una ejecución de glifo.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Método CreateGlyphRunAnalysis de escritura directa
- Método CreateGlyphRunAnalysis de escritura directa, interfaz IDWriteFactory2
- Interfaz IDWriteFactory2 Direct Write, método CreateGlyphRunAnalysis
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422447"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a><span data-ttu-id="89e93-106">IDWriteFactory2:: CreateGlyphRunAnalysis (método)</span><span class="sxs-lookup"><span data-stu-id="89e93-106">IDWriteFactory2::CreateGlyphRunAnalysis method</span></span>

<span data-ttu-id="89e93-107">Crea un objeto de análisis de ejecución de glifos, que encapsula la información utilizada para representar una ejecución de glifo.</span><span class="sxs-lookup"><span data-stu-id="89e93-107">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e93-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89e93-108">Syntax</span></span>


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="89e93-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89e93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89e93-110">*glyphRun* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89e93-110">*glyphRun* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89e93-111">Tipo: \**\* const [**DWRITE \_ \_ ejecución del glifo**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)* _</span><span class="sxs-lookup"><span data-stu-id="89e93-111">Type: \**const [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)\** _</span></span>

<span data-ttu-id="89e93-112">Estructura que especifica las propiedades de la ejecución del glifo.</span><span class="sxs-lookup"><span data-stu-id="89e93-112">Structure specifying the properties of the glyph run.</span></span>

</dd> <dt>

<span data-ttu-id="89e93-113">_transform \* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="89e93-113">_transform\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89e93-114">Tipo: \**const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _</span><span class="sxs-lookup"><span data-stu-id="89e93-114">Type: \**const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\** _</span></span>

<span data-ttu-id="89e93-115">Transformación opcional aplicada a los glifos y sus posiciones.</span><span class="sxs-lookup"><span data-stu-id="89e93-115">Optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="89e93-116">Esta transformación se aplica después del ajuste de escala especificado por emSize y pixelsPerDip.</span><span class="sxs-lookup"><span data-stu-id="89e93-116">This transform is applied after the scaling specified by the emSize and pixelsPerDip.</span></span>

</dd> <dt>

<span data-ttu-id="89e93-117">_renderingMode \*</span><span class="sxs-lookup"><span data-stu-id="89e93-117">_renderingMode\*</span></span> 
</dt> <dd>

<span data-ttu-id="89e93-118">Tipo: **\_ \_ modo de representación DWRITE**</span><span class="sxs-lookup"><span data-stu-id="89e93-118">Type: **DWRITE\_RENDERING\_MODE**</span></span>

<span data-ttu-id="89e93-119">Especifica el modo de representación, que debe ser uno de los modos de representación de tramas (es decir, no tiene valor predeterminado y no contorno).</span><span class="sxs-lookup"><span data-stu-id="89e93-119">Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default and not outline).</span></span>

</dd> <dt>

<span data-ttu-id="89e93-120">*measuringMode*</span><span class="sxs-lookup"><span data-stu-id="89e93-120">*measuringMode*</span></span> 
</dt> <dd>

<span data-ttu-id="89e93-121">Tipo: **[ **\_ \_ modo de medición DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span><span class="sxs-lookup"><span data-stu-id="89e93-121">Type: **[**DWRITE\_MEASURING\_MODE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span></span>

<span data-ttu-id="89e93-122">Especifica el método para medir glifos.</span><span class="sxs-lookup"><span data-stu-id="89e93-122">Specifies the method to measure glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="89e93-123">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="89e93-123">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="89e93-124">Tipo: **[ **DWRITE \_ \_ \_ modo de ajuste de cuadrícula**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="89e93-124">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="89e93-125">Cómo ajustar el glifo a la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="89e93-125">How to grid-fit glyph outlines.</span></span> <span data-ttu-id="89e93-126">Este no debe ser predeterminado.</span><span class="sxs-lookup"><span data-stu-id="89e93-126">This must be non-default.</span></span>

</dd> <dt>

<span data-ttu-id="89e93-127">*antialiasMode*</span><span class="sxs-lookup"><span data-stu-id="89e93-127">*antialiasMode*</span></span> 
</dt> <dd>

<span data-ttu-id="89e93-128">Tipo: **[ **DWRITE \_ \_ \_ modo de suavizado de texto**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span><span class="sxs-lookup"><span data-stu-id="89e93-128">Type: **[**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span></span>

<span data-ttu-id="89e93-129">Especifica el modo antialias.</span><span class="sxs-lookup"><span data-stu-id="89e93-129">Specifies the antialias mode.</span></span>

</dd> <dt>

<span data-ttu-id="89e93-130">*baselineOriginX*</span><span class="sxs-lookup"><span data-stu-id="89e93-130">*baselineOriginX*</span></span> 
</dt> <dd>

<span data-ttu-id="89e93-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="89e93-131">Type: **FLOAT**</span></span>

<span data-ttu-id="89e93-132">Posición horizontal del origen de la línea base, en DIP.</span><span class="sxs-lookup"><span data-stu-id="89e93-132">Horizontal position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="89e93-133">*baselineOriginY*</span><span class="sxs-lookup"><span data-stu-id="89e93-133">*baselineOriginY*</span></span> 
</dt> <dd>

<span data-ttu-id="89e93-134">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="89e93-134">Type: **FLOAT**</span></span>

<span data-ttu-id="89e93-135">Posición vertical del origen de la línea base, en DIP.</span><span class="sxs-lookup"><span data-stu-id="89e93-135">Vertical position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="89e93-136">*glyphRunAnalysis* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="89e93-136">*glyphRunAnalysis* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89e93-137">Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span><span class="sxs-lookup"><span data-stu-id="89e93-137">Type: **[**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span></span>

<span data-ttu-id="89e93-138">Recibe un puntero al objeto que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="89e93-138">Receives a pointer to the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89e93-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89e93-139">Return value</span></span>

<span data-ttu-id="89e93-140">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89e93-140">Type: **HRESULT**</span></span>

<span data-ttu-id="89e93-141">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="89e93-141">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89e93-142">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89e93-142">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="89e93-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89e93-143">Requirements</span></span>



| <span data-ttu-id="89e93-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="89e93-144">Requirement</span></span> | <span data-ttu-id="89e93-145">Value</span><span class="sxs-lookup"><span data-stu-id="89e93-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89e93-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89e93-146">Minimum supported client</span></span><br/> | <span data-ttu-id="89e93-147">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="89e93-147">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="89e93-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89e93-148">Minimum supported server</span></span><br/> | <span data-ttu-id="89e93-149">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="89e93-149">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="89e93-150">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89e93-150">Minimum supported phone</span></span><br/>  | <span data-ttu-id="89e93-151">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="89e93-151">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="89e93-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89e93-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="89e93-153"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89e93-153"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="89e93-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89e93-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89e93-155"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89e93-155"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="89e93-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="89e93-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e93-157">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="89e93-157">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

