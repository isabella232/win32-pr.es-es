---
title: Archivo deshabilitado
description: Archivo deshabilitado
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Reproductor de Windows Media Máscaras móviles, archivos de arte
- skins,art files
- archivos para máscaras, arte
- archivos art para máscaras, archivos deshabilitados
- Reproductor de Windows Media Máscaras móviles, archivos deshabilitados
- máscaras, archivos deshabilitados
- Archivos deshabilitados en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068463"
---
# <a name="disabled-file"></a>Archivo deshabilitado

El archivo Deshabilitado contiene las imágenes que se mostrarán cuando no se pueda usar una función de botón determinada o un estado de botón esté desactivado. Por ejemplo, si se define una  lista  de reproducción vacía, se mostrarán los botones Siguiente y Anterior y se mostrarán con una imagen deshabilitada. Además, para los botones de alternancia, la imagen Deshabilitada se usa para indicar que el estado está desactivado.

La siguiente imagen es un archivo deshabilitado típico.

![archivo deshabilitado](images/cesdkdis.png)

Esto almacena las imágenes de los botones de tipo de llamada que están deshabilitados. Las imágenes son similares al archivo background, pero los colores son más claros. Con el desplazamiento definido en la sección Mapas de bits del archivo de definición de máscara, las imágenes de botón se alinean con la imagen de archivo de fondo.

Observe que el fondo de la imagen de botón coincide exactamente con el área correspondiente en el archivo de fondo. Esto es importante, ya que cuando un botón de tipo de pulsación no está disponible, todo el rectángulo definido para la imagen deshabilitada reemplazará el área correspondiente en el archivo de fondo. Mantenga el gráfico coherente con la imagen de fondo para asegurarse de que solo las partes del botón que desea que aparezcan diferentes cambiarán realmente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




