---
title: IAgentPropertySheet SetVisible
description: IAgentPropertySheet SetVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87c67b5a240018dd1798704f5f954c0b5a24fe4b2fc889b1e2d79c892494652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961465"
---
# <a name="iagentpropertysheetsetvisible"></a>IAgentPropertySheet::SetVisible

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

Establece la [**propiedad Visible**](visible-property.md) para la hoja de propiedades de Microsoft Agent.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valor de propiedad visible. Un valor de **True muestra** la hoja de propiedades; Un valor de **False** lo oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet::GetVisible**](iagentpropertysheet--getvisible.md)


 

 




