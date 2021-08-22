---
description: 'Microsoft Message Queuing (MSMQ): eliminación de Windows servicio de soporte técnico de cliente de 2000'
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): eliminación de Windows servicio de soporte técnico de cliente de 2000'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bdcba684faa0a25994f66cc9cd205ba22b5ed949d8dcdd3e67497484f2784ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053053"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ): eliminación de Windows servicio de soporte técnico de cliente de 2000

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores:** Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** alta  
**Frecuencia:** baja  

## <a name="description"></a>Descripción

El Windows de soporte técnico de cliente de Windows 2000 es un componente opcional del servidor de Message Queue Server que puede instalar en una máquina de controlador de dominio de Windows 2003 o Windows 2008. Este servicio permite que Windows 2000 clientes funcionen en un modo integrado de dominio con cualquier servidor de Message Queuing instalado en Windows máquinas de 2003/2008. Los clientes de MSMQ que Windows XP hacia arriba no necesitan este servicio.

### <a name="manifestation-of-impact"></a>Demostración del impacto

Este cambio afecta Windows 2000 al interoperar en un dominio de Windows 7 donde todos los controladores de dominio se Windows Server 2008 R2. Si un cliente actualiza al dominio Windows 7, las aplicaciones MSMQ existentes en cualquier máquina de Windows 2000 del dominio no podrán funcionar en un modo integrado de dominio a menos que estos clientes actualicen a una versión Windows superior.

### <a name="mitigation"></a>Mitigación

Los usuarios que tienen máquinas cliente de Windows 2000 en un dominio Windows 7 pueden configurar un controlador de dominio Windows 2003/2008 en el dominio e instalar el servicio de soporte técnico de cliente de MSMQ Windows 2000 en este controlador de dominio.

### <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

Los usuarios que Windows 2000 equipos cliente que ejecutan MSMQ deben actualizar a una versión de Windows superior para aprovechar las ventajas de la implementación basada en Active Directory del servidor MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Los usuarios que Windows 2000 Equipos cliente que ejecutan MSMQ en un dominio de Windows 7 con uno o varios controladores de dominio de nivel inferior deben comprobar que sus aplicaciones son funcionales en este dominio mixto.

 

 



