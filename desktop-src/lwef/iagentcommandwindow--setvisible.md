---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075918"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow:: SetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Establezca la propiedad [**visible**](visible-property.md) para la ventana comandos de voz.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Configuración de la propiedad [**visible**](visible-property.md) . Un valor de **true** muestra la ventana comandos de voz. **False** lo oculta.

</dd> </dl>

El usuario puede invalidar esta propiedad.

## <a name="see-also"></a>Consulte también

[**IAgentCommandWindow:: GetVisible**](iagentcommandwindow--getvisible.md)


 

 




