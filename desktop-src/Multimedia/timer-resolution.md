---
title: Resolución de temporizador
description: Resolución de temporizador
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- temporizadores multimedia, resolución
- timers,resolution
- resolución mínima del temporizador
- resolución máxima del temporizador
- temporizadores multimedia, resolución máxima
- temporizadores, resolución máxima
- temporizadores multimedia, resolución mínima
- temporizadores, resolución mínima
- Función timeGetDevCaps
- Función timeBeginPeriod
- función timeEndPeriod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372505"
---
# <a name="timer-resolution"></a>Resolución de temporizador

Para determinar las resoluciones de temporizador mínimas y máximas admitidas por los servicios de temporizador, use la [**función timeGetDevCaps.**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) Esta función rellena los **miembros wPeriodMin** y **wPeriodMax** de la estructura [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) con las resoluciones mínima y máxima. Este intervalo puede variar entre equipos y Windows plataformas.

Después de determinar las resoluciones de temporizador mínimas y máximas disponibles, debe establecer la resolución mínima que desea que use la aplicación. Use las [**funciones timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) [**y timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) para establecer y borrar esta resolución. Debe hacer coincidir cada llamada a **timeBeginPeriod** con una llamada a **timeEndPeriod,** especificando la misma resolución mínima en ambas llamadas. Una aplicación puede realizar varias **llamadas timeBeginPeriod,** siempre que cada llamada coincida con una llamada a **timeEndPeriod.**

En [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) y [**timeEndPeriod,**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)el parámetro *uPeriod* indica la resolución mínima del temporizador, en milisegundos. Puede especificar cualquier valor de resolución de temporizador dentro del intervalo admitido por el temporizador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los temporizadores multimedia](about-multimedia-timers.md)
</dt> </dl>

 

 




