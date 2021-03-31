---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418808"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx::GetFontName

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Recupera el valor de la fuente que se muestra en el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Dirección de un BSTR que recibe el nombre de fuente mostrado en el menú emergente del carácter.

</dd> </dl>

El nombre de fuente devuelto corresponde a la fuente usada para mostrar texto en el menú emergente del carácter cuando la aplicación cliente es de entrada-activa. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente de menú para la configuración de identificador de idioma del carácter, o si no se establece, la configuración de identificador de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx:: SetFontName**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx:: SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




