---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe76edb17c2b099db5e16e2b6160703c6b11e8a9f52bcbc24a9ca4bfcb7077c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477218"
---
# <a name="iagentcommandexsetvoicecaption"></a>IAgentCommandEx::SetVoiceCaption

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Establece el [**texto VoiceCaption**](voicecaption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR que especifica el texto de la propiedad [**VoiceCaption**](voicecaption-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si define un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una [**colección Commands**](/windows/desktop/lwef/the-commands-collection-object) y establece su propiedad [**Voice,**](voice-property.md) normalmente también establecerá su [**propiedad VoiceCaption.**](voicecaption-property.md) Este texto aparecerá en la ventana Comandos de voz cuando la aplicación cliente esté activa. Si no se establece esta propiedad, la configuración de la [**propiedad Caption**](caption-property.md) determina el texto mostrado. Cuando no se establece la propiedad **VoiceCaption** o , el comando no aparece en la ventana Comandos de voz.

[**Caption**](caption-property.md)

## <a name="see-also"></a>Consulte también

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 