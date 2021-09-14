---
title: Creación del archivo de imagen principal
description: Creación del archivo de imagen principal
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- crear máscaras, archivos de arte primarios
- Reproductor de Windows Media máscaras,archivos art
- skins,art files
- archivos para máscaras, art
- archivos de arte para máscaras, imágenes principales
- Reproductor de Windows Media máscaras,imágenes principales
- máscaras, imágenes principales
- imágenes principales en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967623"
---
# <a name="creating-the-primary-art-file"></a>Creación del archivo de imagen principal

El archivo de arte principal contendrá el arte que el usuario de la máscara ve primero. En este caso, va a crear imágenes en diferentes capas del programa de arte. El motivo del uso de capas es que copiará capas específicas más adelante para crear archivos de mapa y archivos de arte alternativos.

Para crear el archivo de ilustración principal, creará las capas siguientes en el orden siguiente:

Capa de fondo de máscara

Este es el color que será transparente cuando se muestre la máscara. Cree primero una capa para esta capa, pero elija el color final de esta capa después de elegir un color para la capa de contenedor de máscara. Este color debe ser similar a la capa del contenedor de máscaras, pero no igual a la capa de contenedor de máscara, para ocultar los efectos de suavizado de alias.

Capa de contenedor de máscara

Esta es la imagen que formará el contorno de la máscara y será lo que el usuario vea. También será el contenedor de los dos botones de este ejemplo. Piense en la máscara como un contenedor para los controles de la interfaz de usuario, como botones, controles deslizantes, entre otros. En este ejemplo, el contenedor es un óvalo amarillo.

Reproducir y cerrar capas de botón

Estos son los dos controles de interfaz de usuario que usa este ejemplo. Las colocará en capas independientes para que pueda ajustarlas fácilmente o copiarlas más adelante.

Antes de crear las capas, debe crear el archivo que contendrán las capas. Inicie Photoshop y cree un nuevo archivo de 100 píxeles de alto y 200 píxeles de ancho. El archivo que se usa para crear el arte de este ejemplo se denomina tiny.psd y se incluye con el SDK.

Todas las instrucciones se proporcionan en términos de Photoshop, pero cualquier otro programa de arte se puede usar para crear máscaras siempre y cuando se pueda guardar en uno de los formatos de archivo compatibles con Reproductor de Windows Media (BMP, GIF, JPG y PNG). La creación de máscaras le será más fácil si usa un programa de arte que tiene capas, como Adobe Photoshop, Jasc Paint Shop Pro o Jedor Sedán. Las capas son muy útiles porque las imágenes deben estar correctamente alineadas para la asignación de imágenes y la presentación de imágenes alternativas.

## <a name="skin-background-layer"></a>Capa de fondo de máscara

Cree una nueva capa y asízcála como "Fondo de máscara". Se convertirá en el color de transparencia que definirá en el archivo de definición de máscara. Espere hasta que se elija el color del contenedor de máscaras antes de rellenar la capa de fondo de la máscara con un color específico.

## <a name="skin-container-layer"></a>Capa de contenedor de máscara

A continuación, cree una capa y llámela "Contenedor de máscaras". Esto definirá los bordes de la máscara y será el contenedor de los botones.

Elija un color de primer plano para la forma mediante los controles deslizantes de color web. En este ejemplo, se eligió el color \# "DBDD11".

A continuación, cree una forma ovalada. La manera más fácil es usar la herramienta Marquee elíptico y crear una selección ovalada. Cuando haya creado una selección ovalada que sea el tamaño y la forma que desee, rellene la selección con el color de primer plano y cancele la selección.

Por último, para que parezca un poco más interesante, aplique el efecto de capa de Bisel y Relieve con los valores predeterminados.

La capa del contenedor de máscara debe tener un aspecto parecido al de la ilustración siguiente.

![capa de contenedor de máscara](images/g01cont.png)

## <a name="background-skin-color"></a>Color de la máscara de fondo

Ahora que ha elegido un color de primer plano para la forma del contenedor de máscaras, puede elegir un color similar para la capa de fondo de la máscara. No quiere el mismo color exacto o el contenedor de máscaras también será transparente. De hecho, asegúrese de no usar este color exacto en ningún otro lugar de la máscara, incluso en fotografías, porque dondequiera que aparezca este color, la imagen de escritorio aparecerá en su lugar.

Quiere un color cercano al color del contenedor de máscaras para evitar efectos de suavizado de alias. Por ejemplo, si tiene un fondo negro, es posible que algunos bits de negro se muestren alrededor del borde de la máscara. Al elegir un color cercano al color del contenedor de máscaras, los píxeles perdidos que se muestren en el proceso de suavizado de alias pasarán desapercibido.

El suavizado de contorno es el proceso de suavizado de los bordes de formas inclinadas o curvadas. El suavizado de contorno crea nuevos colores, para píxeles a lo largo de los bordes de una forma, que son una combinación del color de primer plano y el color de fondo. Algunos de estos colores entre ellos pueden hacer que se falte píxeles cuando el color de fondo se hace transparente.

La capa de fondo de la máscara debe tener un aspecto parecido al de la ilustración siguiente.

![capa de máscara de fondo](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Reproducir y cerrar capas de botón

Cree una capa y asízcála como "Botón Cerrar". Con la herramienta de selección marquesina elíptica de nuevo, cree un círculo y posiciones en el lado izquierdo de la imagen general. Active la visibilidad del archivo de contenedor de máscaras para ayudar a colocar la selección.

Cuando esté satisfecho con la colocación, rellene la selección con cualquier color (excepto el color del contenedor de máscaras o el fondo de la máscara). En este ejemplo, se ha elegido un color púrpura. No es necesario recordar el número del color. A continuación, cancele la selección y aplique otro efecto de capa biselado y relieve predeterminado. Si desea aplicar efectos que no son de capa al botón, realice una copia del original para su uso posterior en la asignación.

El botón Cerrar debe tener un aspecto parecido al de la ilustración siguiente.

![botón Cerrar](images/g01qbut.png)

Cree una nueva capa y asízguela como "Botón de reproducción". Use las mismas técnicas que hizo para el botón Cerrar, pero asínciele un color diferente. En este caso, se eligió un color de botón de color rosa, pero se puede usar cualquier color siempre que no sea el mismo color que el contenedor de máscaras (porque se combinaría en el contenedor) o el color de fondo de la máscara (porque se convertiría en transparente).

El botón Reproducir debe tener un aspecto parecido al de la ilustración siguiente.

![botón de reproducción](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Combinar capas y guardar

Ya está listo para crear el archivo de arte principal. Oculte todas las capas y, a continuación, muestre solo las siguientes capas, en este orden (de arriba abajo):

Botón de reproducción

Botón Cerrar

Contenedor de máscaras

Fondo de máscara

Guarde en un archivo nuevo mediante el comando Guardar una copia del menú Archivo. Seleccione la opción BMP en la parte Guardar como del cuadro de diálogo Guardar una copia y escriba un nombre de archivo al que haga referencia más adelante en el archivo de definición de máscara. Lo ideal es guardar esto en el mismo directorio que el archivo de definición de máscara. Por ejemplo, podría llamar a este background.bmp. Elija la configuración predeterminada y guarde el archivo.

El archivo de arte principal debe tener este aspecto:

![archivo de arte principal](images/g01prime.png)

Usará este nombre de archivo como valor para el atributo **backgroundImage** del **elemento VIEW** en el archivo de definición de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de la primera máscara**](building-your-first-skin.md)
</dt> </dl>

 

 




