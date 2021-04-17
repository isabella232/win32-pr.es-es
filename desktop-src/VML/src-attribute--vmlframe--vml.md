---
title: Atributo src (VMLFrame) (VML)
description: Atributo src (VMLFrame) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359093"
---
# <a name="src-attribute-vmlframevml"></a>Atributo src (VMLFrame) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el origen de datos para el marco. Lectura/escritura **Cadena**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *elemento* src = " *expresión* " >

**Sintaxis de script**

*Element* . src = "*expresión*"

*expresión* = de *elemento*. src

**Comentarios:**

El atributo **src** puede incluir las siguientes sintaxis:

-   Dirección URL del archivo externo. El archivo debe ser un archivo XML con el siguiente formato:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   En el archivo, debe tener una o varias formas de VML con identificadores válidos a los que se pueda hacer referencia mediante esta sintaxis:
    ```HTML
       filename#shapename
    ```

    

-   En la siguiente referencia, los archivos externos tienen la extensión. VML, pero se puede usar cualquier extensión:
    ```HTML
       external.vml#image01
    ```

    

-   Puede hacer referencia a una forma en el mismo archivo utilizando la sintaxis siguiente:
    ```HTML
       #shapename
    ```

    

Si **clip** es **false**, la forma se escalará para ajustarse al marco. Si **es true**, no se mostrarán las partes de la forma que estén fuera del marco.

Tenga en cuenta que el [origen](origin-attribute--vmlframe--vml.md) y [el tamaño](size-attribute--vmlframe.md) no se usarán a menos que el **recorte** sea **true**.

**Atributo estándar de VML**

**Ejemplo**

Se recortará la imagen definida en el archivo externo.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 