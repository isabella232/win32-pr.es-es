---
title: Respuesta del lector a las características de ASF
description: Respuesta del lector a las características de ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows SDK de formato multimedia, respuestas del lector a las características de ASF
- Formato de sistemas avanzados (ASF), respuestas del lector a las características
- ASF (formato de sistemas avanzados), respuestas del lector a las características
- respuestas del lector a las características de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466679"
---
# <a name="reader-response-to-asf-features"></a>Respuesta del lector a las características de ASF

La mayoría de las características de archivo de ASF especiales se pueden establecer en archivos para interactuar con aplicaciones de reproducción personalizadas diseñadas para controlarlas. Sin embargo, algunas de las características tienen compatibilidad integrada en el objeto de lector.

El objeto lector seleccionará automáticamente secuencias de conjuntos que se excluyen mutuamente por velocidad de bits. Este caso especial se conoce como velocidad de bits múltiple (MBR). La secuencia que selecciona el lector se basa en la velocidad de bits de la secuencia. El número de secuencia y el orden en el que se agregó al objeto de exclusión mutua son irrelevantes para la selección automática. Si un archivo incluye más de un conjunto de secuencias mutuamente excluyentes por velocidad de bits, el lector seleccionará secuencias en función del cálculo del mejor uso del ancho de banda disponible.

La exclusión mutua basada en lenguaje se establece mediante una configuración de salida, antes de la reproducción. Si combina la exclusión mutua basada en el idioma y la velocidad de bits, debe agrupar las secuencias mutuamente excluyentes basadas en velocidad de bits por idioma y, a continuación, hacer que los grupos se excluyen mutuamente por idioma. El lector comprobará primero el idioma y, a continuación, determinará qué velocidad de bits se va a usar.

La priorización de secuencias se establece mediante una matriz de registros. Los registros de la matriz están en orden descendente de prioridad. La última secuencia de la matriz es la primera que el lector va a descartar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Exclusión mutua**](mutual-exclusion.md)
</dt> <dt>

[**Priorización de secuencias**](stream-prioritization.md)
</dt> </dl>

 

 




