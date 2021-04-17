---
title: Archivo de definición de máscara
description: Archivo de definición de máscara
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Aspectos de Windows Media Player, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704725"
---
# <a name="skin-definition-file"></a>Archivo de definición de máscara

Los archivos de definición de máscara contienen las instrucciones básicas sobre lo que hace la máscara y dónde se pueden encontrar otros archivos usados por la máscara. Solo puede haber un archivo de definición de máscara para una máscara y una extensión de nombre de archivo. WMS.

Las instrucciones del archivo de definición de máscara se escriben en lenguaje de marcado extensible (XML), que es similar a HTML. Si ha usado HTML para crear páginas web, verá que XML resulta familiar.

El XML en el archivo de definición de máscara utiliza un conjunto de etiquetas de elementos especiales para definir partes de la interfaz de usuario de máscara. Por ejemplo, el elemento [Button](button-element.md) define cómo se comportará un botón, dónde irá y cuál será el aspecto.

Cada etiqueta de elemento tiene atributos específicos. Por ejemplo, el elemento [Button](button-element.md) tiene un atributo **Image** que define dónde se puede encontrar la imagen del botón. Esto es similar a HTML, donde el elemento BODY tendrá un atributo **bgcolor** que define el color de fondo de la página HTML. En la sección [referencia de programación](skin-programming-reference.md) de la máscara se incluye información detallada sobre todos los elementos de máscara y sus atributos.

XML tiene algunas reglas sencillas que debe conocer para crear máscaras. A diferencia de HTML, XML requiere que siga las reglas exactamente.

## <a name="enclose-elements-with-angle-brackets"></a>Incluir elementos con corchetes angulares

Todos los elementos se incluyen entre corchetes angulares. por ejemplo, el elemento de **botón** se escribe de la siguiente manera:


```C++
<BUTTON>

```



No es necesario escribir la palabra "BUTTON" en mayúsculas, pero la Convención de escribir nombres de elementos en mayúsculas se usa en el código de ejemplo de este SDK.

## <a name="put-attributes-before-the-closing-bracket"></a>Colocar atributos antes del corchete de cierre

Todos los atributos de un elemento determinado deben incluirse antes del corchete angular de cierre. Un atributo consta del nombre del atributo seguido de un signo igual (=) y el valor del atributo entre comillas.


```C++
<BUTTON image="mypic.jpg">

```



No es necesario escribir la palabra "imagen" en minúsculas, pero la Convención de escribir nombres de atributo en minúsculas se usa en el código de ejemplo de este SDK. Tenga en cuenta también que el valor del atributo está entre comillas.

## <a name="opening-and-closing-elements"></a>Abrir y cerrar elementos

Algunos elementos se agrupan dentro de otro elemento. Por ejemplo, el elemento **BUTTONGROUP** no tiene mucho sentido a menos que use uno o varios elementos **BUTTONELEMENT** con él. Para que la agrupación sea clara, debe tener una etiqueta de apertura y de cierre para cada elemento. La etiqueta de apertura es solo el nombre de elemento y los atributos relacionados, rodeados por corchetes angulares. La etiqueta de cierre es el nombre del elemento, precedido por una barra diagonal (/) y, a continuación, entre corchetes angulares. Por ejemplo, la etiqueta de apertura del elemento **BUTTONGROUP** tiene el siguiente aspecto:


```C++
<BUTTONGROUP>

```



La etiqueta **BUTTONGROUP** de cierre tiene el siguiente aspecto:


```C++
</BUTTONGROUP>

```



Colocaría las etiquetas **BUTTONELEMENT** entre las etiquetas de elemento **BUTTONGROUP** de apertura y cierre. Por ejemplo:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>Cerrar elementos

Si un elemento no tiene ningún otro elemento dentro de él, debe colocar una barra diagonal al final del nombre del elemento justo antes del corchete angular de cierre. Por ejemplo, en el código anterior, cada elemento **BUTTONELEMENT** tiene una barra diagonal para indicar que no hay otros elementos anidados en él.

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



En la sección siguiente se proporciona más información acerca de los archivos de definición de máscara:

-   [Estructura del archivo de definición de máscara](skin-definition-file-structure.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de máscara**](skin-files.md)
</dt> </dl>

 

 




