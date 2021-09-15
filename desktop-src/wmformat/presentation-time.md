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
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467068"
---
# <a name="presentation-time"></a>Tiempo de presentación

Un tiempo de presentación es una medida del tiempo de la primera muestra de la primera secuencia de un archivo ASF. Esta medida, así como la mayoría de las demás medidas de tiempo que usan los objetos de este SDK, se encuentra en unidades de 100 nanosegundos. Los tiempos de presentación son importantes porque permiten sincronizar las distintas secuencias de un archivo. Debe proporcionar un tiempo de presentación para cada ejemplo de entrada que pase al escritor. Cada objeto de datos de la sección de datos de un archivo ASF tiene asociado un tiempo de presentación. Cada ejemplo de salida recuperado por el lector también tiene un tiempo de presentación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Ejemplos de medios**](media-samples.md)
</dt> </dl>

 

 




