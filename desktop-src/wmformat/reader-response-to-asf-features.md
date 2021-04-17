---
title: Respuesta del lector a las características de ASF
description: Respuesta del lector a las características de ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- SDK de Windows Media Format, respuestas de lector a las características de ASF
- Advanced Systems Format (ASF), respuestas de lector a características
- ASF (formato de sistemas avanzados), respuestas de lector a características
- respuestas de lector a las características de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704649"
---
# <a name="reader-response-to-asf-features"></a>Respuesta del lector a las características de ASF

La mayoría de las características especiales de archivos ASF se pueden establecer en archivos para interactuar con las aplicaciones de reproducción personalizadas diseñadas para controlarlas. Sin embargo, algunas de las características tienen compatibilidad integrada en el objeto lector.

El objeto lector seleccionará automáticamente las secuencias de los conjuntos que se excluyen mutuamente por la velocidad de bits. Este caso especial se conoce como velocidad de bits múltiple (MBR). La secuencia que el lector selecciona se basa en la velocidad de bits de la secuencia. El número de secuencia y el orden en el que se agregó al objeto de exclusión mutua son irrelevantes para la selección automática. Si un archivo incluye más de un conjunto de flujos mutuamente excluyentes según la velocidad de bits, el lector seleccionará las secuencias basadas en el cálculo del mejor uso del ancho de banda disponible.

La exclusión mutua basada en el lenguaje se establece mediante una configuración de salida, antes de la reproducción. Si combina la exclusión mutua basada en el idioma y en la velocidad de bits, debe agrupar los flujos mutuamente exclusivos basados en la velocidad de bits por lenguaje y, a continuación, hacer que los grupos sean mutuamente excluyentes por el lenguaje. El lector comprobará primero el idioma y, a continuación, determinará la velocidad de bits que se va a usar.

La priorización de flujo se establece mediante una matriz de registros. Los registros de la matriz están en orden descendente de prioridad. El último flujo de la matriz es el primero que se quitará por el lector.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Exclusión mutua**](mutual-exclusion.md)
</dt> <dt>

[**Priorización de flujos**](stream-prioritization.md)
</dt> </dl>

 

 




