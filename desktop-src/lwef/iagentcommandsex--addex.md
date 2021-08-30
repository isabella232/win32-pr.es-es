---
title: IAgentCommandsEx AddEx
description: IAgentCommandsEx AddEx
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134f7b0ae7c2b635aaa15beec203b8eea661e4ca925c0ed0eda9dcab314294c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961845"
---
# <a name="iagentcommandsexaddex"></a>IAgentCommandsEx::AddEx

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT AddEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long * pdwID           // address for variable for ID
);
```

Agrega un [**comando**](/windows/desktop/lwef/the-command-object) a una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el valor del texto [**título**](caption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el valor de la configuración [**de**](voice-property.md) texto Voice para [**un comando**](/windows/desktop/lwef/the-command-object) en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR que especifica el valor del texto [**VoiceCaption**](voicecaption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Expresión booleana que especifica el valor [**Habilitado**](enabled-property.md) para un [**comando en**](/windows/desktop/lwef/the-command-object) una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) Si el parámetro es **True**, el **comando** está habilitado y se puede seleccionar; si **es False**, el **comando** está deshabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Expresión booleana que especifica la configuración [**Visible**](visible-property.md) para un [**comando en**](/windows/desktop/lwef/the-command-object) una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) Si el parámetro es **True**, **el** comando estará visible en el [](caption-property.md) menú emergente del carácter (si también se establece la propiedad Caption).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Número de contexto del tema de ayuda asociado al [**objeto Command;**](/windows/desktop/lwef/the-command-object) se usa para proporcionar ayuda contextual para el comando.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Dirección de una variable que recibe el identificador del comando [**agregado.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

[**IAgentCommandsEx::AddEx**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) extiende [**IAgentCommands::Add**](iagentcommands--add.md) incluyendo la [**propiedad HelpContextID.**](helpcontextid-property.md) También puede establecer la propiedad mediante [ **IAgentCommandsEx::SetHelpContextID.**](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Consulte también

[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 