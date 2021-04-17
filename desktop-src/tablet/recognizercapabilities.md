---
description: Especifica los atributos de un IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Enumeración RecognizerCapabilities (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706504"
---
# <a name="recognizercapabilities-enumeration"></a><span data-ttu-id="6edc0-103">Enumeración RecognizerCapabilities</span><span class="sxs-lookup"><span data-stu-id="6edc0-103">RecognizerCapabilities enumeration</span></span>

<span data-ttu-id="6edc0-104">Especifica los atributos de un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="6edc0-104">Specifies the attributes of an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6edc0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6edc0-105">Syntax</span></span>


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a><span data-ttu-id="6edc0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6edc0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6edc0-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="6edc0-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC\_None**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-108">No se especificó ninguna funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="6edc0-108">No capabilities specified.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**</span><span class="sxs-lookup"><span data-stu-id="6edc0-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC\_DoNotCare**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-110">Omite todas las demás marcas que se establecen.</span><span class="sxs-lookup"><span data-stu-id="6edc0-110">Ignores all other flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="6edc0-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC\_Object**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-112">Admite el reconocimiento de objetos; de lo contrario, solo reconoce el texto.</span><span class="sxs-lookup"><span data-stu-id="6edc0-112">Supports object recognition; otherwise, recognizes only text.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**</span><span class="sxs-lookup"><span data-stu-id="6edc0-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC\_FreeInput**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-114">Admite la entrada libre, donde la tinta se escribe sin el uso de una guía de reconocimiento, como una línea o un cuadro.</span><span class="sxs-lookup"><span data-stu-id="6edc0-114">Supports free input, where ink is entered without the use of a recognition guide, such as a line or a box.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**</span><span class="sxs-lookup"><span data-stu-id="6edc0-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC\_LinedInput**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-116">Admite la entrada con líneas, que es similar a escribir en papel con líneas.</span><span class="sxs-lookup"><span data-stu-id="6edc0-116">Supports lined input, which is similar to writing on lined paper.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**</span><span class="sxs-lookup"><span data-stu-id="6edc0-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC\_BoxedInput**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-118">Admite la entrada de conversión boxing, donde cada carácter o palabra se escribe en un cuadro.</span><span class="sxs-lookup"><span data-stu-id="6edc0-118">Supports boxed input, where each character or word is entered in a box.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**</span><span class="sxs-lookup"><span data-stu-id="6edc0-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC\_CharacterAutoCompletionInput**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-120">Admite Autocompletar caracteres.</span><span class="sxs-lookup"><span data-stu-id="6edc0-120">Supports character Autocomplete.</span></span> <span data-ttu-id="6edc0-121">Los reconocedores que admiten la función autocompletar caracteres requieren una entrada de conversión boxing.</span><span class="sxs-lookup"><span data-stu-id="6edc0-121">Recognizers that support character Autocomplete require boxed input.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**</span><span class="sxs-lookup"><span data-stu-id="6edc0-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC\_RightAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-123">Admite la entrada de escritura a mano en orden correcto y hacia abajo, como en idiomas occidentales y en algunos idiomas de Asia oriental.</span><span class="sxs-lookup"><span data-stu-id="6edc0-123">Supports handwriting input in right and down order, such as in western languages and some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**</span><span class="sxs-lookup"><span data-stu-id="6edc0-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC\_LeftAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-125">Admite la entrada de escritura a mano en orden izquierdo y hacia abajo, como en los idiomas hebreo y árabe.</span><span class="sxs-lookup"><span data-stu-id="6edc0-125">Supports handwriting input in left and down order, such as in Hebrew and Arabic languages.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**</span><span class="sxs-lookup"><span data-stu-id="6edc0-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC\_DownAndLeft**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-127">Admite la entrada de escritura a mano en orden descendente y izquierdo, como en algunos idiomas de Asia oriental.</span><span class="sxs-lookup"><span data-stu-id="6edc0-127">Supports handwriting input in down and left order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**</span><span class="sxs-lookup"><span data-stu-id="6edc0-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC\_DownAndRight**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-129">Admite la entrada de escritura a mano en orden descendente y derecho, como en algunos idiomas de Asia oriental.</span><span class="sxs-lookup"><span data-stu-id="6edc0-129">Supports handwriting input in down and right order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**</span><span class="sxs-lookup"><span data-stu-id="6edc0-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC\_ArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-131">Admite texto escrito en ángulos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="6edc0-131">Supports text written at arbitrary angles.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC \_ Lattice**</span><span class="sxs-lookup"><span data-stu-id="6edc0-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC\_Lattice**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-133">Permite devolver Lattice como una cadena alternativa para los resultados de reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="6edc0-133">Supports returning a lattice as an alternative a string for handwriting recognition results.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**</span><span class="sxs-lookup"><span data-stu-id="6edc0-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC\_AdviseInkChange**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-135">Admite la interrupción del reconocimiento en segundo plano, como cuando ha cambiado la tinta.</span><span class="sxs-lookup"><span data-stu-id="6edc0-135">Supports interrupting background recognition, such as when the ink has changed.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**</span><span class="sxs-lookup"><span data-stu-id="6edc0-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC\_StrokeReorder**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-137">Admite el orden de los trazos, espaciales y temporales, como parte de la operación de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="6edc0-137">Supports that stroke order, spatial and temporal, is handled as part of the recognition operation.</span></span> <span data-ttu-id="6edc0-138">[**IInkAnalyzer**](iinkanalyzer.md) no reordena los trazos antes de enviar la entrada manuscrita al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="6edc0-138">The [**IInkAnalyzer**](iinkanalyzer.md) does not reorder strokes before sending ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ personalizable**</span><span class="sxs-lookup"><span data-stu-id="6edc0-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC\_Personalizable**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-140">Admite escritura a mano personalizada, en la que el reconocedor mejora el reconocimiento cuando se expone a la misma escritura a mano a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="6edc0-140">Supports personalized handwriting, where the recognizer improves recognition when exposed to the same handwriting over time.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**</span><span class="sxs-lookup"><span data-stu-id="6edc0-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC\_PrefersArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-142">La [**IInkAnalyzer**](iinkanalyzer.md) no necesita girar la escritura a mano hasta una orientación horizontal antes de enviar la tinta a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="6edc0-142">The [**IInkAnalyzer**](iinkanalyzer.md) need not rotate the handwriting to a horizontal orientation before sending the ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PrefersParagraphBreaking**</span><span class="sxs-lookup"><span data-stu-id="6edc0-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC\_PrefersParagraphBreaking**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-144">El [**IInkAnalyzer**](iinkanalyzer.md) debe enviar párrafos completos de entrada manuscrita al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), lo que permite al **IInkAnalysisRecognizer** realizar el salto de línea y la separación de palabras (o caracteres).</span><span class="sxs-lookup"><span data-stu-id="6edc0-144">The [**IInkAnalyzer**](iinkanalyzer.md) should send entire paragraphs of ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), allowing the **IInkAnalysisRecognizer** to do the line breaking and word (or character) breaking.</span></span>

</dd> <dt>

<span data-ttu-id="6edc0-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**</span><span class="sxs-lookup"><span data-stu-id="6edc0-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC\_PrefersSegmentationRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="6edc0-146">Reconoce solo una palabra o carácter por cada operación de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="6edc0-146">Recognizes only one word or character per recognition operation.</span></span> <span data-ttu-id="6edc0-147">[**IInkAnalyzer**](iinkanalyzer.md) realiza la segmentación en la escritura a mano y envía un solo segmento cada vez a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="6edc0-147">The [**IInkAnalyzer**](iinkanalyzer.md) performs segmentation on the handwriting and sends only one segment at a time to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6edc0-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6edc0-148">Remarks</span></span>

<span data-ttu-id="6edc0-149">Esta enumeración permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="6edc0-149">This enumeration allows a bitwise combination of its member values.</span></span> <span data-ttu-id="6edc0-150">Utilice esta enumeración para buscar un reconocedor de tinta instalado que admita los atributos necesarios.</span><span class="sxs-lookup"><span data-stu-id="6edc0-150">Use this enumeration to find an installed ink recognizer that supports the attributes you need.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edc0-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6edc0-151">Requirements</span></span>



| <span data-ttu-id="6edc0-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="6edc0-152">Requirement</span></span> | <span data-ttu-id="6edc0-153">Value</span><span class="sxs-lookup"><span data-stu-id="6edc0-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6edc0-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6edc0-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6edc0-155">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6edc0-155">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6edc0-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6edc0-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6edc0-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6edc0-157">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6edc0-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6edc0-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="6edc0-159"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6edc0-159"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6edc0-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="6edc0-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edc0-161">**IInkAnalysisRecognizer::GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6edc0-161">**IInkAnalysisRecognizer::GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[<span data-ttu-id="6edc0-162">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="6edc0-162">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




