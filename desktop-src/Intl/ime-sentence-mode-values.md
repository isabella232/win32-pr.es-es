---
description: Revise la lista de valores de modo de oración del editor de métodos de entrada (IME). Estos valores se usan con las funciones ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores del modo de oración de IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c471282ebf50657b45f7c1c22938b27fff5a62c08c48ab4191dd84048a4b6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146134"
---
# <a name="ime-sentence-mode-values"></a>Valores del modo de oración de IME

Estos valores se usan con las funciones [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)



| Constante                  | Definición                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| IME \_ SMODE \_ AUTOMATIC     | El IME lleva a cabo el procesamiento de conversión en modo automático.               |
| IME \_ SMODE \_ NONE          | No hay información para la oración.                                               |
| IME \_ SMODE \_ PHRASEPREDICT | El IME usa información de frases para predecir el carácter siguiente.             |
| \_PLURALCLAUSE de SMODE de IME \_  | El IME usa información de cláusula plural para llevar a cabo el procesamiento de conversión. |
| IME \_ SMODE \_ SINGLECONVERT | El IME lleva a cabo el procesamiento de conversión en modo de un solo carácter.        |
| IME \_ SMODE \_ CONVERSATION  | El IME usa el modo de conversación. Esto es útil para las aplicaciones de chat.      |



 

Los bits del 16 al 31 están reservados para su uso en IME.

 

 



