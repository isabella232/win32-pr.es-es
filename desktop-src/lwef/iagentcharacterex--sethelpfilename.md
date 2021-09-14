---
title: IAgentCharacterEx SetHelpFileName
description: IAgentCharacterEx SetHelpFileName
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1342baecc1e059d4fcb5d1323c0c714bd6bf7087
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072375"
---
# <a name="iagentcharacterexsethelpfilename"></a>IAgentCharacterEx::SetHelpFileName

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

Establece helpFileName para un carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Nombre de archivo de ayuda del carácter.

</dd> </dl>

Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, Microsoft Agent llama automáticamente a help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario hace clic en el carácter o selecciona un comando en el menú emergente. Si hay un número de contexto en la propiedad [**HelpContextID**](helpcontextid-property.md) del comando seleccionado, la Ayuda muestra un tema correspondiente al contexto de Ayuda actual; de lo contrario, muestra "No hay tema de Ayuda asociado a este elemento".

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> La compilación de un archivo de Ayuda requiere microsoft Windows compilador de Ayuda.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::GetHelpFileName**](iagentcharacterex--gethelpfilename.md)


 

 




