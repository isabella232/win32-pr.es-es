---
title: Tiempo de presentación
description: Tiempo de presentación
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- SDK de Windows Media Format, tiempos de presentación
- Advanced Systems Format (ASF), tiempos de presentación
- ASF (formato de sistemas avanzados), tiempos de presentación
- tiempos de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357530"
---
# <a name="presentation-time"></a>Tiempo de presentación

Un tiempo de presentación es una medida de tiempo desde la primera muestra de la primera secuencia en un archivo ASF. Esta medida, así como la mayoría de las demás medidas de tiempo usadas por los objetos de este SDK, se encuentra en unidades de 100-nanosegundos. Los tiempos de presentación son importantes porque permiten sincronizar las diversas secuencias en un archivo. Debe proporcionar un tiempo de presentación para cada ejemplo de entrada que pase al sistema de escritura. Cada objeto de datos de la sección de datos de un archivo ASF tiene un tiempo de presentación asociado a él. Cada ejemplo de salida recuperado por el lector también tiene un tiempo de presentación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Ejemplos de medios**](media-samples.md)
</dt> </dl>

 

 




