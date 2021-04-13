---
title: IAgentCommand GetVisible
description: IAgentCommand GetVisible
ms.assetid: cac07737-6a0b-4587-ae16-2137ce0d412c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1058c3855214dada0f1567f9fef81a3efc7e20a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420692"
---
# <a name="iagentcommandgetvisible"></a>IAgentCommand:: GetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Command
);
```

Recupera el valor de la propiedad [**visible**](visible-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Dirección de una variable que recibe la propiedad [**visible**](visible-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 