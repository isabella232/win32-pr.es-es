---
title: Tiempo de presentación
description: Tiempo de presentación
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows SDK de formato multimedia, tiempos de presentación
- Formato de sistemas avanzados (ASF), tiempos de presentación
- ASF (formato de sistemas avanzados), tiempos de presentación
- tiempos de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2dea9181552b42508745b256768b2c5ceb4443a057fc5d7d7a5a44410c788fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807915"
---
# <a name="presentation-time"></a>Tiempo de presentación

Un tiempo de presentación es una medida del tiempo del primer ejemplo de la primera secuencia en un archivo ASF. Esta medida, así como la mayoría de las demás medidas de tiempo que usan los objetos de este SDK, se encuentra en unidades de 100 nanosegundos. Los tiempos de presentación son importantes porque permiten sincronizar las distintas secuencias de un archivo. Debe proporcionar un tiempo de presentación para cada ejemplo de entrada que pase al escritor. Cada objeto de datos de la sección de datos de un archivo ASF tiene asociado un tiempo de presentación. Cada ejemplo de salida recuperado por el lector también tiene un tiempo de presentación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Ejemplos de medios**](media-samples.md)
</dt> </dl>

 

 




