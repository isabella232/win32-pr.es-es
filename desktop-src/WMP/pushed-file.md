---
title: Archivo de inserción
description: Archivo de inserción
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Reproductor de Windows Media Máscaras móviles, archivos de arte
- skins,art files
- archivos para máscaras, arte
- archivos art para máscaras,archivos pushed
- Reproductor de Windows Media Máscaras móviles, archivos de inserción
- skins,Pushed files
- Archivos inserdos en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0526cad560abfbee3a7ec6cbaa0c355a51d93c2080d7c1ef933f7caaf867ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570685"
---
# <a name="pushed-file"></a>Archivo de inserción

El archivo pushed contiene las imágenes que se mostrarán cuando el usuario pulse un botón. También puede incluir las imágenes normales e insertadas para el estado de pausa del botón PlayPause.

La siguiente imagen es un archivo pushed típico.

![archivo de inserción](images/cesdkpus.png)

Esto almacena las imágenes que se mostrarán cuando se pulsen los botones de tipo de pulsación. También se almacenan en este archivo las imágenes normales e insertadas para la imagen en pausa del botón PlayPause. Excepto en el caso de las imágenes secundarias PlayPause de la derecha, las otras imágenes de botón se alinean con la imagen de fondo, con el desplazamiento definido en la sección Mapas de bits del archivo de definición de máscara.

Observe que el fondo de la imagen de botón coincide exactamente con el área correspondiente en el archivo de fondo. Esto es importante, ya que cuando el usuario pulsa un botón de tipo de pulsación, todo el rectángulo definido para la imagen inserda reemplazará el área correspondiente en el archivo de fondo. Mantenga el gráfico coherente con la imagen de fondo para asegurarse de que solo cambiarán las partes del botón que desea que aparezcan diferentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




