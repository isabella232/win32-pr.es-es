---
description: Revise la lista de valores de modo de oración del editor de métodos de entrada (IME). Estos valores se usan con las funciones ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores del modo de oración IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406768"
---
# <a name="ime-sentence-mode-values"></a>Valores del modo de oración IME

Estos valores se usan con las [**funciones ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)



| Constante                  | Definición                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| IME \_ SMODE \_ AUTOMATIC     | El IME lleva a cabo el procesamiento de conversión en modo automático.               |
| IME \_ SMODE \_ NONE          | No hay información para la oración.                                               |
| IME \_ SMODE \_ PHRASEPREDICT | El IME usa información de frases para predecir el carácter siguiente.             |
| IME \_ SMODE \_ PLURALCLAUSE  | El IME usa información de la cláusula plural para llevar a cabo el procesamiento de conversión. |
| IME \_ SMODE \_ SINGLECONVERT | El IME lleva a cabo el procesamiento de conversión en modo de carácter único.        |
| IME \_ SMODE \_ CONVERSATION  | El IME usa el modo de conversación. Esto es útil para aplicaciones de chat.      |



 

Los bits del 16 al 31 están reservados para el uso de IME.

 

 



