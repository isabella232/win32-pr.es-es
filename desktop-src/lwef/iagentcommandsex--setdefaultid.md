---
title: IAgentCommandsEx SetDefaultID
description: IAgentCommandsEx SetDefaultID
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420616"
---
# <a name="iagentcommandsexsetdefaultid"></a>IAgentCommandsEx::SetDefaultID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

Establece el identificador del comando predeterminado en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

IDENTIFICADOR del [**comando**](/windows/desktop/lwef/the-command-object) que se va a establecer como valor predeterminado.

</dd> </dl>

Esta propiedad establece el conjunto de objetos de [**comando**](/windows/desktop/lwef/the-command-object) predeterminado en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . El comando predeterminado está en negrita en el menú emergente del carácter. Sin embargo, el establecimiento del comando predeterminado no cambia realmente el control de comandos ni los eventos de doble clic.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::GetDefaultID**](iagentcommandsex--getdefaultid.md)


 

 