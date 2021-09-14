---
title: Creación del archivo de asignación
description: Creación del archivo de asignación
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- crear máscaras, asignar archivos
- Reproductor de Windows Media máscaras,archivos art
- skins,art files
- archivos para máscaras, art
- archivos de arte para máscaras, imágenes de asignación
- Reproductor de Windows Media máscaras, imágenes de asignación
- máscaras, imágenes de asignación
- asignar imágenes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967620"
---
# <a name="creating-the-mapping-file"></a>Creación del archivo de asignación

Una vez que haya creado las partes del archivo de arte principal, es relativamente fácil crear un archivo de asignación. Creará el nuevo archivo de asignación combinando el arte de las dos capas de botón que ya ha creado.

1.  Tendrá que tomar los dos botones que creó para el archivo de arte principal y copiarlos en una nueva capa. Siga estos pasos: Copie la capa de botón Cerrar, quite los efectos de capa y cambie su nombre a "Cerrar mapa". El arte debe tener un aspecto plano, sin biseles.
2.  Use el Selector de colores para crear un color de primer plano de rojo puro. Asegúrese de que el valor del número de color es \# "FF0000". A continuación, use Paint bucket para rellenar el interior del círculo de la capa cerrar mapa.
3.  Copie la capa del botón Reproducir, quite los efectos de capa y cambie su nombre a "Play map". Una vez más, el arte debería parecer plano. No desea ningún efecto en la capa de asignación porque solo está definiendo las regiones del mapa de bits que Reproductor de Windows Media usará para determinar dónde realiza una acción el mouse y qué quiere hacer con ella.
4.  Use el Selector de colores para crear un color de primer plano de verde puro. Asegúrese de que el valor del número de color es \# "00FF00". A continuación, Paint herramienta Cubo para rellenar el interior del círculo de la capa de mapa de reproducción.

Ya está listo para crear el archivo de representación de asignación. Oculte todas las capas y, a continuación, muestre solo las siguientes capas, en este orden (de arriba abajo):

Mapa de reproducción

Cerrar mapa

Guarde en un archivo nuevo mediante el comando Guardar una copia del menú Archivo. Seleccione la opción BMP en la parte Guardar como del cuadro de diálogo Guardar una copia y escriba un nombre de archivo al que haga referencia más adelante en el archivo de definición de máscara. Lo ideal es que esté en el mismo directorio que el archivo de definición de máscara. Por ejemplo, podría llamar a este archivo map.bmp. Elija la configuración predeterminada y guarde el archivo.

El archivo de asignación debe tener un aspecto parecido al de la ilustración siguiente.

![mapping file](images/g01map.png)

Como puede adivinar, el área verde se usará para determinar cuándo hacer que Reproductor de Windows Media inicio y el área roja es para que se detenga. Se pueden usar dos colores cualquiera, siempre que use los números de color al configurar el archivo de definición de máscara. Asegúrese de que los colores del mapa son colores puros para la región que desea usar y que tienen bordes distintos. Un color puro sería uno en el que cada píxel del área tiene el mismo valor de color. El uso de un efecto puede desenfocar o distorsionar el borde, con lo que se modifican ligeramente los colores de algunos de los píxeles. El archivo de asignación solo lo ve el mouse, no un humano, por lo que no se preocupe de decorarlo y quite los efectos de capa que pueda haber arrastrado de otras capas.

Al guardar el archivo, el nombre de archivo que elija se usará más adelante como valor para el atributo **mappingImage** del **elemento BUTTONGROUP** en el archivo de definición de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de la primera máscara**](building-your-first-skin.md)
</dt> </dl>

 

 




