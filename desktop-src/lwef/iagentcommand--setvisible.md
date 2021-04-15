---
title: IAgentCommand SetVisible
description: IAgentCommand SetVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695598"
---
# <a name="iagentcommandsetvisible"></a>IAgentCommand:: SetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

Establece el valor de la propiedad [**visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valor booleano que determina la propiedad [**visible**](visible-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object). **True** muestra el **comando**; **False** lo oculta.

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) debe tener su propiedad [**visible**](visible-property.md) establecida en **true** y su propiedad [**Caption**](caption-property.md) establecida en aparece en el menú emergente del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: GetVisible**](iagentcommand--getvisible.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 