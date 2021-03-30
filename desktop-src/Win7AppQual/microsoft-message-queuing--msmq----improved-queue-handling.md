---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: 'Microsoft Message Queuing (MSMQ): control de colas mejorado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002172"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>Microsoft Message Queuing (MSMQ): control de colas mejorado

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : baja  





## <a name="description"></a>Descripción

El servicio MSMQ no pone un límite en el número de colas que se pueden crear en un sistema. Sin embargo, el rendimiento del sistema se ve afectado cuando se crea un gran número de colas. En concreto, cuando hay más de miles de colas, la hora de inicio del servicio MSMQ aumenta exponencialmente, lo que da lugar a un impacto visible.

Microsoft ha optimizado el inicio del servicio MSMQ en Windows 7 para reducir la sobrecarga de búsqueda para cargar las colas en la memoria. Esta optimización ha provocado una mejora espectacular de la hora de inicio del servicio MSMQ incluso cuando se crean varios miles de colas en el sistema.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

Esta mejora de rendimiento no afecta a la funcionalidad de ninguna aplicación existente.

## <a name="leveraging-the-changed-feature"></a>Aprovechamiento de la característica modificada

Los desarrolladores de aplicaciones que usan MSMQ en Windows 7 ahora pueden diseñar sus soluciones sin limitar el número de colas. Tenga en cuenta que el número de colas todavía afecta al rendimiento general del servidor de MSMQ, pero el impacto en el rendimiento es ahora una escala lineal en lugar de una escala exponencial.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Si utiliza un gran número de colas, simule el entorno de producción en un banco de pruebas, supervise el rendimiento y analice el tiempo de inicio del servicio y el rendimiento de los mensajes con un gran número de colas y mensajes presentes en el sistema de prueba.

 

 



