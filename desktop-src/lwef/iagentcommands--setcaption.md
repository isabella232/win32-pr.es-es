---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420574"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands::SetCaption

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Establece el texto de [**título**](caption-property.md) que se muestra para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el valor de la propiedad [**Caption**](caption-property.md) de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

Al establecer la propiedad [**Caption**](caption-property.md) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**visible**](visible-property.md) esté establecida en **true** y la aplicación no sea el cliente de entrada-activo. Para especificar una tecla de acceso (tecla de acceso no alineada) para el **título**, incluya un carácter de y comercial (&) antes de ese carácter.

Si define comandos para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) que tiene su conjunto de [**leyendas**](caption-property.md) , normalmente también se define un **título** para la colección de **comandos** .

## <a name="see-also"></a>Consulte también

[**IAgentCommands:: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: setVisible**](iagentcommands--setvisible.md), [**IAgentCommands:: SetVoice**](iagentcommands--setvoice.md)


 

 