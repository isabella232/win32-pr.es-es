---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776890"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet:: SetPage

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Establece la página actual de la hoja de propiedades del agente de Microsoft.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*
</dt> <dd>

BSTR que establece la página actual de la propiedad. El parámetro puede ser uno de los siguientes.



|                 |                        |
|-----------------|------------------------|
| **Gramatical**    | La página de entrada de voz. |
| **Genere**    | La página de salida.       |
| **SSoftware** | La página Copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 




