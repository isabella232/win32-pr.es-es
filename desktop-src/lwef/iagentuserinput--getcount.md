---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268202"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput:: GetCount

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Recupera el número de alternativas de [**comando**](command-event.md) que se pasan a una devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Dirección de una variable que recibe el recuento de alternativas de [**comandos**](command-event.md) identificadas por el servidor.

</dd> </dl>

Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario selecciona el comando en el menú emergente del carácter, **getCount** devuelve 1. Si **getCount** devuelve cero (0), el motor de reconocimiento de voz detectó una entrada oral pero determinó que no había ningún comando coincidente.

 

 




