---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd9c1392bd56e3bb59212edeb79d862260786edb87583c0e8fdf049e8345b40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359045"
---
# <a name="iagentuserinputgetitemtext"></a>IAgentUserInput::GetItemText

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Recupera el texto de voz de una [**alternativa**](command-event.md) command pasada a la devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Índice de una [**alternativa**](command-event.md) command que se pasa a la devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Dirección de un BSTR que recibe el valor del texto de voz para el [**comando**](command-event.md).

</dd> </dl>

Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario seleccionó [](command-event.md)el comando en el menú emergente del carácter, el servidor devuelve **NULL** para el texto de voz del comando.

## <a name="see-also"></a>Consulte también

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




