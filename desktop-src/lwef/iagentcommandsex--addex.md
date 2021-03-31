---
title: IAgentCommandsEx AddEx
description: IAgentCommandsEx AddEx
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7487bb7c7af0295d82355c7a1f7fb50e30aa6e1f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790600"
---
# <a name="iagentcommandsexaddex"></a>IAgentCommandsEx:: AddEx

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

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

Agrega un [**comando**](/windows/desktop/lwef/the-command-object) a una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el valor del texto de [**título**](caption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el valor de la configuración del texto de la [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR que especifica el valor del texto [**VoiceCaption**](voicecaption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Una expresión booleana que especifica el valor [**habilitado**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Si el parámetro es **true**, el **comando** está habilitado y se puede seleccionar; Si es **false**, el **comando** está deshabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Una expresión booleana que especifica el valor [**visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Si el parámetro es **true**, el **comando** estará visible en el menú emergente del carácter (si también se establece la propiedad [**Caption**](caption-property.md) ).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

El número de contexto del tema de ayuda asociado al objeto de [**comando**](/windows/desktop/lwef/the-command-object) ; se utiliza para proporcionar ayuda contextual para el comando.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Dirección de una variable que recibe el identificador del [**comando**](/windows/desktop/lwef/the-command-object)agregado.

</dd> </dl>

[**IAgentCommandsEx:: Addex**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) extiende [**IAgentCommands:: Add**](iagentcommands--add.md) incluyendo la propiedad [**HelpContextID**](helpcontextid-property.md) . También puede establecer la propiedad mediante [ **IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Consulte también

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setEnabled**](iagentcommand--setenabled.md), [**IAgentCommand:: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 