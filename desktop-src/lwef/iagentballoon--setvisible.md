---
title: IAgentBalloon SetVisible
description: IAgentBalloon SetVisible
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838c34397bc089ea49579b5f6a8c7d5834c8a580
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704657"
---
# <a name="iagentballoonsetvisible"></a>IAgentBalloon:: SetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // word balloon Visible setting 
);
```

Establece la propiedad [**visible**](visible-property.md) para el globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Configuración de la propiedad visible. Un valor de **true** muestra el globo de palabras; un valor **false** lo oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentBalloon:: GetVisible**](iagentballoon--getvisible.md)


 

 




