---
title: IAgentCommandsEx InsertEx
description: IAgentCommandsEx InsertEx
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b43a9e449e16a3be3017a67082da20cb31eb1352a81f699908b0b94267ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961825"
---
# <a name="iagentcommandsexinsertex"></a>IAgentCommandsEx::InsertEx

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

Inserta un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el valor del texto [**título**](caption-property.md) que se muestra para el [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el valor de la [**configuración**](voice-property.md) de texto De voz para un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR que especifica el valor del texto [**VoiceCaption**](voicecaption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Expresión booleana que especifica el valor [**Habilitado**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object). Si el parámetro es **True**, el **comando** está habilitado y se puede seleccionar; si **es False**, el **comando** está deshabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Expresión booleana que especifica el valor [**Visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object). Si el parámetro es **True**, **el** comando estará visible en el [](caption-property.md) menú emergente del carácter (si también se establece la propiedad Caption).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Número de contexto del tema de ayuda asociado al [**objeto Command;**](/windows/desktop/lwef/the-command-object) se usa para proporcionar ayuda contextual para el comando.

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

Identificador de un [**comando utilizado**](/windows/desktop/lwef/the-command-object) como referencia para la inserción relativa del nuevo **comando**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Expresión booleana que especifica dónde colocar el [**comando**](/windows/desktop/lwef/the-command-object). Si este parámetro es **True**, el nuevo **comando** se inserta antes del comando al que se hace **referencia**; si **es False**, el nuevo **comando** se coloca después del comando al que se hace **referencia.**

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Dirección de una variable que recibe el identificador del comando [**insertado.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

[**IAgentCommandsEx::InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) extiende [**IAgentCommands::Insert**](iagentcommands--insert.md) incluyendo la [**propiedad HelpContextID.**](helpcontextid-property.md) También puede establecer la propiedad mediante [ **IAgentCommandsEx::SetHelpContextID.**](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 