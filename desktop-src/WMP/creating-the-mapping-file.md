---
title: Crear el archivo de asignación
description: Crear el archivo de asignación
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- crear máscaras, archivos de asignación
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, imágenes de asignación
- Máscaras de Windows Media Player, imágenes de asignación
- máscaras, imágenes de asignación
- asignar imágenes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418380"
---
# <a name="creating-the-mapping-file"></a>Crear el archivo de asignación

Una vez que haya creado las piezas del archivo de imagen principal, es relativamente fácil crear un archivo de asignación. Creará el nuevo archivo de asignación combinando el arte de las dos capas de botones que ya ha creado.

1.  Tendrá que tomar los dos botones que creó para el archivo de imagen principal y copiarlos en una nueva capa. Siga estos pasos: copiar la capa del botón Cerrar, quitar cualquier efecto de capa y cambiarle el nombre a "cerrar mapa". El arte debe ser plano, sin biseles.
2.  Use el selector de colores para crear un color de primer plano de rojo puro. Asegúrese de que el valor del número de color es " \# FF0000". A continuación, use la herramienta Cubo de pintura para rellenar el interior del círculo de la capa de mapa de cierre.
3.  Copie la capa del botón de reproducción, quite los efectos de capa y cambie su nombre por "Play Map". Una vez más, la imagen debe ser plana. No desea ningún efecto en la capa de asignación porque simplemente está definiendo regiones del mapa de bits que Windows Media Player usará para determinar dónde realiza una acción el mouse y qué desea hacer con él.
4.  Use el selector de colores para crear un color de primer plano de verde puro. Asegúrese de que el valor del número de color es " \# 00FF00". A continuación, use la herramienta Cubo de pintura para rellenar el interior del círculo de la capa Play map.

Ahora está listo para crear el archivo de imagen de asignación. Oculte todas las capas y, a continuación, muestre solo las siguientes capas, en este orden (de arriba abajo):

Reproducir asignación

Cerrar mapa

Guarde en un archivo nuevo con el comando Guardar una copia del menú archivo. Seleccione la opción BMP en la parte guardar como del cuadro de diálogo guardar una copia y escriba un nombre de archivo al que se hará referencia más adelante en el archivo de definición de máscara. Idealmente, debería estar en el mismo directorio que el archivo de definición de máscara. Por ejemplo, podría llamar a este archivo map.bmp. Elija la configuración predeterminada y guarde el archivo.

El archivo de asignación debería tener un aspecto similar al de la siguiente ilustración.

![mapping file](images/g01map.png)

Como puede imaginar, el área verde se usará para determinar cuándo se debe iniciar Windows Media Player y el área roja para indicarle que se detenga. Se pueden usar dos colores cualesquiera, siempre que use los números de color al configurar el archivo de definición de máscara. Asegúrese de que los colores del mapa son colores puros para la región que desea usar y que tienen bordes distintos. Un color puro sería aquél en el que cada píxel individual del área tiene el mismo valor de color. El uso de un efecto puede desenfocar o distorsionar el borde, con lo que se modifican ligeramente los colores de algunos de los píxeles. El archivo de asignación solo lo verá el mouse, no un usuario, por lo que no molestarse en decorarlo y quitar cualquier efecto de capa que haya podido haber realizado desde otras capas.

Al guardar el archivo, el nombre de archivo que elija se usará más adelante como el valor del atributo **mappingImage** del elemento **BUTTONGROUP** en el archivo de definición de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de la primera máscara**](building-your-first-skin.md)
</dt> </dl>

 

 




