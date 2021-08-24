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
- función timeGetDevCaps
- función timeBeginPeriod
- función timeEndPeriod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948e81228acec27e41d43d41de7393ad64345acce25a450e91c815b1bbbf5164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781835"
---
# <a name="timer-resolution"></a>Resolución de temporizador

Para determinar las resoluciones de temporizador mínimas y máximas admitidas por los servicios de temporizador, use la [**función timeGetDevCaps.**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) Esta función rellena los **miembros wPeriodMin** y **wPeriodMax** de la estructura [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) con las resoluciones mínima y máxima. Este intervalo puede variar entre equipos y Windows plataformas.

Después de determinar las resoluciones de temporizador mínimas y máximas disponibles, debe establecer la resolución mínima que quiere que use la aplicación. Use las [**funciones timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) y [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) para establecer y borrar esta resolución. Debe hacer coincidir cada llamada a **timeBeginPeriod** con una llamada a **timeEndPeriod,** especificando la misma resolución mínima en ambas llamadas. Una aplicación puede realizar varias **llamadas timeBeginPeriod,** siempre y cuando cada llamada coincida con una llamada a **timeEndPeriod**.

En [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) y [**timeEndPeriod,**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)el parámetro *uPeriod* indica la resolución mínima del temporizador, en milisegundos. Puede especificar cualquier valor de resolución de temporizador dentro del intervalo admitido por el temporizador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los temporizadores multimedia](about-multimedia-timers.md)
</dt> </dl>

 

 




