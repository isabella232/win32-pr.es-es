---
title: IDWriteFontFallback MapCharacters, método
description: Determina la fuente adecuada que se va a utilizar para representar el intervalo de texto inicial.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Método MapCharacters de escritura directa
- Método MapCharacters de escritura directa, interfaz IDWriteFontFallback
- Interfaz IDWriteFontFallback Direct Write, método MapCharacters
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359765"
---
# <a name="idwritefontfallbackmapcharacters-method"></a><span data-ttu-id="46f06-106">IDWriteFontFallback:: MapCharacters (método)</span><span class="sxs-lookup"><span data-stu-id="46f06-106">IDWriteFontFallback::MapCharacters method</span></span>

<span data-ttu-id="46f06-107">Determina la fuente adecuada que se va a utilizar para representar el intervalo de texto inicial.</span><span class="sxs-lookup"><span data-stu-id="46f06-107">Determines an appropriate font to use to render the beginning range of text.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f06-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46f06-108">Syntax</span></span>


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a><span data-ttu-id="46f06-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46f06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f06-110">*de origen*</span><span class="sxs-lookup"><span data-stu-id="46f06-110">*source*</span></span> 
</dt> <dd>

<span data-ttu-id="46f06-111">Tipo: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _</span><span class="sxs-lookup"><span data-stu-id="46f06-111">Type: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\** _</span></span>

<span data-ttu-id="46f06-112">La implementación de origen de texto contiene el texto y la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="46f06-112">The text source implementation holds the text and locale.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-113">_textPosition \*</span><span class="sxs-lookup"><span data-stu-id="46f06-113">_textPosition\*</span></span> 
</dt> <dd>

<span data-ttu-id="46f06-114">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="46f06-114">Type: **UINT32**</span></span>

<span data-ttu-id="46f06-115">Posición inicial que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="46f06-115">Starting position to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-116">*textLength*</span><span class="sxs-lookup"><span data-stu-id="46f06-116">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="46f06-117">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="46f06-117">Type: **UINT32**</span></span>

<span data-ttu-id="46f06-118">Longitud del texto que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="46f06-118">Length of the text to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-119">*baseFontCollection* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="46f06-119">*baseFontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46f06-120">Tipo: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _</span><span class="sxs-lookup"><span data-stu-id="46f06-120">Type: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\** _</span></span>

<span data-ttu-id="46f06-121">Colección de fuentes predeterminada que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="46f06-121">Default font collection to use.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-122">_baseFamilyName \* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="46f06-122">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46f06-123">Tipo: \**const WCHAR \_ t \** _</span><span class="sxs-lookup"><span data-stu-id="46f06-123">Type: \**const wchar\_t\** _</span></span>

<span data-ttu-id="46f06-124">Nombre de familia de la fuente base.</span><span class="sxs-lookup"><span data-stu-id="46f06-124">Family name of the base font.</span></span> <span data-ttu-id="46f06-125">Si pasa null, no se realizará ninguna coincidencia con la familia.</span><span class="sxs-lookup"><span data-stu-id="46f06-125">If you pass null, no matching will be done against the family.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-126">_baseWeight \*</span><span class="sxs-lookup"><span data-stu-id="46f06-126">_baseWeight\*</span></span> 
</dt> <dd>

<span data-ttu-id="46f06-127">Tipo: **[ **DWRITE \_ \_ espesor de fuente**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span><span class="sxs-lookup"><span data-stu-id="46f06-127">Type: **[**DWRITE\_FONT\_WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span></span>

<span data-ttu-id="46f06-128">Peso deseado.</span><span class="sxs-lookup"><span data-stu-id="46f06-128">The desired weight.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-129">*baseStyle*</span><span class="sxs-lookup"><span data-stu-id="46f06-129">*baseStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="46f06-130">Tipo: **[ **\_ \_ estilo de fuente DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span><span class="sxs-lookup"><span data-stu-id="46f06-130">Type: **[**DWRITE\_FONT\_STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span></span>

<span data-ttu-id="46f06-131">El estilo deseado.</span><span class="sxs-lookup"><span data-stu-id="46f06-131">The desired style.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-132">*baseStretch*</span><span class="sxs-lookup"><span data-stu-id="46f06-132">*baseStretch*</span></span> 
</dt> <dd>

<span data-ttu-id="46f06-133">Tipo: **[ **DWRITE \_ Font \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span><span class="sxs-lookup"><span data-stu-id="46f06-133">Type: **[**DWRITE\_FONT\_STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span></span>

<span data-ttu-id="46f06-134">Stretch deseado.</span><span class="sxs-lookup"><span data-stu-id="46f06-134">The desired stretch.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-135">*mappedLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46f06-135">*mappedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46f06-136">Tipo: \**UINT32 \** _</span><span class="sxs-lookup"><span data-stu-id="46f06-136">Type: \**UINT32\** _</span></span>

<span data-ttu-id="46f06-137">Longitud de texto asignada a la fuente asignada.</span><span class="sxs-lookup"><span data-stu-id="46f06-137">Length of text mapped to the mapped font.</span></span> <span data-ttu-id="46f06-138">Siempre será menor o igual que la longitud del texto y mayor que cero (si la longitud del texto es distinta de cero), por lo que el autor de la llamada avanza al menos un carácter.</span><span class="sxs-lookup"><span data-stu-id="46f06-138">This will always be less than or equal to the text length and greater than zero (if the text length is non-zero) so the caller advances at least one character.</span></span>

</dd> <dt>

<span data-ttu-id="46f06-139">_mappedFont \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="46f06-139">_mappedFont\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46f06-140">Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span><span class="sxs-lookup"><span data-stu-id="46f06-140">Type: **[**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span></span>

<span data-ttu-id="46f06-141">Fuente que se debe usar para representar los primeros caracteres *mappedLength* del texto.</span><span class="sxs-lookup"><span data-stu-id="46f06-141">The font that should be used to render the first *mappedLength* characters of the text.</span></span> <span data-ttu-id="46f06-142">Si devuelve NULL, significa que ninguna fuente puede representar el texto y *mappedLength* es el número de caracteres que se va a omitir (se representa con un glifo que falta).</span><span class="sxs-lookup"><span data-stu-id="46f06-142">If it returns NULL, that means that no font can render the text, and *mappedLength* is the number of characters to skip (rendered with a missing glyph).</span></span>

</dd> <dt>

<span data-ttu-id="46f06-143">*escala* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46f06-143">*scale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46f06-144">Tipo: \**float \** _</span><span class="sxs-lookup"><span data-stu-id="46f06-144">Type: \**FLOAT\** _</span></span>

<span data-ttu-id="46f06-145">Factor de escala para multiplicar el tamaño em de la fuente devuelta por.</span><span class="sxs-lookup"><span data-stu-id="46f06-145">Scale factor to multiply the em size of the returned font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46f06-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46f06-146">Return value</span></span>

<span data-ttu-id="46f06-147">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="46f06-147">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="46f06-148">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="46f06-148">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46f06-149">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46f06-149">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="46f06-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46f06-150">Requirements</span></span>



| <span data-ttu-id="46f06-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="46f06-151">Requirement</span></span> | <span data-ttu-id="46f06-152">Value</span><span class="sxs-lookup"><span data-stu-id="46f06-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46f06-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f06-153">Minimum supported client</span></span><br/> | <span data-ttu-id="46f06-154">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="46f06-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="46f06-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f06-155">Minimum supported server</span></span><br/> | <span data-ttu-id="46f06-156">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="46f06-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="46f06-157">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f06-157">Minimum supported phone</span></span><br/>  | <span data-ttu-id="46f06-158">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="46f06-158">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="46f06-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46f06-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="46f06-160"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46f06-160"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="46f06-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46f06-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46f06-162"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46f06-162"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46f06-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="46f06-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f06-164">**IDWriteFontFallback**</span><span class="sxs-lookup"><span data-stu-id="46f06-164">**IDWriteFontFallback**</span></span>](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

