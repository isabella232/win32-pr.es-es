---
title: Marcas para el modo de conversión (Ctffunc. h)
description: Las marcas siguientes se usan como un valor de conversión de INPUTMODE de teclado del compartimiento de GUID \_ \_ \_ \_ . Esto es equivalente a \_ los valores de CMODE de IME para IMM32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Marcas para el marco de trabajo de servicios de texto en modo de conversión
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
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150433"
---
# <a name="flags-for-conversion-mode"></a>Marcas para el modo de conversión

Las marcas siguientes se usan como un valor de [ \_ conversión de \_ \_ INPUTMODE \_ de teclado del compartimiento de GUID](predefined-compartments.md). Esto es equivalente a los valores de [ \_ CMODE de IME](../intl/ime-conversion-mode-values.md) para IMM32.



| Marca                             | Value  | Descripción                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| TF \_ CONVERSIONMODE \_ alfanumérico | 0x0000 | Se establece en 1 si el modo alfanumérico.                                  |
| TF \_ CONVERSIONMODE \_ Native       | 0x0001 | Se establece en 1 si el modo nativo; 0 si el modo es alfanumérico.                |
| TF \_ CONVERSIONMODE \_ katakana     | 0x0002 | Se establece en 1 si el modo KATAKANA; 0 si el modo es HIRAGANA.                  |
| TF \_ CONVERSIONMODE \_ FULLSHAPE    | 0x0008 | Se establece en 1 si el modo de forma completa; 0 si el modo de mitad de la forma.              |
| TF \_ CONVERSIONMODE \_ Roman        | 0x0010 | Se establece en 1 para evitar el procesamiento de conversiones por parte de IME; 0 si no es así. |
| \_CONVERSIONMODE \_ CódCar     | 0x0020 | Se establece en 1 si el modo de entrada del código de carácter; 0 si no es así.                |
| TF \_ CONVERSIONMODE \_ SOFTKEYBOARD | 0x0080 | Se establece en 1 si el modo de teclado en pantalla; 0 si no es así.                       |
| TF \_ CONVERSIONMODE \_ Conversion | 0x0100 | Se establece en 1 para evitar el procesamiento de conversiones por parte de IME; 0 si no es así. |
| símbolo de TF \_ CONVERSIONMODE \_       | 0x0400 | Se establece en 1 si el modo de conversión de símbolos; 0 si no es así.                   |
| TF \_ CONVERSIONMODE \_ fixed        | 0x0800 | Se establece en 1 si el modo de conversión es fijo; 0 si no es así.                    |



 

Los valores siguientes se usan como un valor de [ \_ INPUTMODE de \_ teclado \_ \_ de compartimiento de GUID](predefined-compartments.md). Esto es equivalente a los valores de [ \_ SMODE de IME](../intl/ime-composition-string-values.md) para IMM32.



| Marca                            | Value  | Descripción                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ SENTENCEMODE \_ ninguno          | 0x0000 | No hay información para la frase.                                               |
| TF \_ SENTENCEMODE \_ PLAURALCLAUSE | 0x0001 | El IME usa la información de la cláusula plural para llevar a cabo el procesamiento de la conversión. |
| TF \_ SENTENCEMODE \_ SINGLECONVERT | 0x0002 | El IME realiza el procesamiento de la conversión en el modo de un solo carácter.        |
| TF \_ SENTENCEMODE \_ Automatic     | 0x0004 | El IME realiza el procesamiento de la conversión en modo automático.               |
| TF \_ SENTENCEMODE \_ PHRASEPREDICT | 0x0008 | El IME usa la información de frases para predecir el siguiente carácter.             |
| TF \_ SENTENCEMODE \_ Conversation  | 0x0010 | El IME usa el modo de conversación. Esto resulta útil para las aplicaciones de chat.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 Windows NT 4.0, Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| Encabezado<br/>                   | <dl> <dt>Ctffunc. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compartimientos predefinidos](predefined-compartments.md)
</dt> </dl>

 

