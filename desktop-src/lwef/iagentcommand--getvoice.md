---
title: IAgentCommand GetVoice
description: IAgentCommand GetVoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704941"
---
# <a name="iagentcommandgetvoice"></a>IAgentCommand::GetVoice

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Recupera el valor de la propiedad texto de la [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Dirección de un BSTR que recibe la propiedad de texto de [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) con su propiedad [**Voice**](voice-property.md) establecida y su propiedad [**Enabled**](enabled-property.md) establecida en **true** será accesible para voz. Si también se establece su propiedad [**título**](caption-property.md) , aparece en la ventana comandos de voz. Si su propiedad [**visible**](visible-property.md) está establecida en **true**, aparecerá en el menú emergente del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 