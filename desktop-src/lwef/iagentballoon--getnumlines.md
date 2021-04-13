---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419109"
---
# <a name="iagentballoongetnumlines"></a>IAgentBalloon::GetNumLines

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

Recupera el valor del número de líneas que se muestran en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*
</dt> <dd>

Dirección de una variable que recibe el número de líneas que se muestran.

</dd> </dl>

El servidor de Microsoft Agent desplaza automáticamente las líneas que se muestran para la salida de voz en el globo de palabras. El número de líneas de un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft. No se puede cambiar por una aplicación.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




