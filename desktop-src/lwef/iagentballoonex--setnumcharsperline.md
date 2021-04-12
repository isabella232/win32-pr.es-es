---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357565"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBalloonEx::SetNumCharsPerLine

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Establece el número de caracteres por línea que se pueden mostrar en el globo de palabras del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.
-   Devuelve E \_ INVALIDARG si el parámetro es menor que ocho.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

Número de líneas que se van a mostrar en el globo de palabras.

</dd> </dl>

El valor mínimo es 8 y el máximo es 255. Si el texto especificado en el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) supera el tamaño del globo actual, el agente desplaza automáticamente el texto del globo.

La configuración predeterminada se basa en la configuración cuando el carácter se compila con el editor de caracteres del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




