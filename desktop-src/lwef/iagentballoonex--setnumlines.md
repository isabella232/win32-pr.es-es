---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486951"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBalloonEx::SetNumLines

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Establece el número de líneas de salida de texto que se pueden mostrar en el globo de palabras del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.
-   Devuelve E \_ INVALIDARG si el valor del parámetro es cero.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

Número de líneas que se van a mostrar en el globo de palabras.

</dd> </dl>

El valor mínimo es 1 y el máximo es 128. Si el texto especificado en el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) supera el tamaño del globo actual, el agente desplaza automáticamente el texto del globo.

Este método producirá un error si se establece el bit de estilo de globo **SizeToText** .

La configuración predeterminada se basa en la configuración cuando el carácter se compila con el editor de caracteres del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon:: GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx:: getStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx:: setStyle**](iagentballoonex--setstyle.md)


 

 




