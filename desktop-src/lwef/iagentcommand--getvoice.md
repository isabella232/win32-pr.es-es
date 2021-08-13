---
title: IAgentCommand GetVoice
description: IAgentCommand GetVoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e27996f06a0446f7aaab944df8638134990fffe951400d94c690f52f78cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750432"
---
# <a name="iagentcommandgetvoice"></a>IAgentCommand::GetVoice

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Recupera el valor de la propiedad de texto [**Voice**](voice-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Dirección de un BSTR que recibe la [**propiedad De**](voice-property.md) voz de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) con su [**propiedad Voice**](voice-property.md) establecida y su propiedad [**Enabled**](enabled-property.md) establecida en **True** serán accesibles por voz. Si su [**propiedad Caption**](caption-property.md) también está establecida, aparece en la ventana Comandos de voz. Si su [**propiedad Visible**](visible-property.md) está establecida en **True,** aparece en el menú emergente del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 