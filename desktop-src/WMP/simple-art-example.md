---
title: Ejemplo de arte sencillo
description: Ejemplo de arte sencillo
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, ejemplos
- Aspectos de Windows Media Player, ejemplos
- máscaras, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775546"
---
# <a name="simple-art-example"></a>Ejemplo de arte sencillo

Se necesitan tres archivos de imagen para crear una máscara simple con dos botones. Se requiere una imagen principal y una imagen de asignación, y una imagen alternativa proporciona una indicación visual al usuario de que se hace clic en un botón.

Estos archivos de imágenes se crearon en un programa de arte que usa capas. El uso de capas facilita la tarea de asegurarse de que la imagen principal, la asignación y las imágenes alternativas tienen el mismo tamaño y se alinean entre sí.

Las instrucciones detalladas sobre la creación de material gráfico se encuentran en la [Guía de creación de máscaras](skin-creation-guide.md).

## <a name="primary-image"></a>Imagen principal

La imagen principal es un óvalo amarillo simple con dos botones, uno rosa para iniciar Windows Media Player y el botón púrpura para detenerlo. El fondo es un amarillo ligeramente más oscuro que el óvalo. Esta imagen se muestra en la siguiente ilustración.

![imagen principal](images/absam01b.png)

La imagen principal era de las siguientes imágenes, cada una en una capa independiente. En primer lugar, se creó un óvalo con un efecto de bisel y de relieve de capa. Esta imagen se muestra en la siguiente ilustración.

![imagen ovalada](images/absam01s.png)

A continuación, se crearon los dos botones, también con efectos de bisel y relieve de capa. Esto se muestra en la siguiente ilustración.

![dos botones](images/absam01p.png)

A continuación, se creó el fondo de la imagen. Se ha elegido un amarillo ligeramente más oscuro para que no se detecte ningún suavizado de contorno entre el óvalo y el fondo. El valor de color es \# CCCC00. Esta imagen se muestra en la siguiente ilustración.

![imagen de fondo](images/absam01y.png)

Las capas que contenían estas imágenes se hicieron visibles y se guardan como una copia en formato de mapa de bits, con lo que se crea la imagen principal. El atributo **BackgroundImage** del elemento **View** usará la imagen compuesta principal.

## <a name="mapping-image"></a>Imagen de asignación

Se necesita una imagen de asignación para especificar Cuándo y dónde se hace clic en una máscara. Se creó una imagen de asignación con un área roja y un área verde. Esta imagen se muestra en la siguiente ilustración.

![imagen de asignación](images/absam01m.png)

El área verde se usará para identificar el área de la máscara que iniciará Windows Media Player y se utilizará el área roja para detenerla. La imagen de asignación tiene el mismo tamaño que la imagen principal.

La imagen de asignación se creó copiando la capa de botón en una nueva capa y desactivando el efecto de bisel y relieve. Se necesitan imágenes planas para la asignación, ya que Windows Media Player buscará valores de color único en cada área. Solo puede buscar un color que defina, como rojo ( \# FF0000). Si la imagen tiene un bisel u otro efecto, no todas serán las rojas exactas que necesite.

Para que los botones de asignación sean un color sencillo de recordar, las imágenes se rellenaron con rojo puro y verde puro, pero se puede usar cualquier color. Tendrá que recordar los números de color del mapa para que se puedan escribir en el archivo de definición de máscara XML. En este caso, el color rojo es \# FF0000 y el verde es \# 00FF00.

A continuación, con solo la nueva capa visible, la imagen se guardó como copia en un archivo BMP. Será llamado por el atributo **mappingImage** del elemento **BUTTONGROUP** .

## <a name="alternate-image"></a>Imagen alternativa

No se requieren imágenes alternativas, pero son muy útiles para proporcionar indicaciones visuales al usuario. En este caso, se recomienda una imagen de mantener el mouse para que el usuario sepa en qué áreas se puede hacer clic.

Se creó una imagen alternativa con dos botones amarillos. Esto se muestra en la siguiente ilustración.

![imagen de desplazamiento](images/absam01h.png)

La imagen alternativa se creó copiando la capa de botón original en una nueva capa y, a continuación, cambiando el color de relleno a amarillo. Se mantuvo el efecto de bisel y de relieve. A continuación, se creó una nueva capa y se agregaron imágenes: la flecha indica "reproducir" y el cuadrado indica "detener". A continuación, con solo el nuevo botón amarillo y las capas de tipo visibles, la imagen se guardó como una copia en un archivo de mapa de bits.

El resultado es que cuando el mouse se desplaza sobre un área definida por la imagen de asignación, se muestra la imagen de mantener el puntero, alertar al lector de que si hace clic en ese punto, pueden reproducir o detener Windows Media Player.

## <a name="final-image"></a>Imagen final

Esta es la imagen final de la máscara.

![imagen final](images/absam01f.png)

Y esta es la imagen que verá si mantiene el puntero sobre el botón rosa de la derecha.

![mantener el mouse sobre el botón derecho](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>Código XML para el ejemplo de arte

Los detalles de cómo escribir código XML se proporcionan en la [Guía de creación de máscaras](skin-creation-guide.md), pero para mostrar la cantidad de código que se necesita para crear una máscara de trabajo, este es el código de la ilustración en este ejemplo.

Los botones predefinidos se utilizan para las funciones Play y STOP. Debe cargar un archivo o una lista de reproducción desde el delimitador de Windows Media. Cuando Windows Media Player cambia al modo de máscara, aparece un cuadro pequeño en la esquina inferior derecha de la pantalla. Este cuadro se denomina "delimitador". Al hacer clic en el delimitador, se proporciona la funcionalidad mínima necesaria, en caso de que una máscara no proporcione una manera de volver al modo completo de Windows Media Player. El usuario puede cambiar entre modos mediante el menú **Ver** si está en modo completo o haciendo clic en el delimitador si está en modo de máscara.


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

[**Archivos de imagen**](art-files.md)
</dt> </dl>

 

 




