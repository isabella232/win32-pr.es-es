---
title: Almacenamiento en búfer de contenido
description: Almacenamiento en búfer de contenido
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows SDK de formato multimedia, almacenamiento en búfer de contenido
- almacenamiento en búfer de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3005895f7a196073566c32bb455f5808bf6f11feb491000b140e1bbf88b94b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586995"
---
# <a name="buffering-content"></a>Almacenamiento en búfer de contenido

Cuando el objeto de lector abre un archivo de streaming, determina el tamaño del búfer en función de la configuración del encabezado del archivo. Puede pensar en el búfer como un depósito con un hueco en la parte inferior que se filtra a una velocidad constante. Siempre que la velocidad a la que se llena el cubo no sea, de media, mayor que la velocidad a la que se está filtrando, el cubo nunca se desbordará.

La velocidad a la que se pierde el cubo imaginario es la velocidad de bits de la secuencia. La velocidad a la que se llena el cubo es la velocidad de bits de streaming real. Los datos de una secuencia comprimida varían en tamaño de la muestra a la muestra en función de la cantidad de compresión que se lograra. Por lo tanto, aunque la velocidad de bits de la secuencia se establece en el perfil, representa la velocidad de bits media, no una constante.

La otra configuración de secuencia importante para el proceso de almacenamiento en búfer es la ventana de búfer. La ventana de búfer se mide en el tiempo y especifica cuánto contenido se puede almacenar en búfer. La capacidad del cubo imaginario se puede encontrar mediante la ventana de búfer. Por ejemplo, si tiene una secuencia con una velocidad de bits de 32 Kbps y una ventana de búfer de 3 segundos, el tamaño del búfer es de 3 segundos de contenido de 32 Kbps o 12 000 bytes (32 000 bits por segundo x 3 segundos/8 bits por byte). El códec limita la variación entre la velocidad de bits de streaming real de las muestras codificadas para que durante un período de tiempo igual a la ventana de búfer, la velocidad de bits media no sea mayor que la velocidad de bits de la secuencia.

Normalmente, se establece la velocidad de bits y la ventana de búfer de una secuencia en un perfil, y el escritor controla el resto. Sin embargo, al pasar muestras comprimidas al lector, debe asegurarse de que los valores correctos se transfieren al nuevo archivo estableciendo la velocidad de bits y la ventana de búfer de la secuencia del perfil de destino en los valores de la secuencia comprimida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Ejemplos de medios**](media-samples.md)
</dt> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




