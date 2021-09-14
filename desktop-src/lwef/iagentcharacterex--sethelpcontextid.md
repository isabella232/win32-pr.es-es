---
title: IAgentCharacterEx SetHelpContextID
description: IAgentCharacterEx SetHelpContextID
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072373"
---
# <a name="iagentcharacterexsethelpcontextid"></a>IAgentCharacterEx::SetHelpContextID

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Establece [**helpContextID**](helpcontextid-property.md) para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Número de contexto del tema de ayuda para asociado a un carácter; se usa para proporcionar ayuda contextual para el carácter.

</dd> </dl>

Si ha creado un archivo de Ayuda de Windows para la aplicación y lo ha establecido en la propiedad [**HelpFile**](helpfile-property.md) del carácter, Microsoft Agent llama automáticamente a la Ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario selecciona el carácter. Si hay un número de contexto en [**HelpContextID,**](helpcontextid-property.md)el Agente llama a la Ayuda y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor **de HelpContextID** para el carácter. Si hay un número de contexto en la **propiedad HelpContextID,** la Ayuda muestra un tema correspondiente al contexto de ayuda actual; de lo contrario, muestra "Sin tema de Ayuda asociado a este elemento".

Esta configuración solo se aplica cuando la aplicación cliente es el cliente activo del carácter superior. No afecta a otros clientes del carácter u otros caracteres que usa la aplicación cliente.

> [!Note]  
> La compilación de un archivo de Ayuda requiere microsoft Windows compilador de ayuda.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




