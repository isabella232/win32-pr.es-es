---
title: IAgentPropertySheet SetVisible
description: IAgentPropertySheet SetVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704667"
---
# <a name="iagentpropertysheetsetvisible"></a>IAgentPropertySheet:: SetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

Establece la propiedad [**visible**](visible-property.md) de la hoja de propiedades del agente de Microsoft.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Configuración de la propiedad visible. Un valor de **true** muestra la hoja de propiedades; un valor **false** lo oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet:: GetVisible**](iagentpropertysheet--getvisible.md)


 

 




