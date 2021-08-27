---
title: El objeto Balloon
description: El objeto Balloon
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc2ad1256b040588121dcb92fc8f66fea540b3051b92a6fe5273eb2f81107b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745977"
---
# <a name="the-balloon-object"></a>El objeto Balloon

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Microsoft Agent admite subtítulos textuales del [**método Speak**](speak-method.md) mediante un globo de palabras. El [**método Think**](think-method.md) permite mostrar texto sin salida de audio en un globo de palabras "pensado".

Los valores predeterminados de la ventana de globo de palabras iniciales de un carácter se definen y compilan en el Editor de caracteres de Microsoft Agent. Una vez en ejecución, el usuario puede reemplazar las propiedades [**Enabled**](enabled-property.md) y [**Font**](https://www.bing.com/search?q=**Font**) del globo. Si un usuario cambia las propiedades de la palabra globo, afecta a todos los caracteres. Los globos de palabras [**Speak**](speak-method.md) y [**Think**](think-method.md) usan la misma configuración de propiedad para el tamaño. Puede acceder a las propiedades de un globo de palabras de un carácter a través del objeto [**Globo,**](/windows/desktop/lwef/the-balloon-object) que es un elemento secundario del [**objeto Character.**](/windows/desktop/lwef/the-characters-object)

El [**objeto Balloon**](/windows/desktop/lwef/the-balloon-object) admite las siguientes propiedades:

-   [**Backcolor**](backcolor-property.md)
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

 

 