---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c296dd152fd1e31a87e21d80f8b25d52ae880b300487cdcba746e81dfa0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749522"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput::GetCount

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Recupera el número de [**alternativas**](command-event.md) de comando que se pasan a una devolución [**de llamada IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Dirección de una variable que recibe el recuento de [**alternativas de**](command-event.md) comandos identificadas por el servidor.

</dd> </dl>

Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario seleccionó el comando en el menú emergente del carácter, **GetCount** devuelve 1. Si **GetCount** devuelve cero (0), el motor de reconocimiento de voz detectó la entrada hablada, pero determinó que no había ningún comando correspondiente.

 

 




