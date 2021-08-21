---
title: IAgentCommandEx GetVoiceCaption
description: IAgentCommandEx GetVoiceCaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d093a971331c6c5cddf467e770dae69960ae0d616ddc9b37863a46d25becb7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105423"
---
# <a name="iagentcommandexgetvoicecaption"></a>IAgentCommandEx::GetVoiceCaption

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

Recupera [**voiceCaption para**](voicecaption-property.md) un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

Dirección de un BSTR que recibe el valor del texto [**de**](caption-property.md) título que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

[**VoiceCaption es**](voicecaption-property.md) el texto que aparece para un objeto [**Command**](/windows/desktop/lwef/the-command-object) en la ventana Comandos de voz cuando la aplicación cliente está activa en la entrada.

## <a name="see-also"></a>Consulte también

[**IAgentCommandEx::SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 