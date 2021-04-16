---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714370"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Establece el texto [**VoiceCaption**](voicecaption-property.md) que se muestra para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR que especifica el texto de la propiedad [**VoiceCaption**](voicecaption-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si define un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) y establece su propiedad [**Voice**](voice-property.md) , normalmente también establecerá su propiedad [**VoiceCaption**](voicecaption-property.md) . Este texto aparecerá en la ventana comandos de voz cuando la aplicación cliente sea de entrada-activa y el carácter esté visible. Si no se establece esta propiedad, el valor de la propiedad [**Caption**](caption-property.md) determina el texto que se muestra. Cuando no se establece la propiedad **VoiceCaption** o **Caption** , el comando no aparece en la ventana comandos de voz.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 