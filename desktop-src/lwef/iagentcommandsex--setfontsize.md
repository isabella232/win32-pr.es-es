---
title: IAgentCommandsEx SetFontSize
description: IAgentCommandsEx SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487591"
---
# <a name="iagentcommandsexsetfontsize"></a>IAgentCommandsEx::SetFontSize

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

Establece el tamaño de la fuente que se muestra en el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Tamaño de la fuente.

</dd> </dl>

Esta propiedad determina el tamaño en puntos de la fuente usada para mostrar texto en el menú emergente del carácter cuando la aplicación cliente es de entrada-activa. El valor predeterminado de la configuración de fuente se basa en el valor de fuente de menú para la configuración de identificador de idioma del carácter, o bien, si no está establecido, es la configuración de idioma predeterminado del usuario. Si no es de entrada-activo, el texto de la [**leyenda**](caption-property.md) de [**comandos**](/windows/desktop/lwef/the-command-object) de la aplicación cliente aparece en el tamaño de punto especificado para el cliente de entrada-activo.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx:: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: SetFontName**](iagentcommandsex--setfontname.md)


 

 