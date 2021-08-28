---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85de69b4b594f93adfb0ff554819243c94986420a79c35e8d7a64a3c2eaccb6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716145"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Establece el [**texto VoiceCaption**](voicecaption-property.md) que se muestra para el [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

BSTR que especifica el texto de la propiedad [**VoiceCaption**](voicecaption-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si define un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una [**colección Commands**](/windows/desktop/lwef/the-commands-collection-object) y establece su propiedad [**Voice,**](voice-property.md) normalmente también establecerá su [**propiedad VoiceCaption.**](voicecaption-property.md) Este texto aparecerá en la ventana Comandos de voz cuando la aplicación cliente esté activa en la entrada y el carácter esté visible. Si no se establece esta propiedad, la configuración de la [**propiedad Caption**](caption-property.md) determina el texto mostrado. Cuando no se **establece la propiedad VoiceCaption** o **Caption,** el comando no aparece en la ventana Comandos de voz.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 