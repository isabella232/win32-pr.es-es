---
title: IDWriteFontFace GetGdiCompatibleMetrics, método
description: Obtiene las unidades de diseño y las métricas comunes para el tipo de fuente. Estas métricas se aplican a todos los glifos dentro de un fontface y las usan las aplicaciones para realizar cálculos de diseño.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Método GetGdiCompatibleMetrics de escritura directa
- Método GetGdiCompatibleMetrics de escritura directa, interfaz IDWriteFontFace
- Interfaz IDWriteFontFace Direct Write, método GetGdiCompatibleMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690138"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a><span data-ttu-id="750b8-107">IDWriteFontFace:: GetGdiCompatibleMetrics (método)</span><span class="sxs-lookup"><span data-stu-id="750b8-107">IDWriteFontFace::GetGdiCompatibleMetrics method</span></span>

<span data-ttu-id="750b8-108">Obtiene las unidades de diseño y las métricas comunes para el tipo de fuente.</span><span class="sxs-lookup"><span data-stu-id="750b8-108">Obtains design units and common metrics for the font face.</span></span> <span data-ttu-id="750b8-109">Estas métricas se aplican a todos los glifos dentro de un fontface y las usan las aplicaciones para realizar cálculos de diseño.</span><span class="sxs-lookup"><span data-stu-id="750b8-109">These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="750b8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="750b8-110">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="750b8-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="750b8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750b8-112">*emSize*</span><span class="sxs-lookup"><span data-stu-id="750b8-112">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="750b8-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="750b8-113">Type: **FLOAT**</span></span>

<span data-ttu-id="750b8-114">Tamaño lógico de la fuente en unidades DIP.</span><span class="sxs-lookup"><span data-stu-id="750b8-114">The logical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="750b8-115">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="750b8-115">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="750b8-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="750b8-116">Type: **FLOAT**</span></span>

<span data-ttu-id="750b8-117">Número de píxeles físicos por DIP.</span><span class="sxs-lookup"><span data-stu-id="750b8-117">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="750b8-118">*transformación* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="750b8-118">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="750b8-119">Tipo: **\* [**\_ matriz de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) const**</span><span class="sxs-lookup"><span data-stu-id="750b8-119">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="750b8-120">Transformación opcional que se aplica a los glifos y sus posiciones.</span><span class="sxs-lookup"><span data-stu-id="750b8-120">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="750b8-121">Esta transformación se aplica después del ajuste de escala especificado por el tamaño de fuente y *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="750b8-121">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="750b8-122">*fontFaceMetrics* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="750b8-122">*fontFaceMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="750b8-123">Tipo: **[ **\_ \_ métricas de fuente DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="750b8-123">Type: **[**DWRITE\_FONT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span></span>

<span data-ttu-id="750b8-124">Puntero a una estructura [**de \_ \_ métricas de fuente DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)para rellenar.</span><span class="sxs-lookup"><span data-stu-id="750b8-124">A pointer to a [**DWRITE\_FONT\_METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S structure to fill in.</span></span> <span data-ttu-id="750b8-125">Las métricas devueltas por esta función están en unidades de diseño de fuentes.</span><span class="sxs-lookup"><span data-stu-id="750b8-125">The metrics returned by this function are in font design units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750b8-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="750b8-126">Return value</span></span>

<span data-ttu-id="750b8-127">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="750b8-127">Type: **HRESULT**</span></span>

<span data-ttu-id="750b8-128">Código de error HRESULT estándar.</span><span class="sxs-lookup"><span data-stu-id="750b8-128">Standard HRESULT error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="750b8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="750b8-129">Requirements</span></span>



| <span data-ttu-id="750b8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="750b8-130">Requirement</span></span> | <span data-ttu-id="750b8-131">Value</span><span class="sxs-lookup"><span data-stu-id="750b8-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="750b8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="750b8-132">Library</span></span><br/> | <dl> <span data-ttu-id="750b8-133"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="750b8-133"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="750b8-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="750b8-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="750b8-135"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="750b8-135"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="750b8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="750b8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750b8-137">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="750b8-137">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="750b8-138">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="750b8-138">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

