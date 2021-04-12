---
title: Crear la imagen de desplazamiento
description: Crear la imagen de desplazamiento
ms.assetid: 169a99ba-96a0-4487-aa1c-07c83c0bc237
keywords:
- crear máscaras, desplazar imágenes
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, imágenes de desplazamiento
- Máscaras de Windows Media Player, imágenes de desplazamiento
- máscaras, imágenes de desplazamiento
- desplazar imágenes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d7f5bbb8b57820c2805b9b9d6ea79762933035
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356731"
---
# <a name="creating-the-hover-image"></a>Crear la imagen de desplazamiento

La imagen principal de esta máscara es dos botones que se encuentran en una elipse. Para proporcionar al usuario una pista sobre lo que debe hacer, puede Agregar imágenes de mantener el mouse. Se trata de imágenes alternativas que se muestran cuando el usuario mantiene el mouse sobre un botón. Los botones de desplazamiento también contendrán los símbolos de control VCR Play y STOP para que los usuarios sepan exactamente lo que pueden hacer. El uso de imágenes de desplazamiento le permite crear máscaras artísticas y de documentos complejos.

Para crear la imagen de mantener el mouse, deberá tomar los dos botones que creó para el archivo de imagen principal, copiarlos en nuevas capas y agregar más capas para el texto. Siga estos pasos:

1.  Copie la capa del botón Cerrar y cambie su nombre por "cerrar el puntero".
2.  Use el selector de colores para crear un color de primer plano de un amarillo claro ( \# CCFF33). Esto se eligió para contrastar con los colores del botón. A continuación, use la herramienta Cubo de pintura para rellenar el interior del círculo en la capa de cierre del mouse.
3.  Copie la capa del botón de reproducción y cambie su nombre por "reproducir el puntero".
4.  Use la herramienta Cubo de pintura para rellenar el interior del círculo en la capa de activación de la reproducción con el mismo color que el círculo de cierre del mouse.
5.  Cree una nueva capa y asígnele el nombre "cerrar cuadrado". Use el selector de colores para crear un color de primer plano de azul marino. Use la herramienta pluma para dibujar un cuadrado, convertirlo en una selección, rellenarlo y eliminar la ruta de acceso. Use la herramienta mover para mover el cuadrado y centrarlo sobre el botón Cerrar.
6.  Cree una nueva capa y asígnele el nombre "Play Triangle". Use la herramienta pluma para crear el triángulo para "reproducir" con las mismas técnicas que hizo para crear la capa cuadrada de cierre. Centre en el botón de reproducción.

Ahora está listo para crear el archivo de imagen emergente. Oculte todas las capas y, a continuación, muestre solo las siguientes capas, en este orden (de arriba abajo):

Reproducir triángulo

Cerrar cuadrado

Mantener el mouse

Cerrar mantenga el mouse

Guarde en un archivo nuevo con el comando Guardar una copia del menú archivo. Seleccione la opción BMP en la parte guardar como del cuadro de diálogo guardar una copia y escriba un nombre de archivo al que se hará referencia más adelante en el archivo de definición de máscara. Idealmente, debe guardarlo en el mismo directorio que el archivo de definición de máscara. Por ejemplo, podría llamar a este hover.bmp. Elija la configuración predeterminada y guarde el archivo.

El archivo de imagen emergente debe tener un aspecto similar al de la siguiente ilustración.

![imagen de desplazamiento](images/absam01h.png)

El botón de desplazamiento amarillo se mostrará en lugar del botón normal. Si mantiene el mouse sobre el botón derecho de la máscara, aparecerá el botón amarillo con la etiqueta "reproducir" y, si mantiene el mouse sobre el botón izquierdo, el usuario verá "cerrar". Las dos imágenes de desplazamiento nunca se mostrarán al mismo tiempo, ya que el mouse no puede mantener el puntero sobre ambos botones al mismo tiempo. Debe activar el desplazamiento y tener un archivo de imagen emergente que coincida con las áreas de los archivos de asignación en áreas del archivo que mantiene el mouse.

Al guardar el archivo, el nombre de archivo que elija se usará más adelante como el valor del atributo **hoverImage** del elemento **BUTTONGROUP** en el archivo de definición de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de la primera máscara**](building-your-first-skin.md)
</dt> </dl>

 

 




