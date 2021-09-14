---
description: Revise la lista de valores del modo de conversión del editor de métodos de entrada (IME). Estos valores se usan con las funciones ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valores del modo de conversión de IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274580"
---
# <a name="ime-conversion-mode-values"></a>Valores del modo de conversión de IME

Estos valores se usan con las [**funciones ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)



| bit                      | Significado                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| IME \_ CMODE \_ ALPHANUMERIC | Modo de entrada alfanumérico. Este es el valor predeterminado, definido como 0x0000.                          |
| IME \_ CMODE \_ CHARCODE     | Se establece en 1 si el modo de entrada de código de caracteres; 0 si no es así.                                          |
| EUDC \_ de CMODE de IME \_         | Se establece en 1 si el modo de conversión eudc; 0 si no es así.                                               |
| IME \_ CMODE \_ FIXED        | **Windows Me/98, Windows 2000, Windows XP:** Se establece en 1 si el modo de conversión es fijo; 0 si no es así. |
| IME \_ CMODE \_ FULLSHAPE    | Se establece en 1 si el modo de forma completa; 0 si el modo de forma media.                                        |
| IME \_ CMODE \_ HANJACONVERT | Se establece en 1 si el modo de conversión HANJA; 0 si no es así.                                                 |
| IME \_ CMODE \_ KATAKANA     | Se establece en 1 si el modo KATAKANA; 0 si el modo HIRAGANA.                                            |
| IME \_ CMODE \_ NATIVE       | Se establece en 1 si el modo NATIVE; 0 si el modo ALFANUMÉRICO.                                          |
| IME \_ CMODE \_ NOCONVERSION | Establezca en 1 para evitar el procesamiento de conversiones por IME; 0 si no es así.                           |
| IME \_ CMODE \_ ROMAN        | Se establece en 1 si el modo de entrada DE ROMÁN; 0 si no es así.                                                   |
| IME \_ CMODE \_ SOFTKBD      | Se establece en 1 si el modo de teclado suave; 0 si no es así.                                                 |
| SÍMBOLO \_ CMODE de \_ IME       | Se establece en 1 si el modo de conversión SYMBOL; 0 si no es así.                                             |



 

Todos los demás bits están reservados.

 

 



