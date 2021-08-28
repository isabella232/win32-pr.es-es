---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757b2d7554f1efcee27a519b9df61b4601a237b557c3aa26b6575864144a2850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105241"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx::GetFontName

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Recupera el valor de la fuente que se muestra en el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Dirección de un BSTR que recibe el nombre de fuente que se muestra en el menú emergente del carácter.

</dd> </dl>

El nombre de fuente devuelto corresponde a la fuente utilizada para mostrar texto en el menú emergente del carácter cuando la aplicación cliente está activa en la entrada. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente del menú para la configuración del identificador de idioma del carácter o, si no se establece, en la configuración del identificador de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




