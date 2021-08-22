---
title: Ejemplo de arte simple
description: Ejemplo de arte simple
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Reproductor de Windows Media máscaras, archivos art
- skins,art files
- archivos para máscaras, arte
- archivos de arte para máscaras, ejemplos
- Reproductor de Windows Media máscaras, ejemplos
- máscaras, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbd50cb4ad0dbd76babd99439a885f9e77557d04e18f2698bb970effa23d6b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615969"
---
# <a name="simple-art-example"></a>Ejemplo de arte simple

Se necesitan tres archivos de arte para crear una máscara sencilla con dos botones. Se requieren una imagen principal y una imagen de asignación, y una imagen alternativa proporciona una indicación visual al usuario de que se puede hacer clic en un botón.

Estos archivos de arte se crearon en un programa de arte que usa capas. El uso de capas facilita la seguridad de que las imágenes principales, de asignación y alternativas tienen el mismo tamaño y se alinean entre sí.

Las instrucciones detalladas sobre cómo crear el arte se encuentran en la [Guía de creación de máscaras](skin-creation-guide.md).

## <a name="primary-image"></a>Imagen principal

La imagen principal es un óvalo amarillo simple con dos botones, uno rosa para iniciar Reproductor de Windows Media y un botón púrpura para detenerla. El fondo es un amarillo ligeramente más oscuro que el óvalo. Esta imagen se muestra en la ilustración siguiente.

![imagen principal](images/absam01b.png)

La imagen principal era de las siguientes imágenes, cada una en una capa independiente. En primer lugar, se creó un óvalo con un bisel de capa y un efecto de relieve. Esta imagen se muestra en la ilustración siguiente.

![imagen oval](images/absam01s.png)

A continuación, se crearon los dos botones, también con efectos de bisel de capa y relieve. Esto se muestra en la siguiente ilustración.

![dos botones](images/absam01p.png)

A continuación, se creó el fondo de la imagen. Se eligió un amarillo ligeramente más oscuro para que no se note ningún suavizado de suavizado entre el óvalo y el fondo. El valor de color \# esCCIC00. Esta imagen se muestra en la ilustración siguiente.

![imagen de fondo](images/absam01y.png)

Las capas que contenían estas imágenes se hicieron visibles y se guardaron como una copia en formato de mapa de bits, creando la imagen principal. El atributo **backgroundImage** del **elemento VIEW** usará la imagen compuesta principal.

## <a name="mapping-image"></a>Imagen de asignación

Se necesita una imagen de asignación para especificar cuándo y dónde se hace clic en una máscara. Se creó una imagen de asignación con un área roja y un área verde. Esta imagen se muestra en la ilustración siguiente.

![imagen de asignación](images/absam01m.png)

El área verde se usará para identificar el área de la máscara que se iniciará Reproductor de Windows Media y el área roja se usará para detenerla. La imagen de asignación tiene el mismo tamaño que la imagen principal.

La imagen de asignación se creó copiando la capa de botón en una nueva capa y desactivando el efecto bisel y relieve. Las imágenes planas son necesarias para la asignación porque Reproductor de Windows Media buscará valores de color único en cada área. Solo puede buscar un color definido, como rojo \# (FF0000). Si la imagen tiene un bisel u otro efecto, no todo será el rojo exacto que necesita.

Para que los botones de asignación sean un color fácil de recordar, las imágenes se rellenaron con rojo puro y verde puro, pero se puede usar cualquier color. Deberá recordar los números de color del mapa para que se puedan especificar en el archivo de definición de máscara XML. En este caso, el rojo es \# FF0000 y el verde \# es 00FF00.

A continuación, con solo la nueva capa visible, la imagen se guardó como una copia en un archivo BMP. Lo llamará el atributo **mappingImage** del **elemento BUTTONGROUP.**

## <a name="alternate-image"></a>Imagen alternativa

Las imágenes alternativas no son necesarias, pero son muy útiles para proporcionar indicaciones visuales al usuario. En este caso, se recomienda mantener el puntero sobre la imagen para que el usuario sepa en qué áreas se puede hacer clic.

Se creó una imagen alternativa con dos botones amarillos. Esto se muestra en la siguiente ilustración.

![mantener el puntero de la imagen](images/absam01h.png)

La imagen alternativa se creó copiando la capa de botón original en una nueva capa y, a continuación, cambiando el color de relleno a amarillo. Se ha mantenido el efecto bisel y relieve. A continuación, se creó una nueva capa y se agregaron imágenes: la flecha indica "play" y el cuadrado indica "stop". A continuación, con solo el nuevo botón amarillo y las capas de tipo visibles, la imagen se guardó como una copia en un archivo de mapa de bits.

El resultado es que, cuando el mouse mantiene el mouse sobre un área definida por la imagen de asignación, se muestra la imagen con el mouse, lo que alerta al lector de que, si hace clic en ese punto, puede reproducir o detener Reproductor de Windows Media.

## <a name="final-image"></a>Imagen final

Esta es la imagen final de la máscara.

![imagen final](images/absam01f.png)

Y esta es la imagen que verá si mantiene el puntero sobre el botón rosa de la derecha.

![mantener el puntero sobre el botón derecho](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>Código XML para el ejemplo de arte

Los detalles de cómo escribir código [](skin-creation-guide.md)XML se indican en la Guía de creación de máscaras, pero para mostrar lo poco que se necesita código para crear una máscara de trabajo, este es el código de las ilustraciones de este ejemplo.

Los botones predefinidos se usan para las funciones de reproducción y de detenerse. Debe cargar un archivo o una lista de reproducción desde el delimitador Windows media. Cuando Reproductor de Windows Media cambia al modo de máscara, aparece un cuadro pequeño en la esquina inferior derecha de la pantalla. Este cuadro se denomina "delimitador". Al hacer clic en el delimitador se proporciona la funcionalidad mínima necesaria, en caso de que una máscara no proporcione una manera de volver al modo completo de Reproductor de Windows Media. El usuario puede cambiar entre  modos mediante el menú Ver si está en modo completo o haciendo clic en el delimitador si está en modo de máscara.


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de arte**](art-files.md)
</dt> </dl>

 

 




