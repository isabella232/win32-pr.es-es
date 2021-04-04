---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076308"
---
# <a name="iagentballoongetnumcharsperline"></a>IAgentBalloon::GetNumCharsPerLine

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

Recupera el valor para el promedio de caracteres por línea mostrado en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*
</dt> <dd>

Dirección de una variable que recibe el número de caracteres por línea.

</dd> </dl>

El servidor de Microsoft Agent desplaza automáticamente las líneas que se muestran para la salida de voz en el globo de palabras. El número promedio de caracteres por línea para el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft. No se puede cambiar por una aplicación.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md)


 

 




