---
description: Tablas de frecuencia
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tablas de frecuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db832144aedb8f64d18692a30a8e8c7d812c4cbd517b1b9ab31bd9cdc231019b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401263"
---
# <a name="frequency-tables"></a>Tablas de frecuencia

El filtro tv tuner (kstvtune.ax) tiene una lista interna de tablas de frecuencia. Cada tabla de frecuencias contiene una lista de frecuencias y corresponde a las frecuencias de difusión o cable de un país o región determinados. Una aplicación se ajuste a una frecuencia determinada llamando al método [**IAMTuner::p ut \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) con el índice de la frecuencia deseada.

En algunos países o regiones, los números de índice de las tablas de frecuencia se asignan directamente a los números de canal. Sin embargo, los números de canal fijos no son adecuados para todos los mercados. Por ejemplo, los consumidores no usan realmente los números del canal europeo. En su lugar, los consumidores esperan elegir y asignar sus propios números de canal para las frecuencias que usan los operadores de difusión o cable de su área. En estos países o regiones, las aplicaciones no deben exponer los números de índice directamente al usuario. Instread, la aplicación debe mantener una asignación interna entre los números de canal (presentados al usuario) y los índices de frecuencia (para la optimización).

La mayoría de los operadores de cable que no son de EE. UU. tienen libertad para difundir las frecuencias que elijan, a menudo combinando frecuencias de distintos estándares en la misma línea de canales. Por lo tanto, se usa una tabla de frecuencia "Unicable" para cualquier país o región que no tiene una autoridad estándar estándar de canales de cable. Además, se proporciona un mecanismo para invalidar frecuencias individuales en las tablas de frecuencia. Este mecanismo se describe en la sección siguiente, [Invalidaciones de frecuencia](frequency-overrides.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ajuste de televisión análoga internacional](international-analog-tv-tuning.md)
</dt> </dl>

 

 



