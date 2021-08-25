---
title: Creación de la imagen de mantener el puntero
description: Creación de la imagen de mantener el puntero
ms.assetid: 169a99ba-96a0-4487-aa1c-07c83c0bc237
keywords:
- crear máscaras, mantener el puntero sobre las imágenes
- Reproductor de Windows Media máscaras, archivos art
- skins,art files
- archivos para máscaras, art
- archivos art para máscaras, imágenes de mantener el mouse
- Reproductor de Windows Media máscaras, mantener el puntero sobre las imágenes
- skins,hover images
- mantener el puntero de las imágenes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88eff91123a28dae94425d7ea6e7591462545a2d7da0372b088eeec6bd67ed60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902285"
---
# <a name="creating-the-hover-image"></a>Creación de la imagen de mantener el puntero

La imagen principal de esta máscara son dos botones sentados en un óvalo. Para proporcionar al usuario una pista sobre lo que debe hacer, puede agregar imágenes de mantener el puntero. Se trata de imágenes alternativas que se muestran cuando el usuario mantiene el mouse sobre un botón. Los botones de mantener el puntero también contendrán los símbolos de control de reproducción y detención de VCR para que los usuarios sepan exactamente lo que pueden hacer. El uso de imágenes de mantener el mouse le permite crear máscaras complejas, auto documentadas y complicadas.

Para crear la imagen de mantener el puntero, deberá tomar los dos botones que creó para el archivo de arte principal, copiarlos en nuevas capas y agregar capas adicionales para el texto. Siga estos pasos:

1.  Copie la capa de botón Cerrar y cámbiele el nombre "Cerrar al mantener el puntero".
2.  Use el Selector de colores para crear un color de primer plano de un amarillo claro \# (CCFF33). Se eligió para contrastar con los colores del botón. A continuación, use Paint bucket para rellenar el interior del círculo en la capa cerrar el mouse.
3.  Copie la capa del botón Reproducir y cámbiele el nombre "Reproducir mantener el puntero".
4.  Use la herramienta Paint Bucket para rellenar el interior del círculo en la capa de mantener el mouse de reproducción con el mismo color que el círculo Cerrar el mouse.
5.  Cree una nueva capa y asízcála como "Cerrar cuadrado". Use el Selector de colores para crear un color de primer plano de azul oscuro. Use la herramienta de lápiz para dibujar un cuadrado, convertirlo en una selección, rellenarlo y eliminar la ruta de acceso. Con la herramienta Mover, mueva el cuadrado y al centro sobre el botón Cerrar.
6.  Cree una nueva capa y asízguela como "Triángulo de reproducción". Use la herramienta de lápiz para crear el triángulo para "Reproducir" con las mismas técnicas que hizo para crear la capa cuadrada Cerrar. Center it over the Play hover button (Centrarlo sobre el botón reproducir).

Ya está listo para crear el archivo de imagen con el puntero del mouse. Oculte todas las capas y, a continuación, muestre solo las siguientes capas en este orden (de arriba abajo):

Triángulo de reproducción

Cerrar cuadrado

Mantener el puntero de reproducción

Cierre el puntero

Guarde en un archivo nuevo mediante el comando Guardar una copia del menú Archivo. Seleccione la opción BMP en la parte Guardar como del cuadro de diálogo Guardar una copia y escriba un nombre de archivo al que haga referencia más adelante en el archivo de definición de máscara. Lo ideal es guardar esto en el mismo directorio que el archivo de definición de máscara. Por ejemplo, podría llamar a este hover.bmp. Elija la configuración predeterminada y guarde el archivo.

El archivo art debe tener un aspecto parecido al de la ilustración siguiente.

![mantener el puntero de la imagen](images/absam01h.png)

El botón de mantener el puntero amarillo se mostrará en lugar del botón normal. Si mantiene el puntero sobre el botón derecho de la máscara, aparecerá el botón amarillo con la etiqueta "Reproducir" y, si mantiene el puntero sobre el botón izquierdo, el usuario verá "Cerrar". Las dos imágenes de mantener el puntero nunca se mostrarán al mismo tiempo, porque el mouse no puede mantener el puntero sobre ambos botones al mismo tiempo. Debe activar el puntero y tener un archivo art que coincida con las áreas de los archivos de asignación a las áreas del archivo de desplazamiento.

Al guardar el archivo, el nombre de archivo que elija se usará más adelante como valor para el atributo **hoverImage** del **elemento BUTTONGROUP** en el archivo de definición de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de la primera máscara**](building-your-first-skin.md)
</dt> </dl>

 

 




