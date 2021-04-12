---
title: El objeto Balloon
description: El objeto Balloon
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270905"
---
# <a name="the-balloon-object"></a>El objeto Balloon

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El agente de Microsoft admite la subtítulos de texto del método [**Speak**](speak-method.md) mediante un globo de palabras de dibujo. El método de [**reflexión**](think-method.md) le permite mostrar texto sin salida de audio en un globo de palabra "pensamiento".

Los valores predeterminados de la ventana de globo de palabras iniciales de un carácter se definen y compilan en el editor de caracteres del agente de Microsoft. Una vez que se ejecuta, el usuario puede invalidar las propiedades [**habilitadas**](enabled-property.md) y de [**fuente**](https://www.bing.com/search?q=**Font**) del globo. Si un usuario cambia las propiedades del globo de palabras, afectan a todos los caracteres. Tanto el globo de palabras [**Speak**](speak-method.md) como el de [**reflexión**](think-method.md) usan la misma configuración de propiedades para el tamaño. Puede tener acceso a las propiedades del globo de palabras de un carácter a través del objeto de [**globo**](/windows/desktop/lwef/the-balloon-object) , que es un elemento secundario del objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) .

El objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) admite las siguientes propiedades:

-   [**BackColor**](backcolor-property.md)
-   [**BorderColor**](bordercolor-property.md)
-   [**CharsPerLine**](charsperline-property.md)
-   [**habilitado**](enabled-property.md)
-   [**FontCharSet**](fontcharset-property.md)
-   [**FontName**](fontname-property-bal.md)
-   [**FontBold**](fontbold-property.md)
-   [**FontItalic**](fontitalic-property.md)
-   [**FontSize**](fontsize-property-bal.md)
-   [**FontStrikeThru**](fontstrikethru-property.md)
-   [**FontUnderline**](fontunderline-property.md)
-   [**ForeColor**](forecolor-property.md)
-   [**NumberOfLines**](numberoflines-property.md)
-   [**Estilo**](style-property.md)
-   [**Visible**](visible-property-bal.md)

 

 