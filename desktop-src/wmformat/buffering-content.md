---
title: Almacenar contenido en búfer
description: Almacenar contenido en búfer
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK, contenido almacenado en búfer
- almacenar contenido en búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704569"
---
# <a name="buffering-content"></a>Almacenar contenido en búfer

Cuando el objeto de lector abre un archivo de streaming, determina el tamaño del búfer en función de los valores del encabezado del archivo. Puede considerar el búfer como un depósito con un hueco en la parte inferior que se pierde a una velocidad constante. Siempre y cuando la velocidad a la que se rellene el depósito no sea mayor que la velocidad a la que se pierde, el cubo nunca se desbordará.

La velocidad a la que se pierde el depósito imaginario es la velocidad de bits de la secuencia. La velocidad a la que se llena el depósito es la velocidad de bits de streaming real. Los datos de un flujo comprimido varían en tamaño de muestra a muestra, en función de la cantidad de compresión que se haya logrado. Por lo tanto, aunque la velocidad de bits de la secuencia está establecida en el perfil, representa la velocidad media de bits, no una constante.

La otra configuración de flujo importante para el proceso de almacenamiento en búfer es la ventana de búfer. La ventana de búfer se mide en el tiempo y especifica la cantidad de contenido que se puede almacenar en búfer. La capacidad del depósito imaginario se puede encontrar mediante la ventana de búfer. Por ejemplo, si tiene una secuencia con una velocidad de bits de 32 Kbps y una ventana de búfer de 3 segundos, se ajusta el tamaño del búfer para que contenga 3 segundos de contenido de 32 kbps o 12.000 bytes (32.000 bits por segundo x 3 segundos/8 bits por byte). El códec limita la variación entre la velocidad de bits de streaming real de muestras codificadas, de modo que en un período de tiempo igual a la ventana de búfer, la velocidad de bits promedio no es mayor que la velocidad de bits de la secuencia.

Normalmente, se establece la velocidad de bits y la ventana de búfer de una secuencia en un perfil, y el escritor controla el resto. Sin embargo, al pasar muestras comprimidas al lector, debe asegurarse de que los valores correctos se transfieren al nuevo archivo estableciendo la velocidad de bits y la ventana de búfer para la secuencia del perfil de destino en los valores de la secuencia comprimida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Ejemplos de medios**](media-samples.md)
</dt> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




