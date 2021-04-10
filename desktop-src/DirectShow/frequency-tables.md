---
description: Tablas de frecuencia
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tablas de frecuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152016"
---
# <a name="frequency-tables"></a>Tablas de frecuencia

El filtro de sintonizador de TV (kstvtune.ax) tiene una lista interna de tablas de frecuencia. Cada tabla de frecuencias contiene una lista de frecuencias y corresponde a las frecuencias de difusión o de cable para un país o región determinados. Una aplicación se ajusta a una frecuencia determinada llamando al método de [**\_ canal IAMTuner::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) con el índice de la frecuencia deseada.

En algunos países o regiones, los números de índice de las tablas de frecuencia se asignan directamente a los números de canal. Sin embargo, los números de canal fijos no son adecuados para todos los mercados. Por ejemplo, los consumidores no utilizan realmente los números de canal europeos. En su lugar, los consumidores esperan elegir y asignar sus propios números de canal para las frecuencias que usan los operadores de difusión o cable en su área. En estos países o regiones, las aplicaciones no deben exponer los números de índice directamente al usuario. Instread, la aplicación debe mantener una asignación interna entre los números de canal (presentados al usuario) y los índices de frecuencia (para la optimización).

La mayoría de los operadores de cable que no son de Estados Unidos son gratis para difundir las frecuencias de su elección, a menudo mezclando frecuencias de diferentes estándares en la misma línea de canal. Por lo tanto, se usa una tabla de frecuencias de "Unicable" para cualquier país o región que carezca de una entidad de estándares de canal de cable estándar. Además, se proporciona un mecanismo para invalidar las frecuencias individuales en las tablas de frecuencia. Este mecanismo se describe en la sección siguiente, [invalidaciones de frecuencia](frequency-overrides.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ajuste de TV analógica internacional](international-analog-tv-tuning.md)
</dt> </dl>

 

 



