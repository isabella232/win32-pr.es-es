---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098a89500606482914bfb31303a2cd79cac88f6d96d17abec58c75759f7abedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976465"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBalloonEx::SetNumCharsPerLine

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Establece el número de caracteres por línea que se pueden mostrar en el globo de palabras del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.
-   Devuelve E \_ INVALIDARG si el parámetro es menor que ocho.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

Número de líneas que se mostrarán en el globo de palabras.

</dd> </dl>

El valor mínimo es 8 y el máximo es 255. Si el texto especificado en el método [**Speak**](speak-method.md) o [**Think**](think-method.md) supera el tamaño del globo actual, el Agente desplaza automáticamente el texto del globo.

La configuración predeterminada se basa en la configuración cuando el carácter se compila con el Editor de caracteres del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




