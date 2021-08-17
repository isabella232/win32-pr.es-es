---
description: Los tipos de contadores del algoritmo de temporizador de precisión obtienen lecturas más precisas que los temporizadores del sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de temporizador de precisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137d136db0b4dd579dfec4673b09ce216bef4042d9356b3938b79e7817e3d83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131037"
---
# <a name="precision-timer-algorithm-counter-types"></a>Tipos de contadores de algoritmo de temporizador de precisión

Los tipos de contadores del algoritmo de temporizador de precisión obtienen lecturas más precisas que los temporizadores del sistema. El servicio que proporciona los datos también proporciona una marca de tiempo, que elimina los errores que pueden producirse debido al tiempo pequeño y variable que transcurre entre la captura de la marca de tiempo del sistema y la recopilación de los datos del archivo DLL de rendimiento. Esta marca de tiempo base para temporizadores de precisión es una propiedad PERF PRECISION TIMESTAMP, que debe seguir inmediatamente \_ \_ la propiedad PERF PRECISION \_ \_ TIMER.



| CounterType (constante)                                                                                         | Descripción                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ Precision \_ SYSTEM \_ TIMER Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))541525248<br/> | Similar a PERF COUNTER TIMER, salvo que usa una base de tiempo definida \_ por el contador en lugar de la marca de tiempo del \_ sistema.             |
| [PERF \_ Precision \_ 100NS \_ TIMER Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))542573824<br/>  | Similar a PERF 100NSEC TIMER, salvo que usa una base de tiempo definida por el contador de 100ns en lugar de la marca \_ \_ de tiempo 100ns del sistema. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> </dl>

 

