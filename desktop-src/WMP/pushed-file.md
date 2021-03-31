---
title: Archivo insertado
description: Archivo insertado
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos insertados
- Máscaras móviles de Windows Media Player, archivos insertados
- máscaras, archivos insertados
- Archivos insertados en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418785"
---
# <a name="pushed-file"></a>Archivo insertado

El archivo insertado contiene las imágenes que se mostrarán cuando el usuario puntee en un botón. También puede incluir las imágenes normales e insertadas para el estado de pausa del botón PlayPause.

La siguiente imagen es un archivo insertado típico.

![archivo insertado](images/cesdkpus.png)

Esto almacena las imágenes que se mostrarán cuando se PUNTEEN los botones de tipo de posicionamiento. También se almacenan en este archivo las imágenes normales e insertadas para la imagen en pausa del botón PlayPause. Excepto en el caso de las imágenes secundarias de PlayPause a la derecha, las demás imágenes de botón se alinean con la imagen de fondo mediante el desplazamiento definido en la sección de mapas de bits del archivo de definición de máscara.

Observe que el fondo de la imagen del botón coincide exactamente con el área correspondiente en el archivo en segundo plano. Esto es importante, porque cuando el usuario pulsa un botón de tipo de posicionamiento, el rectángulo completo definido para la imagen insertada reemplazará el área de coincidencia en el archivo de fondo. Mantenga el gráfico coherente con la imagen de fondo para asegurarse de que solo cambian las partes del botón que desea que aparezcan de forma diferente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de imagen**](art-files-mobile.md)
</dt> </dl>

 

 




