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
# <a name="recognizercapabilities-enumeration"></a>Enumeración RecognizerCapabilities

Especifica los atributos de un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

## <a name="syntax"></a>Sintaxis


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ ninguno**
</dt> <dd>

No se especificó ninguna funcionalidad.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**
</dt> <dd>

Omite todas las demás marcas que se establecen.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC ( \_ objeto)**
</dt> <dd>

Admite el reconocimiento de objetos; de lo contrario, solo reconoce el texto.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**
</dt> <dd>

Admite la entrada libre, donde la tinta se escribe sin el uso de una guía de reconocimiento, como una línea o un cuadro.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**
</dt> <dd>

Admite la entrada con líneas, que es similar a escribir en papel con líneas.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**
</dt> <dd>

Admite la entrada de conversión boxing, donde cada carácter o palabra se escribe en un cuadro.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**
</dt> <dd>

Admite Autocompletar caracteres. Los reconocedores que admiten la función autocompletar caracteres requieren una entrada de conversión boxing.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**
</dt> <dd>

Admite la entrada de escritura a mano en orden correcto y hacia abajo, como en idiomas occidentales y en algunos idiomas de Asia oriental.

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**
</dt> <dd>

Admite la entrada de escritura a mano en orden izquierdo y hacia abajo, como en los idiomas hebreo y árabe.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**
</dt> <dd>

Admite la entrada de escritura a mano en orden descendente y izquierdo, como en algunos idiomas de Asia oriental.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**
</dt> <dd>

Admite la entrada de escritura a mano en orden descendente y derecho, como en algunos idiomas de Asia oriental.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**
</dt> <dd>

Admite texto escrito en ángulos arbitrarios.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC \_ Lattice**
</dt> <dd>

Permite devolver Lattice como una cadena alternativa para los resultados de reconocimiento de escritura a mano.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**
</dt> <dd>

Admite la interrupción del reconocimiento en segundo plano, como cuando ha cambiado la tinta.

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**
</dt> <dd>

Admite el orden de los trazos, espaciales y temporales, como parte de la operación de reconocimiento. [**IInkAnalyzer**](iinkanalyzer.md) no reordena los trazos antes de enviar la entrada manuscrita al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ personalizable**
</dt> <dd>

Admite escritura a mano personalizada, en la que el reconocedor mejora el reconocimiento cuando se expone a la misma escritura a mano a lo largo del tiempo.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**
</dt> <dd>

La [**IInkAnalyzer**](iinkanalyzer.md) no necesita girar la escritura a mano hasta una orientación horizontal antes de enviar la tinta a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PrefersParagraphBreaking**
</dt> <dd>

El [**IInkAnalyzer**](iinkanalyzer.md) debe enviar párrafos completos de entrada manuscrita al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), lo que permite al **IInkAnalysisRecognizer** realizar el salto de línea y la separación de palabras (o caracteres).

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**
</dt> <dd>

Reconoce solo una palabra o carácter por cada operación de reconocimiento. [**IInkAnalyzer**](iinkanalyzer.md) realiza la segmentación en la escritura a mano y envía un solo segmento cada vez a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración permite una combinación bit a bit de sus valores de miembro. Utilice esta enumeración para buscar un reconocedor de tinta instalado que admita los atributos necesarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




