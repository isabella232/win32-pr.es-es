---
title: IAgentCharacterEx GetHelpContextID
description: IAgentCharacterEx GetHelpContextID
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfec03a217745838b88a592433defae01529ed50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778715"
---
# <a name="iagentcharacterexgethelpcontextid"></a>IAgentCharacterEx::GetHelpContextID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

Recupera [**HelpContextID**](helpcontextid-property.md) para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Dirección de una variable que recibe el número de contexto del tema de ayuda para el carácter.

</dd> </dl>

Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el agente de Microsoft llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el carácter. Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el carácter.

**IAgentCharacterEx:: GetHelpContextID** devuelve el [**HelpContextID**](helpcontextid-property.md) que estableció para el carácter. No devuelve el valor de **HelpContextID** establecido por otros clientes.

> [!Note]  
> La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




