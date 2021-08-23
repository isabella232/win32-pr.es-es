---
title: Usar el elemento Textbox
description: Usar el elemento Textbox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Taller web, elemento de cuadro de texto
- diseñar páginas web, elemento de cuadro de texto
- Lenguaje de marcado de vectores (VML),elemento textbox
- VML (Lenguaje de marcado de vectores),elemento de cuadro de texto
- vector graphics,textbox element
- elemento textbox
- Elementos VML, cuadro de texto
- Formas de VML, elemento de cuadro de texto
- Lenguaje de marcado de vectores (VML), adjuntar texto
- VML (Lenguaje de marcado de vectores), adjuntar texto
- gráficos vectoriales, adjuntar texto
- Formas de VML, adjuntar texto
- adjuntar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a9b4cb0b9096777a017dafd7df1c738621a4d5681ac3228741b3fd30386ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512635"
---
# <a name="using-the-textbox-element"></a>Usar el elemento Textbox

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

## <a name="examples"></a>Ejemplos:

Para adjuntar texto a un rectángulo, puede escribir las líneas siguientes en la `<BODY>` región de la página web:


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





Para adjuntar un hipervínculo a un rectángulo redondeado con relleno de degradado, puede escribir las líneas siguientes en la `<BODY>` región de la página web:

![textbox2.gif (1147 bytes)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





Para obtener más información sobre este elemento, consulte la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .

 

 