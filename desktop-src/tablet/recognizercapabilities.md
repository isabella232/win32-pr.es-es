---
description: Especifica los atributos de un IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Enumeración RecognizerCapabilities (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467155"
---
# <a name="recognizercapabilities-enumeration"></a>Enumeración RecognizerCapabilities

Especifica los atributos de un [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

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

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ None**
</dt> <dd>

No se especifica ninguna funcionalidad.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**
</dt> <dd>

Omite todas las demás marcas establecidas.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC \_ (objeto)**
</dt> <dd>

Admite el reconocimiento de objetos; de lo contrario, solo reconoce texto.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**
</dt> <dd>

Admite entrada libre, donde se introduce la entrada de lápiz sin el uso de una guía de reconocimiento, como una línea o un cuadro.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**
</dt> <dd>

Admite entradas alineadas, que es similar a escribir en papel forrado.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**
</dt> <dd>

Admite la entrada con caja, donde cada carácter o palabra se introduce en un cuadro.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**
</dt> <dd>

Admite el carácter Autocompletar. Los reconocedores que admiten el carácter Autocompletar requieren entrada con formato boxed.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**
</dt> <dd>

Admite la entrada de escritura a mano en orden correcto y descendente, como en idiomas del oeste y algunos idiomas de Asia Oriental.

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**
</dt> <dd>

Admite la entrada de escritura a mano en orden izquierdo y descendente, como en idiomas hebreo y árabe.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**
</dt> <dd>

Admite la escritura a mano de entradas en orden hacia abajo y a la izquierda, como en algunos idiomas de Este de Asia.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**
</dt> <dd>

Admite la entrada de escritura a mano en orden descendente y correcto, como en algunos idiomas de Asia Oriental.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**
</dt> <dd>

Admite texto escrito en ángulos arbitrarios.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC \_ Lattice**
</dt> <dd>

Admite la devolución de un entramado como una cadena alternativa para los resultados del reconocimiento de escritura a mano.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**
</dt> <dd>

Admite la interrupción del reconocimiento de fondo, como cuando ha cambiado la entrada de lápiz.

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**
</dt> <dd>

Admite que el orden del trazo, espacial y temporal, se controla como parte de la operación de reconocimiento. [**IInkAnalyzer no**](iinkanalyzer.md) reordena los trazos antes de enviar la entrada de lápiz a [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ Personalizable**
</dt> <dd>

Admite escritura a mano personalizada, donde el reconocedor mejora el reconocimiento cuando se expone a la misma escritura a mano a lo largo del tiempo.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**
</dt> <dd>

[**IInkAnalyzer no**](iinkanalyzer.md) necesita girar la escritura a mano a una orientación horizontal antes de enviar la entrada de lápiz a [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PrefersParagraphBreaking**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) debe enviar párrafos completos de lápiz al [**IInkAnalysisRecognizer,**](iinkanalysisrecognizer.md)lo que permite al **IInkAnalysisRecognizer** realizar la separación de línea y la separación de palabras (o caracteres).

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**
</dt> <dd>

Reconoce solo una palabra o carácter por operación de reconocimiento. [**IInkAnalyzer**](iinkanalyzer.md) realiza la segmentación en la escritura a mano y envía solo un segmento a la vez al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración permite una combinación bit a bit de sus valores de miembro. Use esta enumeración para buscar un reconocedor de lápiz instalado que admita los atributos que necesita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




