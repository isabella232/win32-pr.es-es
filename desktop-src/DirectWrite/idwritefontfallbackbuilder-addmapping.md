---
title: IDWriteFontFallbackBuilder AddMapping, método
description: Anexa una única asignación a la lista. Llame a este método una vez por cada asignación adicional.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Método AddMapping de escritura directa
- Método AddMapping de escritura directa, interfaz IDWriteFontFallbackBuilder
- Interfaz IDWriteFontFallbackBuilder Direct Write, método AddMapping
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422444"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a><span data-ttu-id="3f3c9-107">IDWriteFontFallbackBuilder:: AddMapping (método)</span><span class="sxs-lookup"><span data-stu-id="3f3c9-107">IDWriteFontFallbackBuilder::AddMapping method</span></span>

<span data-ttu-id="3f3c9-108">Anexa una única asignación a la lista.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-108">Appends a single mapping to the list.</span></span> <span data-ttu-id="3f3c9-109">Llame a este método una vez por cada asignación adicional.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-109">Call this once for each additional mapping.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3c9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f3c9-110">Syntax</span></span>


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a><span data-ttu-id="3f3c9-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f3c9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f3c9-112">*alcance*</span><span class="sxs-lookup"><span data-stu-id="3f3c9-112">*ranges*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3c9-113">Tipo: \**\* [**DWRITE \_ \_ intervalo Unicode**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)* _</span><span class="sxs-lookup"><span data-stu-id="3f3c9-113">Type: \**[**DWRITE\_UNICODE\_RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\** _</span></span>

<span data-ttu-id="3f3c9-114">Intervalos Unicode que se aplican a esta asignación.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-114">Unicode ranges that apply to this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="3f3c9-115">_rangesCount \*</span><span class="sxs-lookup"><span data-stu-id="3f3c9-115">_rangesCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3c9-116">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3f3c9-116">Type: **UINT32**</span></span>

<span data-ttu-id="3f3c9-117">Número de intervalos Unicode.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-117">Number of Unicode ranges.</span></span>

</dd> <dt>

<span data-ttu-id="3f3c9-118">*targetFamilyNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f3c9-118">*targetFamilyNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3c9-119">Tipo: **const WCHAR \* \***</span><span class="sxs-lookup"><span data-stu-id="3f3c9-119">Type: **const WCHAR\*\***</span></span>

<span data-ttu-id="3f3c9-120">Lista de cadenas de nombre de familia de destino.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-120">List of target family name strings.</span></span>

</dd> <dt>

<span data-ttu-id="3f3c9-121">*targetFamilyNamesCount*</span><span class="sxs-lookup"><span data-stu-id="3f3c9-121">*targetFamilyNamesCount*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3c9-122">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3f3c9-122">Type: **UINT32**</span></span>

<span data-ttu-id="3f3c9-123">Número de nombres de familia de destino.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-123">Number of target family names.</span></span>

</dd> <dt>

<span data-ttu-id="3f3c9-124">*fontCollection* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3f3c9-124">*fontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3c9-125">Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span><span class="sxs-lookup"><span data-stu-id="3f3c9-125">Type: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span></span>

<span data-ttu-id="3f3c9-126">Colección de fuentes explícitas opcional para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-126">Optional explicit font collection for this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="3f3c9-127">*localeName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3f3c9-127">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3c9-128">Tipo: \**const WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="3f3c9-128">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="3f3c9-129">Configuración regional del contexto.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-129">Locale of the context.</span></span>

</dd> <dt>

<span data-ttu-id="3f3c9-130">_baseFamilyName \* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3f3c9-130">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3c9-131">Tipo: \**const WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="3f3c9-131">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="3f3c9-132">Nombre de familia base con el que coincidir, si procede.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-132">Base family name to match against, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="3f3c9-133">_scale \*</span><span class="sxs-lookup"><span data-stu-id="3f3c9-133">_scale\*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3c9-134">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3f3c9-134">Type: **FLOAT**</span></span>

<span data-ttu-id="3f3c9-135">Factor de escala para multiplicar la fuente de destino del resultado por.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-135">Scale factor to multiply the result target font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f3c9-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f3c9-136">Return value</span></span>

<span data-ttu-id="3f3c9-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3f3c9-137">Type: **HRESULT**</span></span>

<span data-ttu-id="3f3c9-138">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3f3c9-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f3c9-139">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f3c9-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f3c9-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f3c9-140">Requirements</span></span>



| <span data-ttu-id="3f3c9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f3c9-141">Requirement</span></span> | <span data-ttu-id="3f3c9-142">Value</span><span class="sxs-lookup"><span data-stu-id="3f3c9-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3c9-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f3c9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3c9-144">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="3f3c9-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="3f3c9-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f3c9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3c9-146">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3f3c9-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="3f3c9-147">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f3c9-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="3f3c9-148">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="3f3c9-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="3f3c9-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f3c9-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f3c9-150"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f3c9-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3f3c9-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f3c9-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f3c9-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f3c9-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f3c9-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f3c9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3c9-154">**IDWriteFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="3f3c9-154">**IDWriteFontFallbackBuilder**</span></span>](idwritefontfallbackbuilder.md)
</dt> </dl>

 

