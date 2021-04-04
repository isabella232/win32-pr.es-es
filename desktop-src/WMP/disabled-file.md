---
title: Archivo deshabilitado
description: Archivo deshabilitado
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos deshabilitados
- Aspectos móviles de Windows Media Player, archivos deshabilitados
- máscaras, archivos deshabilitados
- Archivos deshabilitados en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075972"
---
# <a name="disabled-file"></a>Archivo deshabilitado

El archivo deshabilitado contiene las imágenes que se mostrarán cuando no se pueda usar una función de botón determinada o cuando un estado de botón esté desactivado. Por ejemplo, si se define una lista de reproducción vacía, se mostrarán los botones **siguiente** y **anterior** , y deben mostrarse con una imagen deshabilitada. Además, en el caso de los botones de alternancia, se usa la imagen deshabilitada para indicar que el estado es OFF.

La siguiente imagen es un archivo deshabilitado típico.

![archivo deshabilitado](images/cesdkdis.png)

Esto almacena las imágenes de los botones de tipo de acceso que están deshabilitados. Las imágenes son similares al archivo en segundo plano, pero los colores son más claros. Con el desplazamiento definido en la sección de mapas de bits del archivo de definición de máscara, las imágenes de botón se alinean con la imagen de archivo de fondo.

Observe que el fondo de la imagen del botón coincide exactamente con el área correspondiente en el archivo en segundo plano. Esto es importante, porque cuando un botón de tipo de aciertos no está disponible, el rectángulo completo definido para la imagen deshabilitada reemplazará el área de coincidencia en el archivo en segundo plano. Mantenga el gráfico coherente con la imagen de fondo para asegurarse de que solo cambian las partes del botón que desea que aparezcan de forma diferente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de imagen**](art-files-mobile.md)
</dt> </dl>

 

 




