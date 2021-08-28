---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3951cd4a8593d5e043e1571cdf24e14fdd9d93aef690c057860c2889022aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848725"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBalloonEx::SetNumLines

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Establece el número de líneas de salida de texto que se pueden mostrar en el globo de palabras del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.
-   Devuelve E \_ INVALIDARG si el parámetro es cero.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

Número de líneas que se mostrarán en el globo de palabras.

</dd> </dl>

El valor mínimo es 1 y el máximo es 128. Si el texto especificado en el método [**Speak**](speak-method.md) o [**Think**](think-method.md) supera el tamaño del globo actual, el Agente desplaza automáticamente el texto del globo.

Este método producirá un error si se establece el bit de estilo de globo **SizeToText.**

La configuración predeterminada se basa en la configuración cuando el carácter se compila con el Editor de caracteres del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)


 

 




