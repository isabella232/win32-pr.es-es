---
description: Estos valores se usan con las funciones ImmGetConversionStatus y ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valores del modo de conversión IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154585"
---
# <a name="ime-conversion-mode-values"></a>Valores del modo de conversión IME

Estos valores se usan con las funciones [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) y [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .



| bit                      | Significado                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| CMODE de IME \_ \_ alfanumérica | Modo de entrada alfanumérico. Este es el valor predeterminado, definido como 0x0000.                          |
| CMODE de IME \_ \_     | Se establece en 1 si el modo de entrada del código de carácter; 0 si no es así.                                          |
| CMODE de IME \_ \_         | Se establece en 1 si el modo de conversión de EUDC; 0 si no es así.                                               |
| IME \_ CMODE \_ corregido        | **Windows Me/98, windows 2000 y Windows XP:** Se establece en 1 si el modo de conversión es fijo; 0 si no es así. |
| IME \_ CMODE \_ FULLSHAPE    | Se establece en 1 si el modo de forma completa; 0 si el modo de mitad de la forma.                                        |
| IME \_ CMODE \_ HANJACONVERT | Se establece en 1 si el modo de conversión HANJA; 0 si no es así.                                                 |
| \_CMODE \_ katakana de IME     | Se establece en 1 si el modo KATAKANA; 0 si el modo es HIRAGANA.                                            |
| IME \_ CMODE \_ nativo       | Se establece en 1 si el modo nativo; 0 si el modo es alfanumérico.                                          |
| CMODE de IME \_ \_ | Se establece en 1 para evitar el procesamiento de conversiones por parte de IME; 0 si no es así.                           |
| IME \_ CMODE \_ Roman        | Se establece en 1 si el modo de entrada ROMAN; 0 si no es así.                                                   |
| IME \_ CMODE \_ SOFTKBD      | Se establece en 1 si el modo de teclado en pantalla; 0 si no es así.                                                 |
| \_símbolo CMODE de IME \_       | Se establece en 1 si el modo de conversión de símbolos; 0 si no es así.                                             |



 

Todos los demás bits están reservados.

 

 



