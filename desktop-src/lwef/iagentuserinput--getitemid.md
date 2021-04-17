---
title: IAgentUserInput GetItemID
description: IAgentUserInput GetItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704561"
---
# <a name="iagentuserinputgetitemid"></a>IAgentUserInput::GetItemID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

Recupera el identificador de una alternativa de [**comando**](command-event.md) pasada a una devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Índice de la alternativa de [**comando**](command-event.md) que se pasa a la devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*
</dt> <dd>

Dirección de una variable que recibe el identificador de un [**comando**](command-event.md).

</dd> </dl>

Si la entrada de voz desencadena la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , el servidor devuelve los identificadores para los [**comandos**](command-event.md) coincidentes definidos por la aplicación.

## <a name="see-also"></a>Consulte también

[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




