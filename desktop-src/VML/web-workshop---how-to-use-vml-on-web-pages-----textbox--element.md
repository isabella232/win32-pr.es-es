---
title: Usar el elemento TextBox
description: Usar el elemento TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Web Workshop, elemento TextBox
- diseñar páginas web, elemento TextBox
- Lenguaje de marcado de vectores (VML), elemento TextBox
- VML (Lenguaje de marcado de vectores), elemento TextBox
- gráficos vectoriales, elemento TextBox
- Elemento TextBox
- Elementos VML, TextBox
- Formas VML, elemento TextBox
- Lenguaje de marcado de vectores (VML), adjuntar texto
- VML (Lenguaje de marcado de vectores), adjuntar texto
- gráficos vectoriales, adjuntar texto
- Formas VML, adjuntar texto
- Adjuntar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488223"
---
# <a name="using-the-textbox-element"></a>Usar el elemento TextBox

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

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





Para adjuntar un hipervínculo a un rectángulo redondeado con relleno degradado, puede escribir las líneas siguientes en la `<BODY>` región de la página web:

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





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .

 

 