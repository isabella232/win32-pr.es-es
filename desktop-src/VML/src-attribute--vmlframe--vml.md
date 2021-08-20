---
title: Atributo Src (VMLFrame)(VML)
description: Atributo Src (VMLFrame)(VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f7761a55304eefc655d00ed58d84b7af8f7ce5daf86a3aaf462308b43c193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057592"
---
# <a name="src-attribute-vmlframevml"></a>Atributo Src (VMLFrame)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el origen de datos para el marco. Lectura/escritura **Cadena**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *element* src=" *expression* ">

**Sintaxis de script**

*Element* .src="*expression*"

*expresión* = *elemento*.src

**Comentarios:**

El **atributo Src** puede implicar las sintaxis siguientes:

-   Dirección URL al archivo externo. El archivo debe ser un archivo XML con el formato siguiente:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   Dentro del archivo debe tener una o varias formas de VML con identificadores válidos a los que se puede hacer referencia mediante esta sintaxis:
    ```HTML
       filename#shapename
    ```

    

-   En la siguiente referencia, los archivos externos tienen la extensión .vml, pero se puede usar cualquier extensión:
    ```HTML
       external.vml#image01
    ```

    

-   Puede hacer referencia a una forma dentro del mismo archivo mediante la sintaxis siguiente:
    ```HTML
       #shapename
    ```

    

Si **Clip** es **False,** la forma se escalará para ajustarse al marco. Si **es True**, no se mostrarán las partes de la forma que estén fuera del marco.

Tenga en cuenta [que Origin](origin-attribute--vmlframe--vml.md) [y Size](size-attribute--vmlframe.md) no se usarán a menos **que Clip** sea **True.**

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



 

 