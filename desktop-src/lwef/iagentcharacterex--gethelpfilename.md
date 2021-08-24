---
title: IAgentCharacterEx GetHelpFileName
description: IAgentCharacterEx GetHelpFileName
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba5acdcfef90d1918f5c4697127b4449e96f2667b20a2de0230fcdf2cd6dd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105533"
---
# <a name="iagentcharacterexgethelpfilename"></a>IAgentCharacterEx::GetHelpFileName

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

Recupera HelpFileName para un carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Dirección de una variable que recibe el nombre de archivo de ayuda del carácter.

</dd> </dl>

Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, Microsoft Agent llama automáticamente a la Ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario hace clic en el carácter o selecciona un comando en su menú emergente. Si hay un número de contexto en la propiedad [**HelpContextID**](helpcontextid-property.md) del comando seleccionado, la Ayuda muestra un tema correspondiente al contexto de Ayuda actual; de lo contrario, muestra "Sin tema de Ayuda asociado a este elemento".

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> La compilación de un archivo de Ayuda requiere el compilador Windows Ayuda de Microsoft.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




