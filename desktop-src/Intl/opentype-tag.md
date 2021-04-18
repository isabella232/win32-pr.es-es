---
description: Define una matriz de 4 bytes que contiene los valores ASCII de 4 8 bits de espacio, A-Z o a-z para identificar las etiquetas de características de fuente, idioma y script OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687192"
---
# <a name="opentype_tag"></a><span data-ttu-id="9ac2e-103">\_etiqueta OPENTYPE</span><span class="sxs-lookup"><span data-stu-id="9ac2e-103">OPENTYPE\_TAG</span></span>

<span data-ttu-id="9ac2e-104">Define una matriz de 4 bytes que contiene los valores ASCII de 4 8 bits de espacio, A-Z o a-z para identificar las etiquetas de características de fuente, idioma y script OpenType.</span><span class="sxs-lookup"><span data-stu-id="9ac2e-104">Defines a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z to identify OpenType script, language, and font feature tags.</span></span>


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a><span data-ttu-id="9ac2e-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ac2e-105">Remarks</span></span>

<span data-ttu-id="9ac2e-106">En los siguientes ejemplos se definen representaciones de etiquetas de características OpenType.</span><span class="sxs-lookup"><span data-stu-id="9ac2e-106">The following examples define representations of OpenType feature tags.</span></span>

-   <span data-ttu-id="9ac2e-107">La etiqueta de característica de la característica de ligadura es "Liga".</span><span class="sxs-lookup"><span data-stu-id="9ac2e-107">The feature tag for the ligature feature is "liga".</span></span>
-   <span data-ttu-id="9ac2e-108">Las etiquetas de idioma para rumano, urdu y persa son "ROM", "URD" y "FAR", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9ac2e-108">The language tags for Romanian, Urdu, and Persian are "ROM ", "URD ", and "FAR ", respectively.</span></span> <span data-ttu-id="9ac2e-109">Tenga en cuenta que cada una de estas etiquetas finaliza con un espacio.</span><span class="sxs-lookup"><span data-stu-id="9ac2e-109">Note that each of these tags ends with a space.</span></span>
-   <span data-ttu-id="9ac2e-110">Las etiquetas de script para los scripts latinos y árabes son "latn" y "árabe", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9ac2e-110">The script tags for Latin and Arabic scripts are "latn" and "arab", respectively.</span></span>

<span data-ttu-id="9ac2e-111">Para obtener más información sobre las etiquetas de las características OpenType y la especificación OpenType, vea <https://www.microsoft.com/typography/otspec/featuretags.htm> .</span><span class="sxs-lookup"><span data-stu-id="9ac2e-111">For more information on OpenType feature tags and the OpenType specification, see <https://www.microsoft.com/typography/otspec/featuretags.htm>.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac2e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ac2e-112">Requirements</span></span>



| <span data-ttu-id="9ac2e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ac2e-113">Requirement</span></span> | <span data-ttu-id="9ac2e-114">Value</span><span class="sxs-lookup"><span data-stu-id="9ac2e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac2e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ac2e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac2e-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ac2e-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9ac2e-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ac2e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac2e-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ac2e-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9ac2e-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9ac2e-119">Redistributable</span></span><br/>          | <span data-ttu-id="9ac2e-120">Usp10.dll la versión 1,600 o superior de la ventana de Windows más adelante</span><span class="sxs-lookup"><span data-stu-id="9ac2e-120">Usp10.dll version 1.600 or greater onWindows XPand later</span></span><br/>                |
| <span data-ttu-id="9ac2e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ac2e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ac2e-122"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ac2e-122"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac2e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ac2e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac2e-124">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="9ac2e-124">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="9ac2e-125">Estructuras de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="9ac2e-125">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="9ac2e-126">**ScriptGetFontAlternateGlyphs**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-126">**ScriptGetFontAlternateGlyphs**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[<span data-ttu-id="9ac2e-127">**ScriptGetFontFeatureTags**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-127">**ScriptGetFontFeatureTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[<span data-ttu-id="9ac2e-128">**ScriptGetFontLanguageTags**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-128">**ScriptGetFontLanguageTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[<span data-ttu-id="9ac2e-129">**ScriptGetFontScriptTags**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-129">**ScriptGetFontScriptTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[<span data-ttu-id="9ac2e-130">**ScriptItemizeOpenType**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-130">**ScriptItemizeOpenType**</span></span>](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[<span data-ttu-id="9ac2e-131">**ScriptPlaceOpenType**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-131">**ScriptPlaceOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[<span data-ttu-id="9ac2e-132">**ScriptPositionSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-132">**ScriptPositionSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[<span data-ttu-id="9ac2e-133">**ScriptShapeOpenType**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-133">**ScriptShapeOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[<span data-ttu-id="9ac2e-134">**ScriptSubstituteSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="9ac2e-134">**ScriptSubstituteSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




