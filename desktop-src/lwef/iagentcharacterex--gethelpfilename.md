---
title: IAgentCharacterEx GetHelpFileName
description: IAgentCharacterEx GetHelpFileName
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d692de5704f88d14e32231a7d63fc80150f1481a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994429"
---
# <a name="iagentcharacterexgethelpfilename"></a>IAgentCharacterEx::GetHelpFileName

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

Recupera el HelpFileName para un carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Dirección de una variable que recibe el nombre de archivo de ayuda para el carácter.

</dd> </dl>

Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el agente de Microsoft llama automáticamente a la ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario hace clic en el carácter o selecciona un comando en el menú emergente. Si hay un número de contexto en la propiedad [**IDDelContextoDeAyuda**](helpcontextid-property.md) del comando seleccionado, la ayuda muestra un tema correspondiente al contexto de ayuda actual. en caso contrario, se muestra "no hay ningún tema de ayuda asociado a este elemento".

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




