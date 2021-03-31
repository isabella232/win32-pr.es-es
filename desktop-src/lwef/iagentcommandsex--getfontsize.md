---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418807"
---
# <a name="iagentcommandsexgetfontsize"></a>IAgentCommandsEx::GetFontSize

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

Recupera el valor para el tamaño de la fuente que se muestra en el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Dirección de un valor que recibe el tamaño de la fuente.

</dd> </dl>

El tamaño en puntos de la fuente devuelta corresponde al tamaño definido para mostrar texto en el menú emergente del carácter cuando el cliente es de entrada-activo. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente de menú para la configuración de identificador de idioma del carácter, o si no se establece, la configuración de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx:: SetFontSize**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx:: SetFontName**](iagentcommandsex--setfontname.md)


 

 




