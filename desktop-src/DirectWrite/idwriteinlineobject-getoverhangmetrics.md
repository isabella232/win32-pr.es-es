---
title: IDWriteInlineObject GetOverhangMetrics, método
description: IDWriteTextLayout llama a esta función de devolución de llamada para obtener las extensiones visibles (en DIP) del objeto insertado. En el caso de un mapa de bits simple, sin relleno y sin voladizo, todos los sobrebloqueos serán simplemente ceros.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Método GetOverhangMetrics de escritura directa
- Método GetOverhangMetrics de escritura directa, interfaz IDWriteInlineObject
- Interfaz IDWriteInlineObject Direct Write, método GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671208"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a><span data-ttu-id="85def-107">IDWriteInlineObject:: GetOverhangMetrics (método)</span><span class="sxs-lookup"><span data-stu-id="85def-107">IDWriteInlineObject::GetOverhangMetrics method</span></span>

<span data-ttu-id="85def-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llama a esta función de devolución de llamada para obtener las extensiones visibles (en DIP) del objeto insertado.</span><span class="sxs-lookup"><span data-stu-id="85def-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the visible extents (in DIPs) of the inline object.</span></span> <span data-ttu-id="85def-109">En el caso de un mapa de bits simple, sin relleno y sin voladizo, todos los sobrebloqueos serán simplemente ceros.</span><span class="sxs-lookup"><span data-stu-id="85def-109">In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.</span></span>

<span data-ttu-id="85def-110">Los sobrebloqueos deben devolverse en relación con el tamaño del objeto indicado (vea [**DWRITE \_ en \_ línea \_ métricas de objeto**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) y no deben ajustarse a la línea base.</span><span class="sxs-lookup"><span data-stu-id="85def-110">The overhangs should be returned relative to the reported size of the object (see [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)), and should not be baseline adjusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="85def-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85def-111">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="85def-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85def-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85def-113">*sobrebloqueos* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="85def-113">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85def-114">Tipo: **[ **\_ \_ métricas salientes de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="85def-114">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="85def-115">Exceso de extensiones visibles (en DIP) fuera del objeto.</span><span class="sxs-lookup"><span data-stu-id="85def-115">Overshoot of visible extents (in DIPs) outside the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85def-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85def-116">Return value</span></span>

<span data-ttu-id="85def-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="85def-117">Type: **HRESULT**</span></span>

<span data-ttu-id="85def-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="85def-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85def-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85def-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="85def-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85def-120">Requirements</span></span>



| <span data-ttu-id="85def-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="85def-121">Requirement</span></span> | <span data-ttu-id="85def-122">Value</span><span class="sxs-lookup"><span data-stu-id="85def-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85def-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85def-123">Library</span></span><br/> | <dl> <span data-ttu-id="85def-124"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85def-124"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="85def-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85def-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="85def-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85def-126"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85def-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="85def-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85def-128">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="85def-128">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[<span data-ttu-id="85def-129">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="85def-129">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

