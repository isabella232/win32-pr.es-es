---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356653"
---
# <a name="iagentuserinputgetitemconfidence"></a>IAgentUserInput::GetItemConfidence

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

Recupera el valor de confianza para un [**comando**](command-event.md) que se pasa a una devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Índice de una alternativa de [**comando**](command-event.md) que se pasa a la devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*
</dt> <dd>

Dirección de una variable que recibe la puntuación de confianza para una alternativa de [**comando**](command-event.md) que se pasa a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario selecciona el comando en el menú emergente del carácter, el servidor de agente de Microsoft devuelve el valor de confianza de la mejor coincidencia como 100 y los valores de confianza para todas las demás alternativas como cero (0).

## <a name="see-also"></a>Consulte también

[**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md)


 

 




