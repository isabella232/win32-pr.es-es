---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120750"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet::SetPage

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Establece la página actual de la hoja de propiedades de Microsoft Agent.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*
</dt> <dd>

BSTR que establece la página actual de la propiedad. El parámetro puede ser uno de los siguientes.



|                 | Descripción            |
|-----------------|------------------------|
| **"Voz"**    | Página Entrada de voz. |
| **"Salida"**    | Página Salida.       |
| **"Copyright"** | Página Copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 




