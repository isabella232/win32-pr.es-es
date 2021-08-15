---
title: Marcas para el modo de conversión (Ctffunc.h)
description: Las marcas siguientes se usan como un valor de GUID \_ COMPARTMENT \_ KEYBOARD \_ INPUTMODE \_ CONVERSION. Esto equivale a los valores \_ CMODE de IME para IMM32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Marcas para el modo de conversión Text Services Framework
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c8c3a452e3115e66e4f0f6e75999cad9bce7e1eadf14b4cadd24fae640a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879221"
---
# <a name="flags-for-conversion-mode"></a>Marcas para el modo de conversión

Las marcas siguientes se usan como un valor de [GUID \_ COMPARTMENT KEYBOARD \_ \_ INPUTMODE \_ CONVERSION](predefined-compartments.md). Esto equivale a los [valores \_ CMODE de IME](../intl/ime-conversion-mode-values.md) para IMM32.



| Marca                             | Value  | Descripción                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| TF \_ CONVERSIONMODE \_ ALPHANUMERIC | 0x0000 | Se establece en 1 si el modo ALFANUMERIC.                                  |
| TF \_ CONVERSIONMODE \_ NATIVE       | 0x0001 | Se establece en 1 si el modo NATIVE; 0 si el modo ALFANUMERIC.                |
| TF \_ CONVERSIONMODE \_ KATAKANA     | 0x0002 | Se establece en 1 si el modo KATAKANA; 0 si el modo HIRAGANA.                  |
| TF \_ CONVERSIONMODE \_ FULLSHAPE    | 0x0008 | Se establece en 1 si el modo de forma completa; 0 si el modo de forma media.              |
| TF \_ CONVERSIONMODE \_ ROMAN        | 0x0010 | Establezca en 1 para evitar el procesamiento de conversiones por IME; 0 si no es así. |
| TF \_ CONVERSIONMODE \_ CHARCODE     | 0x0020 | Se establece en 1 si el modo de entrada de código de caracteres; 0 si no es así.                |
| \_SOFTKEYBOARD DE TF CONVERSIONMODE \_ | 0x0080 | Se establece en 1 si el modo de teclado flexible; 0 si no es así.                       |
| TF \_ CONVERSIONMODE \_ NOCONVERSION | 0x0100 | Establezca en 1 para evitar el procesamiento de conversiones por IME; 0 si no es así. |
| SÍMBOLO \_ CONVERSIONMODE DE \_ TF       | 0x0400 | Se establece en 1 si el modo de conversión SYMBOL; 0 si no es así.                   |
| TF \_ CONVERSIONMODE \_ FIXED        | 0x0800 | Se establece en 1 si el modo de conversión es fijo; 0 si no es así.                    |



 

Los valores siguientes se usan como un valor de [GUID \_ COMPARTMENT KEYBOARD \_ \_ INPUTMODE \_ SENTENCE](predefined-compartments.md). Esto es equivalente a los [valores \_ SMODE de IME](../intl/ime-composition-string-values.md) para IMM32.



| Marca                            | Value  | Descripción                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ SENTENCEMODE \_ NONE          | 0x0000 | No hay información para la oración.                                               |
| TF \_ SENTENCEMODE \_ PLAURALCLAUSE | 0x0001 | El IME usa información de cláusula plural para llevar a cabo el procesamiento de conversión. |
| TF \_ SENTENCEMODE \_ SINGLECONVERT | 0x0002 | El IME lleva a cabo el procesamiento de conversión en modo de un solo carácter.        |
| TF \_ SENTENCEMODE \_ AUTOMATIC     | 0x0004 | El IME lleva a cabo el procesamiento de conversión en modo automático.               |
| TF \_ SENTENCEMODE \_ PHRASEPREDICT | 0x0008 | El IME usa información de frases para predecir el carácter siguiente.             |
| TF \_ SENTENCEMODE \_ CONVERSATION  | 0x0010 | El IME usa el modo de conversación. Esto es útil para las aplicaciones de chat.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| Header<br/>                   | <dl> <dt>Ctffunc.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctffunc.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compartimientos predefinidos](predefined-compartments.md)
</dt> </dl>

 

