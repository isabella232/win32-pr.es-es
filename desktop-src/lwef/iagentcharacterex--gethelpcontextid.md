---
title: IAgentCharacterEx GetHelpContextID
description: IAgentCharacterEx GetHelpContextID
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3a64de0f4373bcaa890156ec88595d066aae9ae84b5b242fe62ffae10479d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750800"
---
# <a name="iagentcharacterexgethelpcontextid"></a>IAgentCharacterEx::GetHelpContextID

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

Recupera [**helpContextID para**](helpcontextid-property.md) el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Dirección de una variable que recibe el número de contexto del tema de ayuda para el carácter.

</dd> </dl>

Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, Microsoft Agent llama automáticamente a la Ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario selecciona el carácter. Si hay un número de contexto en [**HelpContextID,**](helpcontextid-property.md)el Agente llama a la Ayuda y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor **de HelpContextID** para el carácter.

**IAgentCharacterEx::GetHelpContextID** devuelve el [**HelpContextID**](helpcontextid-property.md) que estableció para el carácter. No devuelve el **HelpContextID** establecido por otros clientes.

> [!Note]  
> La compilación de un archivo de Ayuda requiere el compilador Windows Ayuda de Microsoft.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




