---
title: IAgentBalloon SetVisible
description: IAgentBalloon SetVisible
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c821d4e3686a9e454798cb80a85f3047f8cbdbaf57c075dae1361db6606d4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478599"
---
# <a name="iagentballoonsetvisible"></a>IAgentBalloon::SetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // word balloon Visible setting 
);
```

Establece la [**propiedad Visible**](visible-property.md) para la palabra globo.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valor de propiedad visible. Un valor de **True muestra** la palabra globo; Un valor de **False** lo oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetVisible**](iagentballoon--getvisible.md)


 

 




