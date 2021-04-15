---
title: Atributo de destino VML
description: Atributo de destino VML
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676385"
---
# <a name="vml-target-attribute"></a>Atributo de destino VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un marco o una ventana en la que se muestra una dirección URL. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* target = " *expresión* " >

**Comentarios:**

El atributo de **destino** es similar al atributo de **destino** HTML estándar de los delimitadores.

Estos valores incluyen:



| Value      | Descripción                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TargetName | Cadena que contiene el nombre del marco o la ventana en la que se va a cargar el documento.                                                                                                                                                                                 |
| \_en blanco    | Especifica que el documento vinculado se carga en una nueva ventana en blanco. Esta ventana no tiene nombre.                                                                                                                                                                  |
| \_soporte    | A partir de Internet Explorer 6 para Windows XP Service Pack 2, el \_ atributo multimedia está obsoleto y ya no se admite. En primer lugar, disponible en Internet Explorer 6, este valor especifica que el documento vinculado debe cargarse en la barra multimedia.                |
| \_aérea   | Especifica que el documento vinculado se carga en el elemento primario inmediato del documento que contiene el vínculo.                                                                                                                                                      |
| \_buscan   | A partir de Internet Explorer 7 para Windows XP Service Pack 2,: el \_ atributo de búsqueda está obsoleto y ya no se admite. En primer lugar, disponible en Internet Explorer 6, este valor especifica que el documento vinculado se cargará en el panel de búsqueda del explorador. |
| \_self     | Especifica que el documento vinculado se carga en la ventana en la que se hizo clic en el vínculo (la ventana activa).                                                                                                                                                  |
| \_Arriba      | Especifica que el documento vinculado se carga en la ventana de nivel superior.                                                                                                                                                                                            |



 

*Atributo estándar de VML*

**Ejemplo**

Cuando se hace clic en el rectángulo, el explorador carga la Página principal de Microsoft Corporation en la misma ventana.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo de destino](/previous-versions/bb264096(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 