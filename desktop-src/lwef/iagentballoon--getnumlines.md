---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461ebc4fa7c7e0ae9080544e9114db9f8c179925dae665925d893288f95de027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478629"
---
# <a name="iagentballoongetnumlines"></a>IAgentBalloon::GetNumLines

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

Recupera el valor del número de líneas que se muestran en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*
</dt> <dd>

Dirección de una variable que recibe el número de líneas mostradas.

</dd> </dl>

El servidor de Microsoft Agent desplaza automáticamente las líneas mostradas para la salida hablada en el globo de palabras. El número de líneas de un globo de palabras de caracteres se define en el Editor de caracteres de Microsoft Agent. Una aplicación no puede cambiarlo.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




