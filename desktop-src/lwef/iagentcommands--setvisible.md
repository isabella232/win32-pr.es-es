---
title: IAgentCommands SetVisible
description: IAgentCommands SetVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714353"
---
# <a name="iagentcommandssetvisible"></a>IAgentCommands:: SetVisible

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

Establece el valor de la propiedad [**visible**](visible-property.md) para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valor booleano que determina la propiedad [**visible**](visible-property.md) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . **True** establece el [**título**](caption-property.md) de la colección de **comandos** para que esté visible cuando se muestre el menú emergente del carácter; *False* no la muestra.

</dd> </dl>

Una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) debe tener su propiedad [**Caption**](caption-property.md) establecida y su propiedad [**visible**](visible-property.md) establecida en **true** para que aparezca en el menú emergente del carácter. La propiedad **visible** también se debe establecer en **true** para que los comandos de la colección aparezcan cuando la aplicación cliente sea de entrada.

## <a name="see-also"></a>Consulte también

[**IAgentCommands:: GetVisible**](iagentcommands--getvisible.md), [ **IAgentCommand:: SetCaption**](iagentcommand--setcaption.md)


 

 