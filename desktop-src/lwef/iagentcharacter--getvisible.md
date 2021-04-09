---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149196"
---
# <a name="iagentcharactergetvisible"></a>IAgentCharacter:: GetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

Determina si el marco de animación del carácter está actualmente visible.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Dirección de una variable que recibe **true** si el fotograma del carácter está visible y **false** si está oculto.

</dd> </dl>

Puede usar este método para determinar si el marco del carácter está visible actualmente. Para hacer que un carácter esté visible, use el método [**Show**](/windows/desktop/lwef/iagentcharacter--show) . Para ocultar un carácter, utilice el método [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .

 

 