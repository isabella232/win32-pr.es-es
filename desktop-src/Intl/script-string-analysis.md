---
description: Define algunos o todos los atributos de carácter, glifos, anchos de avance, posiciones x e y, asignaciones de carácter a glifo, etc., para una cadena.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653000"
---
# <a name="script_string_analysis"></a><span data-ttu-id="0709e-103">\_análisis de cadenas de script \_</span><span class="sxs-lookup"><span data-stu-id="0709e-103">SCRIPT\_STRING\_ANALYSIS</span></span>

<span data-ttu-id="0709e-104">Define algunos o todos los atributos de carácter, glifos, anchos de avance, posiciones x e y, asignaciones de carácter a glifo, etc., para una cadena.</span><span class="sxs-lookup"><span data-stu-id="0709e-104">Defines some or all of the character attributes, glyphs, advance widths, x and y positions, character-to-glyph mappings, and so forth, for a string.</span></span>


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a><span data-ttu-id="0709e-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0709e-105">Remarks</span></span>

<span data-ttu-id="0709e-106">Se trata de una estructura opaca que se asigna dinámicamente y se recupera mediante [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span><span class="sxs-lookup"><span data-stu-id="0709e-106">This is an opaque structure that is allocated dynamically and retrieved by [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span></span> <span data-ttu-id="0709e-107">También es necesario para todas las demás funciones \**ScriptString \** _.</span><span class="sxs-lookup"><span data-stu-id="0709e-107">It is required for all other \**ScriptString\** _ functions, as well.</span></span>

<span data-ttu-id="0709e-108">Dado que el análisis puede ser grande, es importante que la aplicación llame a [_ *ScriptStringFree* \*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) en cuanto termine con la cadena.</span><span class="sxs-lookup"><span data-stu-id="0709e-108">Since the analysis can be large, it is important for your application to call [_ *ScriptStringFree*\*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) as soon as it has finished with the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="0709e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0709e-109">Requirements</span></span>



| <span data-ttu-id="0709e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0709e-110">Requirement</span></span> | <span data-ttu-id="0709e-111">Value</span><span class="sxs-lookup"><span data-stu-id="0709e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0709e-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0709e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0709e-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0709e-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0709e-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0709e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0709e-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0709e-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0709e-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0709e-116">Redistributable</span></span><br/>          | <span data-ttu-id="0709e-117">Internet Explorer 5 o posterior Windows Me/98/95</span><span class="sxs-lookup"><span data-stu-id="0709e-117">Internet Explorer 5 or later onWindows Me/98/95</span></span><br/>                         |
| <span data-ttu-id="0709e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0709e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0709e-119"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0709e-119"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0709e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0709e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0709e-121">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="0709e-121">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="0709e-122">Estructuras de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="0709e-122">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="0709e-123">**ScriptStringAnalyse**</span><span class="sxs-lookup"><span data-stu-id="0709e-123">**ScriptStringAnalyse**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[<span data-ttu-id="0709e-124">**ScriptStringFree**</span><span class="sxs-lookup"><span data-stu-id="0709e-124">**ScriptStringFree**</span></span>](script-string-analysis.md)
</dt> </dl>

 

 




