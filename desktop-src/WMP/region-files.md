---
title: Archivos de regiones
description: Archivos de regiones
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos de regiones
- Aspectos móviles de Windows Media Player, archivos de regiones
- máscaras, archivos de regiones
- Archivos de regiones en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357631"
---
# <a name="region-files"></a>Archivos de regiones

Los archivos de regiones son necesarios si se usa cualquier tipo de botón de posicionamiento (2PushHit, PushHit o ToggleHit).

Los archivos de región se usan para definir áreas que responderán a una pulsación, también conocida como golpe, en un botón específico. Para cada botón de posicionamiento, se asigna un color Web específico a un área en el mapa de bits de la región (por ejemplo \# , FF0000, que es el valor de rojo sólido). El número de color se especifica en la definición del botón de región. Cuando el usuario muestra la máscara, la imagen del botón se superpone en el fondo mediante las coordenadas del área en el mapa de bits de la región.

Por ejemplo, puede dibujar un círculo rojo en una ubicación que corresponda a la ubicación del botón siguiente y colorearlo en rojo sólido ( \# FF0000). Después, en la definición del botón, podría asignar un valor RGB de posicionamiento de 255, 0, 0 (que es el equivalente RGB de \# FF0000). En este caso, el botón siguiente solo respondería a los grifos (aciertos) dentro del círculo rojo.

Los botones de acceso se utilizan cuando se desea definir formas que no sean rectángulos. Todavía debe definir las coordenadas de cada botón para que las imágenes secundarias, como Insert y Disabled, se puedan encontrar correctamente. En la práctica, cada botón está limitado por un rectángulo y estos rectángulos de límite imaginarios no deben superponerse.

> [!Note]  
> Los archivos de región no son necesarios en las máscaras móviles de Windows Media Player 10 porque los tipos de botón no se admiten en Windows Media Player 10 Mobile o posterior.

 

La siguiente imagen es un archivo de región típico.

![archivo de región](images/cesdkreg.png)

Este archivo define los elementos de la máscara para cada botón de tipo de posicionamiento. Cada color se identificará por su número de color en la sección botones del archivo de definición de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de imagen**](art-files-mobile.md)
</dt> </dl>

 

 




