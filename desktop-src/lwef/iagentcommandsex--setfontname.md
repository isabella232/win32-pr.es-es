---
title: IAgentCommandsEx SetFontName
description: IAgentCommandsEx SetFontName
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773693"
---
# <a name="iagentcommandsexsetfontname"></a>IAgentCommandsEx::SetFontName

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

Establece la fuente mostrada en el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

BSTR que establece la fuente mostrada en el menú emergente del carácter.

</dd> </dl>

Esta propiedad determina la fuente usada para mostrar texto en el menú emergente del carácter. El valor predeterminado de la configuración de fuente se basa en el valor de fuente de menú para la configuración de identificador de idioma del carácter, o bien, si no se establece, la configuración de identificador de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx:: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




