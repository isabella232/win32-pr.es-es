---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949591bc22c93711af19ce18cb024ede9714335f249839eb4819a73e231e0d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976245"
---
# <a name="iagentcommandwindowgetvisible"></a>IAgentCommandWindow::GetVisible

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

Determina si la ventana Comandos de voz está visible u oculta.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Dirección de una variable que recibe **True si** la ventana Comandos de voz está visible, o **False** si está oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommandWindow::SetVisible**](iagentcommandwindow--setvisible.md)


 

 




