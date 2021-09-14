---
title: Archivo pushed
description: Archivo pushed
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Reproductor de Windows Media Máscaras móviles, archivos art
- skins,art files
- archivos para máscaras, art
- archivos art para máscaras, archivos pushed
- Reproductor de Windows Media Máscaras móviles, archivos pushed
- skins,Pushed files
- Archivos inserdos en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073232"
---
# <a name="pushed-file"></a>Archivo pushed

El archivo pushed contiene las imágenes que se mostrarán cuando el usuario pulse un botón. También puede incluir las imágenes normales e insertadas para el estado de pausa del botón PlayPause.

La siguiente imagen es un archivo pushed típico.

![archivo de inserción](images/cesdkpus.png)

Esto almacena las imágenes que se mostrarán cuando se pulsen los botones de tipo de pulsación. También se almacenan en este archivo las imágenes normales e insertadas para la imagen en pausa del botón PlayPause. A excepción de las imágenes secundarias PlayPause de la derecha, las demás imágenes de botón se alinean con la imagen background, usando el desplazamiento definido en la sección Mapas de bits del archivo de definición de máscara.

Observe que el fondo de la imagen de botón coincide exactamente con el área correspondiente del archivo background. Esto es importante, porque cuando el usuario pulsa un botón de tipo de pulsación, todo el rectángulo definido para la imagen inserda reemplazará el área de coincidencia en el archivo de fondo. Mantenga el gráfico coherente con la imagen de fondo para asegurarse de que solo las partes del botón que desea que aparezcan diferentes cambiarán realmente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




