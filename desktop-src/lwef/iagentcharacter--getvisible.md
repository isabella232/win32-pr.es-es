---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c812c7765bed791532db00c8f2e9cfd68cc771575e7a70fd27d45adef00bdb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478378"
---
# <a name="iagentcharactergetvisible"></a>IAgentCharacter::GetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

Determina si el marco de animación del carácter está visible actualmente.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Dirección de una variable que recibe **True si** el marco del carácter está visible y **False** si está oculto.

</dd> </dl>

Puede usar este método para determinar si el marco del carácter está visible actualmente. Para que un carácter sea visible, use el [**método Show.**](/windows/desktop/lwef/iagentcharacter--show) Para ocultar un carácter, use el [**método Hide.**](/windows/desktop/lwef/iagentcharacter--hide)

 

 