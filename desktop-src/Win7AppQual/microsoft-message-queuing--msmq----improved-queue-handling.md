---
description: 'Microsoft Message Queuing (MSMQ): control mejorado de colas'
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: 'Microsoft Message Queuing (MSMQ): control mejorado de colas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7b7b00cfce68a183d7925f7cfab5ff7ab54b9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088163"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>Microsoft Message Queuing (MSMQ): control mejorado de colas

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

El servicio MSMQ no pone un límite máximo en el número de colas que se pueden crear en un sistema. Sin embargo, el rendimiento del sistema se afecta cuando se crea un gran número de colas. En concreto, cuando hay más de unos miles de colas, el tiempo de inicio del servicio MSMQ aumenta exponencialmente, lo que provoca un impacto visible.

Microsoft ha optimizado el inicio del servicio MSMQ en Windows 7 para reducir la sobrecarga de búsqueda para cargar las colas en la memoria. Esta optimización ha llevado a una mejora considerable del tiempo de inicio del servicio MSMQ incluso cuando se crean varios miles de colas en el sistema.

## <a name="manifestation-of-impact"></a>Demostración del impacto

Esta mejora del rendimiento no afecta a la funcionalidad de ninguna aplicación existente.

## <a name="leveraging-the-changed-feature"></a>Aprovechamiento de la característica modificada

Los desarrolladores de aplicaciones que usan MSMQ en Windows 7 ahora pueden diseñar sus soluciones sin limitar el número de colas. Tenga en cuenta que el número de colas sigue afectando al rendimiento general del servidor MSMQ, pero el impacto en el rendimiento se encuentra ahora en una escala lineal en lugar de exponencial.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Si usa un gran número de colas, simule el entorno de producción en un nivel de prueba, supervise el rendimiento y analice el tiempo de inicio del servicio y el rendimiento del mensaje con un gran número de colas y mensajes presentes en el sistema de prueba.

 

 



