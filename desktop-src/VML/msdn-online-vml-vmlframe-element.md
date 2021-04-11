---
title: Elemento VMLFrame de VML
description: Elemento VMLFrame de VML
ms.assetid: a1582223-d6e2-42d1-95bb-97f6f1d453d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f53371afb0c2790ff6dd666f0121b30b586c51b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149327"
---
# <a name="vml-vmlframe-element"></a>Elemento VMLFrame de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un marco para una forma externa.

Los atributos siguientes modifican un marco.



| Atributo                                     | Descripción                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------|
| [Secuencia](msdn-online-vml-clip-attribute.md)    | Determina si la imagen se va a recortar.                         |
| [Id](id-attribute--vmlframe--vml.md)         | Define un identificador único para el marco.                            |
| [Origen](origin-attribute--vmlframe--vml.md) | Especifica el origen del marco.                                    |
| [Tamaño](size-attribute--vmlframe.md)          | Especifica el tamaño del marco.                                      |
| [Diez](src-attribute--vmlframe--vml.md)       | Especifica el origen de los datos que se mostrarán en el marco. |
| [Estilo](msdn-online-vml-style-attribute.md)  | Define los estilos CSS normales que se pueden usar para colocar el marco. |



 

**Comentarios:**

Los datos de origen que se van a mostrar en el marco pueden estar contenidos en la misma página web o formar parte de otra página. Mediante scripting, el origen se puede cambiar dinámicamente y las características de presentación se pueden modificar.

Los objetos dentro de **VMLFrame** se "amplían". Es decir, se escalan como los metaarchivos, donde los pesos de línea, los desplazamientos de la sombra y el área de texto se escalan proporcionalmente. Esto es diferente de un grupo, donde el tamaño y la posición del objeto se escalan proporcionalmente, pero la línea, la sombra, etc. no lo son.

A continuación se encuentra el código mínimo necesario para cargar una imagen en un marco.


```HTML
   <v:vmlframe
     style="top:1;left:1;width:50;height:50">
     src="external.vml#rect01"/>
   </v:vmlframe>
```



Si el archivo es externo, debe ser un archivo XML. El código siguiente es el código mínimo necesario para especificar un archivo de origen externo que debe contener una forma identificable. Este ejemplo contiene una forma de imagen que muestra un mapa de bits.


```HTML
   <xml xmlns:v = "urn:schemas-microsoft-com:vml">
   <v:image id="rect01"
     style="height:100;width:100;top:50;left:50">
     src="kids.jpg">
   </v:rect>
   </xml>
```



> [!Note]  
> En versiones preliminares de VML, este elemento se llamaba **VMLCanvas** .

 

**Ejemplos**

-   [Ejemplo de VMLFrame simple](/previous-versions/bb263920(v=vs.85))
-   [Ejemplo de VMLFrame dinámico](/previous-versions/bb263902(v=vs.85))

 

 