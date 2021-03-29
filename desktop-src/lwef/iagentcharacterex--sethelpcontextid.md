---
title: IAgentCharacterEx SetHelpContextID
description: IAgentCharacterEx SetHelpContextID
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774497"
---
# <a name="iagentcharacterexsethelpcontextid"></a>IAgentCharacterEx::SetHelpContextID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Establece [**HelpContextID**](helpcontextid-property.md) para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

El número de contexto del tema de ayuda para asociado a un carácter; se utiliza para proporcionar ayuda contextual para el carácter.

</dd> </dl>

Si ha creado un archivo de ayuda de Windows para la aplicación y lo ha establecido en la propiedad [**HelpFile**](helpfile-property.md) del carácter, el agente de Microsoft llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el carácter. Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el carácter. Si hay un número de contexto en la propiedad **HelpContextID** , la ayuda muestra un tema correspondiente al contexto de ayuda actual. en caso contrario, se muestra "no hay ningún tema de ayuda asociado a este elemento".

Esta configuración solo se aplica cuando la aplicación cliente es el cliente activo del carácter más alto. No afecta a otros clientes del carácter u otros caracteres que usa la aplicación cliente.

> [!Note]  
> La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:: GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




