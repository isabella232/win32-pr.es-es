---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6eabb7278e40030209ac85f55c3a7d5c00edda5c666493e053dfcbfae2ecd9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692466"
---
# <a name="iagentpropertysheetgetpage"></a>IAgentPropertySheet::GetPage

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Recupera la página actual de la hoja de propiedades de Microsoft Agent.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*
</dt> <dd>

Dirección de una variable que recibe la página actual de la hoja de propiedades (última página vista si la ventana no está abierta). El parámetro puede ser uno de los siguientes:



|                 | Descripción            |
|-----------------|------------------------|
| **"Voz"**    | Página Entrada de voz. |
| **"Salida"**    | Página Salida.       |
| **"Copyright"** | Página Copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet::SetPage**](iagentpropertysheet--setpage.md)


 

 




