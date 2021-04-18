---
title: Crear el archivo de imagen principal
description: Crear el archivo de imagen principal
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- crear máscaras, archivos de imagen principal
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, imágenes principales
- Aspectos de Windows Media Player, imágenes principales
- máscaras, imágenes principales
- imágenes principales en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104554130"
---
# <a name="creating-the-primary-art-file"></a>Crear el archivo de imagen principal

El archivo de imagen principal contendrá el arte que el usuario de la máscara ve en primer lugar. En este caso, creará imágenes en diferentes capas del programa de arte. El motivo del uso de capas es que se copiarán niveles específicos posteriormente para crear archivos de mapa y archivos de imagen alternativos.

Para crear el archivo de imagen principal, creará las siguientes capas en el siguiente orden:

Capa de fondo de máscara

Este es el color que será transparente cuando se muestre la máscara. Cree una capa por primera vez, pero elija el color final de esta capa después de elegir un color para la capa de contenedor de máscara. Este color debe ser similar a, pero no igual que el de la capa de contenedor de máscara, para ocultar los efectos de suavizado de contorno.

Capa de contenedor de máscara

Esta es la imagen que formará el contorno de la máscara y será lo que vea el usuario. También será el contenedor de los dos botones de este ejemplo. Considere la piel como un contenedor para los controles de interfaz de usuario, como botones, controles deslizantes, etc. En este ejemplo, el contenedor es un óvalo amarillo.

Capas de los botones Reproducir y cerrar

Estos son los dos controles de interfaz de usuario que utiliza este ejemplo. Los colocará en capas independientes para que pueda ajustarlos fácilmente o copiarlos más adelante.

Antes de crear las capas, debe crear el archivo que contendrá las capas. Inicie Photoshop y cree un nuevo archivo de 100 píxeles de alto y 200 píxeles de ancho. El archivo que se usa para crear la imagen de este ejemplo se denomina tiny.psd y se incluye con el SDK.

Todas las instrucciones se proporcionan en términos de Photoshop, pero cualquier otro programa de arte se puede usar para crear máscaras siempre que se pueda guardar en uno de los formatos de archivo admitidos por la Media Player de Windows (BMP, GIF, JPG y PNG). Encontrará más fácil la creación de máscaras si usa un programa artístico con capas, como Adobe Photoshop, Jasc Paint Shop Pro o Jedor viscosidad. Las capas son muy útiles porque las imágenes se deben alinear correctamente para la asignación de imágenes y la presentación de imágenes alternativas.

## <a name="skin-background-layer"></a>Capa de fondo de máscara

Cree una nueva capa y asígnele el nombre "fondo de máscara". Se convertirá en el color de transparencia que definirá en el archivo de definición de máscara. Espere hasta que se elija el color del contenedor de máscara antes de rellenar el nivel de fondo de la máscara con un color específico.

## <a name="skin-container-layer"></a>Capa de contenedor de máscara

A continuación, cree una nueva capa y llámela "contenedor de máscara". Esto definirá los bordes de la máscara y será el contenedor de los botones.

Elija un color de primer plano para la forma mediante los controles deslizantes de color Web. En este ejemplo, \# se ha elegido el color "DBDD11".

A continuación, cree una forma ovalada. La manera más fácil es usar la herramienta eliptical marquesina y crear una selección ovalada. Cuando haya creado una selección de óvalo que tenga el tamaño y la forma que desee, rellene la selección con el color de primer plano y cancele la selección.

Por último, para que este aspecto sea un poco más interesante, aplique el efecto de capa de bisel y relieve con los valores predeterminados.

La capa de contenedor de máscara debe ser similar a la siguiente ilustración.

![capa de contenedor de máscara](images/g01cont.png)

## <a name="background-skin-color"></a>Color de máscara de fondo

Ahora que ha elegido un color de primer plano para la forma de contenedor de máscara, puede elegir un color similar para la capa de fondo de la máscara. No desea el mismo color exacto o el contenedor de máscara también será transparente. De hecho, asegúrese de que no usa este color exacto en cualquier parte de la máscara, ni siquiera en fotografías, ya que, siempre que aparezca este color, aparecerá la imagen de escritorio en su lugar.

Desea un color cerca del color del contenedor de máscara para evitar efectos de suavizado de contorno. Por ejemplo, si tiene un fondo negro, algunos bits de negro pueden aparecer en torno al borde de la piel. Al elegir un color cerca del color del contenedor de máscara, los píxeles aislados que se muestran en el proceso de suavizado de contorno no se apreciarán.

El suavizado de contorno es el proceso de suavizar los bordes de las formas inclinadas o curvas. Suavizado de contorno crea nuevos colores, para píxeles a lo largo de los bordes de una forma, que son una combinación del color de primer plano y el color de fondo. Algunos de estos colores, entre otros, pueden provocar que se pierdan los píxeles cuando el color de fondo se hace transparente.

La capa de fondo de la máscara debe ser similar a la siguiente ilustración.

![capa de máscara de fondo](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Capas de los botones Reproducir y cerrar

Cree una nueva capa y asígnele el nombre "botón Cerrar". Con la herramienta de selección de marquesina eliptical, cree un círculo y colóquelo en el lado izquierdo de la imagen global. Active la visibilidad del archivo contenedor de máscara para ayudar a colocar la selección.

Cuando esté satisfecho con la selección de ubicación, rellene la selección con cualquier color (excepto el color del contenedor de máscara o el fondo de la máscara). En este ejemplo, se ha elegido un color púrpura. No es necesario recordar el número del color. A continuación, cancele la selección y aplique otro efecto de la capa de bisel y de relieve predeterminados. Si desea aplicar efectos que no son de capa al botón, haga una copia del original para su uso posterior en la asignación.

El botón Cerrar debe ser similar al de la siguiente ilustración.

![botón Cerrar](images/g01qbut.png)

Cree una nueva capa y asígnele el nombre "botón reproducir". Utilice las mismas técnicas que hizo para el botón Cerrar, pero asígnele un color diferente. En este caso, se ha elegido un color de botón rosa, pero se puede usar cualquier color siempre que no sea el mismo color que el contenedor de máscara (porque se fusionaría en el contenedor) o el color de fondo de la máscara (porque se convertiría en transparente).

El botón de reproducción debería tener un aspecto similar al de la siguiente ilustración.

![botón reproducir](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Combinar capas y guardar

Ahora está listo para crear el archivo de imagen principal. Oculte todas las capas y, a continuación, muestre solo las siguientes capas, en este orden (de arriba abajo):

Botón de reproducción

Botón Cerrar

Contenedor de máscara

Fondo de máscara

Guarde en un archivo nuevo con el comando Guardar una copia del menú archivo. Seleccione la opción BMP en la parte guardar como del cuadro de diálogo guardar una copia y escriba un nombre de archivo al que se hará referencia más adelante en el archivo de definición de máscara. Idealmente, debe guardarlo en el mismo directorio que el archivo de definición de máscara. Por ejemplo, podría llamar a este background.bmp. Elija la configuración predeterminada y guarde el archivo.

El archivo de imagen principal debe tener el siguiente aspecto:

![archivo de imagen principal](images/g01prime.png)

Usará este nombre de archivo como el valor del atributo **BackgroundImage** del elemento **View** en el archivo de definición de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de la primera máscara**](building-your-first-skin.md)
</dt> </dl>

 

 




