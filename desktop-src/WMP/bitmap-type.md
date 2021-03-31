---
title: Tipo de mapa de bits
description: Tipo de mapa de bits
ms.assetid: 208df4b9-d1be-49ff-bc0b-2e000608e9c7
keywords:
- Máscaras móviles de Windows Media Player, mapas de bits
- máscaras, mapas de bits
- referencia para máscaras, mapas de bits
- mapas de bits en máscaras, tipos
- mapas de bits en máscaras, valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602a436b5f4428b897672607265098104a9c1b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903457"
---
# <a name="bitmap-type"></a>Tipo de mapa de bits

En la tabla siguiente se muestran los valores que son válidos para el tipo de mapa de bits. Solo se requiere el tipo background. otros son opcionales y se relacionan con los diferentes usos posibles de las imágenes.



| Value       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Información previa  | Obligatorio. Imagen en la que se superponen todas las imágenes de botón. Las dimensiones de la imagen de fondo base incluyen el ancho y el alto completos de la pantalla. Este es también el archivo en el que se muestran las imágenes para los Estados naturales de los botones y trackbars. (Los botones insertar y deshabilitado no forman parte de esta imagen).                                                                                                                                                                                                                                                                                           |
| Disabled    | Obligatorio. Indica que la inserción del botón no tendrá ningún efecto. Define una imagen que se muestra cuando la funcionalidad específica del reproductor no está disponible para el usuario. Debe proporcionar un valor de coordenadas para indicar la posición de la esquina superior izquierda de esta imagen con respecto a la imagen de fondo.                                                                                                                                                                                                                                                                                                                |
| Hacen      | Obligatorio. Define una imagen que se muestra cuando el usuario presiona un botón. Use pushd para proporcionar información visual al usuario cuando pulsa un botón. Debe proporcionar un valor de coordenadas para indicar la posición de la esquina superior izquierda de esta imagen con respecto a la imagen de fondo.                                                                                                                                                                                                                                                                                                                              |
| Region      | Define imágenes que usan regiones en color para representar el área de respuesta de TAP para los botones de tipo de posicionamiento: PushHit, ToggleHit, 2PushHit. Si utiliza los botones de tipo de posicionamiento, debe proporcionar una imagen de región. Este archivo de imagen utiliza colores de paleta de Windows específicos para cada control. Los colores se definen mediante números que representan el valor de rojo, verde y azul para la región. El usuario nunca verá esta imagen. También debe proporcionar un valor de coordenadas para indicar la posición de la esquina superior izquierda de esta imagen con respecto a la imagen de fondo.                                                      |
| SeekThumb   | Define una imagen que se utilizará junto con una barra de contenido para indicar la posición actual en el elemento multimedia. Por ejemplo, si una canción ha terminado de reproducirse, la imagen de SeekThumb se muestra en medio de la barra de presentación. Al pulsar y arrastrar la imagen SeekThumb, el usuario puede reiniciar el elemento multimedia en cualquier posición, lo que se denomina *búsqueda*. La imagen del propio TrackBar se define en la imagen de fondo. La imagen SeekThumb no se incluye en la sección bitmaps del archivo de definición de máscara, pero se especifica como parte de la definición de TrackBar en la sección TrackBars. |
| Super       | Define la imagen deshabilitada para un TrackBar. También puede contener imágenes alternativas para el botón silenciar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| VolumeThumb | Define una imagen que se va a usar junto con una barra de información para indicar la posición del volumen. Al pulsar y arrastrar la imagen VolumeThumb, el usuario puede cambiar el nivel de volumen. La imagen del propio TrackBar se define en la imagen de fondo. La imagen VolumeThumb no se incluye en la sección bitmaps del archivo de definición de máscara, pero se especifica como parte de la definición de TrackBar en la sección TrackBars.                                                                                                                                                                                      |



 

> [!Note]  
> Los tipos region y Super Bitmap están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior.

 

Tenga en cuenta que el nombre de archivo y el tipo de archivo no son necesariamente los mismos. Puede llamar al archivo insertado con todo lo que quiera, pero todavía se hace referencia a él en otros lugares como insertado. Por ejemplo, en la sección botones, tendrá un elemento como:


```C++
Pushed @ 50,60

```



Esto hace referencia al tipo del archivo, no al nombre de archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mapas de bits**](bitmaps.md)
</dt> </dl>

 

 




