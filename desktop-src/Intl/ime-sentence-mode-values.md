---
description: Estos valores se usan con las funciones ImmGetConversionStatus y ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores del modo de oración IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277043"
---
# <a name="ime-sentence-mode-values"></a>Valores del modo de oración IME

Estos valores se usan con las funciones [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) y [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .



| Constante                  | Definición                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| SMODE de IME \_ \_ automática     | El IME realiza el procesamiento de la conversión en modo automático.               |
| IME \_ SMODE \_ ninguno          | No hay información para la frase.                                               |
| IME \_ SMODE \_ PHRASEPREDICT | El IME usa la información de frases para predecir el siguiente carácter.             |
| IME \_ SMODE \_ PLURALCLAUSE  | El IME usa la información de la cláusula plural para llevar a cabo el procesamiento de la conversión. |
| IME \_ SMODE \_ SINGLECONVERT | El IME realiza el procesamiento de la conversión en el modo de un solo carácter.        |
| \_conversación SMODE de IME \_  | El IME usa el modo de conversación. Esto resulta útil para las aplicaciones de chat.      |



 

Los bits 16 a 31 están reservados para el uso de IME.

 

 



