---
title: IAgentCommand SetVisible
description: IAgentCommand SetVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e28d1b1c16dca0ddc48a83af42111420a5f07eda7ab546f57904f79dcf6a6e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692837"
---
# <a name="iagentcommandsetvisible"></a>IAgentCommand::SetVisible

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

Establece el valor de la [**propiedad Visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valor booleano que determina la [**propiedad Visible**](visible-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object). **True** muestra el **comando**; **False** lo oculta.

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) debe tener su [**propiedad Visible**](visible-property.md) establecida en **True** y su propiedad [**Caption**](caption-property.md) establecida para que aparezca en el menú emergente del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCommand::GetVisible**](iagentcommand--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 