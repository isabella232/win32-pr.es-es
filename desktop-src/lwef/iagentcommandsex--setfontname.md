---
title: IAgentCommandsEx SetFontName
description: IAgentCommandsEx SetFontName
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511425df848749791d2803a484e00da8e838cfa191eade05c578fdad4b3ca6cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105219"
---
# <a name="iagentcommandsexsetfontname"></a>IAgentCommandsEx::SetFontName

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

Establece la fuente que se muestra en el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

BSTR que establece la fuente que se muestra en el menú emergente del carácter.

</dd> </dl>

Esta propiedad determina la fuente utilizada para mostrar texto en el menú emergente del carácter. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente del menú para la configuración del identificador de idioma del carácter o si no se establece la configuración del identificador de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




