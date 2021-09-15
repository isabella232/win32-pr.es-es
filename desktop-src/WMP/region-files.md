---
title: Archivos de región
description: Archivos de región
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Reproductor de Windows Media Máscaras móviles, archivos de arte
- skins,art files
- archivos para máscaras, arte
- archivos art para máscaras,archivos de región
- Reproductor de Windows Media Máscaras móviles, archivos de región
- skins,Archivos de región
- Archivos de región en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567512"
---
# <a name="region-files"></a>Archivos de región

Los archivos de región son necesarios si usa cualquier tipo de botón de pulsación (2PushHit, PushHit o ToggleHit).

Los archivos de región se usan para definir áreas que responderán a una pulsación, también conocida como pulsación, en un botón específico. Para cada botón de pulsación, a un área del mapa de bits Región se le da un color web específico (como FF0000, que es el valor \# de rojo sólido). El número de color se especifica en la definición del botón de región. Cuando el usuario muestra la máscara, la imagen del botón se superpone al fondo mediante las coordenadas del área en el mapa de bits Región.

Por ejemplo, podría dibujar un círculo rojo en una ubicación correspondiente a la ubicación del botón Siguiente y colorearlo de color rojo sólido \# (FF0000). A continuación, en la definición del botón, podría asignar un valor RGB de 255,0,0 (que es el equivalente RGB de \# FF0000). En este caso, el botón Siguiente solo respondería a pulsaciones (aciertos) dentro del círculo rojo.

Los botones de pulsación se usan cuando se quieren definir formas que no sean rectángulos. Todavía debe definir las coordenadas de cada botón para que las imágenes secundarias como Pushed (Insertar) y Disabled (Deshabilitado) se puedan encontrar correctamente. En la práctica, cada botón está delimitado por un rectángulo y estos rectángulos de límite imaginarios no deben superponerse.

> [!Note]  
> Los archivos de arte de la región no son necesarios Reproductor de Windows Media 10 máscaras móviles porque los tipos de botón no se admiten en Reproductor de Windows Media 10 Mobile o versiones posteriores.

 

La siguiente imagen es un archivo de región típico.

![archivo de región](images/cesdkreg.png)

Este archivo define las partes de la máscara para cada botón de tipo de pulsación. Cada color se identificará por su número de color en la sección Botones del archivo de definición de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




