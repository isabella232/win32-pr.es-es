---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418773"
---
# <a name="iagentpropertysheetgetpage"></a>IAgentPropertySheet::GetPage

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Recupera la página actual de la hoja de propiedades del agente de Microsoft.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*
</dt> <dd>

Dirección de una variable que recibe la página actual de la hoja de propiedades (última página que se vio si la ventana no está abierta). El parámetro puede ser uno de los siguientes:



|                 |                        |
|-----------------|------------------------|
| **Gramatical**    | La página de entrada de voz. |
| **Genere**    | La página de salida.       |
| **SSoftware** | La página Copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet:: SetPage**](iagentpropertysheet--setpage.md)


 

 




