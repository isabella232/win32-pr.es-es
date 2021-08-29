---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62415c5e51cbf6642b4a348de2060fccb6bac41467dd00b7671888d06b8e71f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888405"
---
# <a name="iagentballoongetnumcharsperline"></a>IAgentBalloon::GetNumCharsPerLine

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

Recupera el valor del número medio de caracteres por línea que se muestra en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*
</dt> <dd>

Dirección de una variable que recibe el número de caracteres por línea.

</dd> </dl>

El servidor de Microsoft Agent desplaza automáticamente las líneas mostradas para la salida hablada en el globo de palabras. El número medio de caracteres por línea para el globo de palabras de un carácter se define en el Editor de caracteres de Microsoft Agent. Una aplicación no puede cambiarla.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md)


 

 




