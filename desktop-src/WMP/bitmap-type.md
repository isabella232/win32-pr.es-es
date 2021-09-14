---
title: Tipo de mapa de bits
description: Tipo de mapa de bits
ms.assetid: 208df4b9-d1be-49ff-bc0b-2e000608e9c7
keywords:
- Reproductor de Windows Media Máscaras móviles, mapas de bits
- máscaras, mapas de bits
- referencia de máscaras, mapas de bits
- mapas de bits en máscaras, tipos
- mapas de bits en máscaras, valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602a436b5f4428b897672607265098104a9c1b0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243297"
---
# <a name="bitmap-type"></a>Tipo de mapa de bits

En la tabla siguiente se muestran los valores que son válidos para el tipo de mapa de bits. Solo se requiere el tipo Background; otras son opcionales y están relacionadas con diferentes usos posibles de imágenes.



| Value       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fondo  | Necesario. Imagen en la que se superponen todas las imágenes de botón. Las dimensiones de la imagen de fondo base incluyen el ancho completo y el alto de la pantalla. Este es también el archivo donde se muestran las imágenes de los estados naturales de los botones y las barras de seguimiento. (Los botones presionados y deshabilitados no forman parte de esta imagen).                                                                                                                                                                                                                                                                                           |
| Disabled    | Necesario. Indica que insertar el botón no tendrá ningún efecto. Define una imagen que se muestra cuando una funcionalidad específica del reproductor no está disponible para el usuario. Debe proporcionar un valor De coordenadas para indicar la posición de la esquina superior izquierda de esta imagen con respecto a la imagen de fondo.                                                                                                                                                                                                                                                                                                                |
| Empujado      | Necesario. Define una imagen que se muestra cuando el usuario presiona un botón. Use Pushed para proporcionar comentarios visuales al usuario cuando pulse un botón. Debe proporcionar un valor De coordenadas para indicar la posición de la esquina superior izquierda de esta imagen con respecto a la imagen de fondo.                                                                                                                                                                                                                                                                                                                              |
| Region      | Define imágenes que usan regiones de color para representar el área de respuesta de pulsación para los botones de tipo de pulsación: PushHit, ToggleHit, 2PushHit. Si usa los botones de tipo de llamada, debe proporcionar una imagen de región. Este archivo de imagen usa colores Windows paleta específica para cada control. Los colores se definen mediante números que representan el valor de rojo, verde y azul para la región. El usuario nunca ve esta imagen. También debe proporcionar un valor coordenadas para indicar la posición de la esquina superior izquierda de esta imagen con respecto a la imagen de fondo.                                                      |
| SeekThumb   | Define una imagen que usará junto con una barra de seguimiento para indicar la posición actual en el elemento multimedia. Por ejemplo, si una canción ha terminado de reproducirse a la mitad, la imagen SeekThumb se muestra en medio de la barra de seguimiento. Al pulsar y arrastrar la imagen SeekThumb, el usuario puede reiniciar el elemento multimedia en cualquier posición, lo que se denomina *buscar*. La imagen de la propia barra de seguimiento se define en la imagen De fondo. La imagen SeekThumb no se incluye en la sección Mapas de bits del archivo de definición de máscara, pero se especifica como parte de la definición de la barra de seguimiento en la sección TrackBars. |
| Super       | Define la imagen Deshabilitada para una barra de seguimiento. También puede contener imágenes alternativas para el botón de exclusión mutua.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| VolumeThumb | Define una imagen que se va a usar junto con una barra de seguimiento para indicar la posición del volumen. Al pulsar y arrastrar la imagen VolumeThumb, el usuario puede cambiar el nivel de volumen. La imagen de la propia barra de seguimiento se define en la imagen De fondo. La imagen VolumeThumb no se incluye en la sección Mapas de bits del archivo de definición de máscara, pero se especifica como parte de la definición de la barra de seguimiento en la sección TrackBars.                                                                                                                                                                                      |



 

> [!Note]  
> Los tipos region y Super bitmap están en desuso en máscaras para Reproductor de Windows Media 10 Mobile o posterior.

 

Tenga en cuenta que el nombre de archivo y el tipo de archivo no son necesariamente los mismos. Puede llamar al archivo pushed cualquier cosa que quiera, pero todavía se hace referencia a él en otros lugares como Inserción. Por ejemplo, en la sección Botones, tendrá un elemento como:


```C++
Pushed @ 50,60

```



Esto hace referencia al tipo del archivo, no al nombre de archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mapas de bits**](bitmaps.md)
</dt> </dl>

 

 




