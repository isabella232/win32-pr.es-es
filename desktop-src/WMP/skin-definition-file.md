---
title: Archivo de definición de máscara
description: Archivo de definición de máscara
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Reproductor de Windows Media máscaras, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf162870596968872c4f146772c9e62277f5b2ccb660270794248786a71355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995245"
---
# <a name="skin-definition-file"></a>Archivo de definición de máscara

Los archivos de definición de máscara contienen las instrucciones básicas sobre lo que hace la máscara y dónde se pueden encontrar otros archivos usados por la máscara. Solo puede haber un archivo de definición de máscara para una máscara y tiene una extensión de nombre de archivo .wms.

Las instrucciones del archivo de definición de máscara se escriben lenguaje de marcado extensible (XML), que es similar a HTML. Si ha usado HTML para crear páginas web, verá que XML le resulta familiar.

El XML del archivo de definición de máscara usa un conjunto de etiquetas de elementos especiales para definir partes de la interfaz de usuario de máscara. Por ejemplo, el [elemento BUTTON](button-element.md) define cómo se comportará un botón, dónde irá y cómo será.

Cada etiqueta de elemento tiene atributos específicos. Por ejemplo, el [elemento BUTTON](button-element.md) tiene un **atributo image** que define dónde se puede encontrar la imagen del botón. Esto es similar a HTML, donde el elemento BODY tendrá un atributo **bgcolor** que define el color de fondo de la página HTML. En la sección Referencia de programación de máscara se incluye información [detallada](skin-programming-reference.md) sobre todos los elementos de máscara y sus atributos.

XML tiene algunas reglas sencillas que debe conocer para crear máscaras. A diferencia de HTML, XML requiere que siga exactamente las reglas.

## <a name="enclose-elements-with-angle-brackets"></a>Incluir elementos con corchetes angulares

Todos los elementos se incluyen entre corchetes angulares; Por ejemplo, el **elemento BUTTON** tiene el siguiente tipo:


```C++
<BUTTON>

```



No es necesario escribir la palabra "BUTTON" en mayúsculas, pero la convención de escribir nombres de elementos en mayúsculas se usa en el código de ejemplo de este SDK.

## <a name="put-attributes-before-the-closing-bracket"></a>Colocar atributos antes del corchete de cierre

Todos los atributos de un elemento determinado deben incluirse antes del corchete angular de cierre. Un atributo consta del nombre del atributo seguido de un signo igual (=) y el valor del atributo entre comillas.


```C++
<BUTTON image="mypic.jpg">

```



No es necesario escribir la palabra "image" en minúsculas, pero la convención de escribir nombres de atributo en minúsculas se usa en el código de ejemplo de este SDK. Tenga en cuenta también que el valor del atributo está entre comillas.

## <a name="opening-and-closing-elements"></a>Apertura y cierre de elementos

Algunos elementos se agrupan dentro de otro elemento. Por ejemplo, el **elemento BUTTONGROUP** no tiene mucho sentido a menos que use uno o varios **elementos BUTTONELEMENT** con él. Para que la agrupación sea clara, debe tener una etiqueta de apertura y cierre para cada elemento. La etiqueta de apertura es solo el nombre del elemento y los atributos relacionados, entre corchetes angulares. La etiqueta de cierre es el nombre del elemento, precedido por una barra diagonal (/) y, a continuación, entre corchetes angulares. Por ejemplo, la etiqueta de apertura del elemento **BUTTONGROUP** tiene el siguiente aspecto:


```C++
<BUTTONGROUP>

```



La etiqueta **BUTTONGROUP de** cierre tiene el siguiente aspecto:


```C++
</BUTTONGROUP>

```



Colocaría las etiquetas **BUTTONELEMENT** entre las etiquetas de **elemento BUTTONGROUP** de apertura y cierre. Por ejemplo:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>Cerrar elementos

Si un elemento no tiene ningún otro elemento dentro de él, debe colocar una barra diagonal al final del nombre del elemento justo antes del corchete angular de cierre. Por ejemplo, en el código anterior, cada elemento **BUTTONELEMENT** tiene una barra diagonal para indicar que no hay ningún otro elemento anidado en él.

En otras palabras, debe tener una etiqueta de elemento de cierre o cerrar el elemento con una barra diagonal.

Esto es correcto:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Esto no es correcto:


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Esto tampoco es correcto:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



En la sección siguiente se proporciona más información sobre los archivos de definición de máscara:

-   [Estructura del archivo de definición de máscara](skin-definition-file-structure.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de máscara**](skin-files.md)
</dt> </dl>

 

 




