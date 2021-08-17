---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8d06c40fd88b525cadf9f90a1edd4edaaf3a9e9be7ccdcfa98dd6abf8b833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692648"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow::SetVisible

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Establezca la [**propiedad Visible**](visible-property.md) para la ventana Comandos de voz.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

[**Valor de**](visible-property.md) propiedad visible. Un valor de **True muestra** la ventana Comandos de voz; **False** lo oculta.

</dd> </dl>

El usuario puede invalidar esta propiedad.

## <a name="see-also"></a>Consulte también

[**IAgentCommandWindow::GetVisible**](iagentcommandwindow--getvisible.md)


 

 




