---
title: IAgentBalloon
description: IAgentBalloon
ms.assetid: 94a48cd9-bea5-4993-8991-50c6c86a646b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b811956e368abbaf2d2782c68017084f5e17a09f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790329"
---
# <a name="iagentballoon"></a>IAgentBalloon

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

**IAgentBalloon** define una interfaz que permite que las aplicaciones consulten las propiedades del globo de palabras del agente de Microsoft. Estas funciones también están disponibles en [**IAgentBalloonEx**](https://www.bing.com/search?q=**IAgentBalloonEx**).

Los valores predeterminados iniciales del globo de palabras de un carácter se establecen en el editor de caracteres del agente de Microsoft, pero una vez que la aplicación se está ejecutando, el usuario puede invalidar las propiedades de [fuente](fontname-property.md) y [**habilitadas**](enabled-property.md) . Si un usuario cambia las propiedades del globo, el cambio afecta a todos los caracteres. Las propiedades del objeto [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) también se aplican a la salida de texto a través del método de [**reflexión**](think-method.md) .

**Métodos en orden de Vtable**



| Métodos IAgentBalloon                                       | Descripción                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [GetEnabled](iagentballoon--getenabled.md)                 | Devuelve si el globo de palabras está habilitado.                                          |
| [GetNumLines](iagentballoon--getnumlines.md)               | Devuelve el número de líneas que se muestran en el globo de palabras.                            |
| [GetNumCharsPerLine](iagentballoon--getnumcharsperline.md) | Devuelve el número promedio de caracteres por línea mostrado en el globo de palabras.      |
| [GetFontName](iagentballoon--getfontname.md)               | Devuelve el nombre de la fuente que se muestra en el globo de palabras.                           |
| [GetFontSize](iagentballoon--getfontsize.md)               | Devuelve el tamaño de la fuente que se muestra en el globo de palabras.                           |
| [GetFontBold](iagentballoon--getfontbold.md)               | Devuelve si la fuente mostrada en el globo de palabras está en negrita.                       |
| [GetFontItalic](iagentballoon--getfontitalic.md)           | Devuelve si la fuente mostrada en el globo de palabras está en cursiva.                     |
| [GetFontStrikethru](iagentballoon--getfontstrikethru.md)   | Devuelve si la fuente mostrada en el globo de palabras se muestra tachado. |
| [GetFontUnderline](iagentballoon--getfontunderline.md)     | Devuelve si la fuente mostrada en el globo de palabras está subrayada.                 |
| [GetForeColor](iagentballoon--getforecolor.md)             | Devuelve el color de primer plano que se muestra en el globo de palabras.                           |
| [GetBackColor](iagentballoon--getbackcolor.md)             | Devuelve el color de fondo que se muestra en el globo de palabras.                           |
| [GetBorderColor](iagentballoon--getbordercolor.md)         | Devuelve el color del borde que se muestra en el globo de palabras.                               |
| [SetVisible](iagentballoon--setvisible.md)                 | Establece que el globo de palabras esté visible.                                                  |
| [GetVisible](iagentballoon--getvisible.md)                 | Devuelve la configuración de visibilidad para el globo de palabras.                                  |
| [SetFontName](iagentballoon--setfontname.md)               | Establece la fuente utilizada en el globo de palabras.                                               |
| [SetFontSize](iagentballoon--setfontsize.md)               | Establece el tamaño de fuente utilizado en el globo de palabras.                                          |
| [SetFontCharSet](iagentballoon--setfontcharset.md)         | Establece el juego de caracteres utilizado en el globo de palabras.                                      |
| [GetFontCharSet](iagentballoon--getfontcharset.md)         | Devuelve el juego de caracteres utilizado en el globo de palabras.                                   |



 

 

 