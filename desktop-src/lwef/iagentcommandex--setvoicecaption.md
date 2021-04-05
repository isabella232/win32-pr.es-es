---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077586"
---
# <a name="iagentcommandexsetvoicecaption"></a>IAgentCommandEx::SetVoiceCaption

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Establece el texto [**VoiceCaption**](voicecaption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR que especifica el texto de la propiedad [**VoiceCaption**](voicecaption-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si define un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) y establece su propiedad [**Voice**](voice-property.md) , normalmente también establecerá su propiedad [**VoiceCaption**](voicecaption-property.md) . Este texto aparecerá en la ventana comandos de voz cuando se active la entrada de la aplicación cliente. Si no se establece esta propiedad, el valor de la propiedad [**Caption**](caption-property.md) determina el texto que se muestra. Cuando no se establece la propiedad **VoiceCaption** o, el comando no aparece en la ventana comandos de voz.

[**Caption**](caption-property.md)

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: setEnabled**](iagentcommand--setenabled.md), [**IAgentCommand:: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx:: Addex**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 