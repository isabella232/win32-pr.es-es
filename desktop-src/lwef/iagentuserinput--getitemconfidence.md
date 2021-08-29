---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aec7e19c97161437dd4fd5d0e784a78ec7ebbe7e20edd8ff540c3ddeedb27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716065"
---
# <a name="iagentuserinputgetitemconfidence"></a>IAgentUserInput::GetItemConfidence

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

Recupera el valor de confianza de un [**comando pasado**](command-event.md) a una devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Índice de una [**alternativa**](command-event.md) command que se pasa a la devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*
</dt> <dd>

Dirección de una variable que recibe la puntuación de confianza de una [**alternativa command**](command-event.md) pasada a la devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> </dl>

Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario seleccionó el comando en el menú emergente del carácter, el servidor de Microsoft Agent devuelve el valor de confianza de la mejor coincidencia como 100 y los valores de confianza para todas las demás alternativas como cero (0).

## <a name="see-also"></a>Consulte también

[**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md)


 

 




