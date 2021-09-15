---
title: Calcular la velocidad de bits y los valores de la ventana de búfer para los valores Secuencias
description: Calcular la velocidad de bits y los valores de la ventana de búfer para los valores Secuencias
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- flujos, velocidades de bits
- códecs, calcular las tasas de bits para secuencias arbitrarias
- velocidades de bits, cálculo de secuencias arbitrarias
- secuencias, calcular las tasas de bits para secuencias arbitrarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466213"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>Calcular la velocidad de bits y los valores de la ventana de búfer para los valores Secuencias

Calcular la velocidad de bits adecuada y la ventana de búfer para un tipo de flujo arbitrario no es una ciencia exacta. Un enfoque sencillo es establecer la velocidad de bits para que coincida con el tamaño de la secuencia dividida por su longitud, en segundos. Por ejemplo, una secuencia que contiene un total de 68 000 bits con una duración de 20 segundos podría tener una velocidad de bits de 3400 bits por segundo (68 000 bits/20 segundos = 3400 bits por segundo).

El problema con esta sencilla técnica de asignación de velocidad de bits es que no tiene en cuenta la distribución de datos dentro del flujo. Muchas secuencias arbitrarias contienen grandes cantidades de datos a intervalos a lo largo de la escala de tiempo del archivo. Las secuencias de imágenes, por ejemplo, tienen muestras que son bastante grandes, pero normalmente se separan varios segundos. La ventana de búfer debe establecerse para asegurarse de que el búfer no se desbordará.

Para comprobar la ventana del búfer, multiplique la velocidad de bits (bits por segundo) por la ventana del búfer (en segundos) y divida por 1000 para obtener el tamaño, en bits, del búfer para la secuencia. A continuación, asegúrese de que el tamaño del búfer sea lo suficientemente grande como para contener cualquier combinación de muestras de la secuencia que sean menores que la ventana del búfer en tiempo de presentación. En caso de duda, establezca ambos valores un poco más altos de lo que cree que los necesita.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Almacenamiento en búfer de contenido**](buffering-content.md)
</dt> <dt>

[**Configuración de tipos de secuencia arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




