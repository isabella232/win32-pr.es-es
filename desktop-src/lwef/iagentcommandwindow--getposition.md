---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52571311a87ee0846dcaf515912762069fe3025a25c5a2589770ee9738bb2de7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716105"
---
# <a name="iagentcommandwindowgetposition"></a>IAgentCommandWindow::GetPosition

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Recupera la posición de la ventana Comandos de voz.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde izquierdo de la ventana Comandos de voz en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde superior de la ventana Comandos de voz en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommandWindow::GetSize**](iagentcommandwindow--getsize.md)


 

 




