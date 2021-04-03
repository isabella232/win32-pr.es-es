---
title: Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios
description: Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- flujos, velocidades de bits
- códecs, calcular velocidades de bits para flujos arbitrarios
- velocidades de bits, calcular flujos arbitrarios
- secuencias, calcular velocidades de bits para flujos arbitrarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075148"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios

Calcular la velocidad de bits y la ventana de búfer adecuados para un tipo de flujo arbitrario no es una ciencia exacta. Un enfoque sencillo es establecer la velocidad de bits para que coincida con el tamaño de la secuencia dividida por su longitud, en segundos. Por ejemplo, una secuencia que contiene un total de 68000 bits de hasta 20 segundos puede tener una velocidad de bits de 3400 bits por segundo (68000 bits/20 segundos = 3400 bits por segundo).

El problema con esta sencilla técnica de asignar la velocidad de bits es que no tiene en cuenta la distribución de los datos dentro de la secuencia. Muchas secuencias arbitrarias contienen grandes cantidades de datos a intervalos a lo largo de la escala de tiempo del archivo. Los flujos de imagen, por ejemplo, tienen ejemplos que son más grandes, pero normalmente se espacian varios segundos. La ventana de búfer debe establecerse para asegurarse de que el búfer no se desbordará.

Para comprobar la ventana de búfer, multiplique la velocidad de bits (bits por segundo) por la ventana de búfer (en segundos) y divida por 1000 para obtener el tamaño, en bits, del búfer para la secuencia. Después, asegúrese de que el tamaño del búfer es lo suficientemente grande como para contener cualquier combinación de muestras de la secuencia que sean inferiores a la ventana del búfer en el momento de la presentación. En duda, establezca los dos valores un poco más alto de lo que cree que los necesita.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Almacenar contenido en búfer**](buffering-content.md)
</dt> <dt>

[**Configuración de tipos de flujo arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




