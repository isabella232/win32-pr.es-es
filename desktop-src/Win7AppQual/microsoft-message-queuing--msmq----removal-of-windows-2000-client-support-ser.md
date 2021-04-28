---
description: 'Microsoft Message Queuing (MSMQ): eliminación del servicio de soporte técnico de cliente de Windows 2000'
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): eliminación del servicio de soporte técnico de cliente de Windows 2000'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088153"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ): eliminación del servicio de soporte técnico de cliente de Windows 2000

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores:** Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** alta  
**Frecuencia:** baja  

## <a name="description"></a>Descripción

El servicio de soporte técnico de cliente de Windows 2000 es un componente opcional de Message Queuing Server que puede instalar en un equipo de controlador de dominio de Windows 2003 o Windows 2008. Este servicio permite que los clientes de Windows 2000 funcionen en un modo integrado de dominio con cualquier servidor de Message Queuing instalado en equipos con Windows 2003/2008. Los clientes de MSMQ que funcionan en Windows XP hacia arriba no necesitan este servicio.

### <a name="manifestation-of-impact"></a>Demostración de impacto

Este cambio afecta a Windows 2000 al interoperar en un dominio de Windows 7 donde todos los controladores de dominio son Windows Server 2008 R2. Si un cliente actualiza al dominio de Windows 7, las aplicaciones MSMQ existentes en cualquier máquina Windows 2000 del dominio no podrán funcionar en un modo integrado de dominio a menos que estos clientes actualicen a una versión superior de Windows.

### <a name="mitigation"></a>Mitigación

Los usuarios que tienen equipos cliente de Windows 2000 en un dominio de Windows 7 pueden configurar un controlador de dominio de Windows 2003/2008 en el dominio e instalar el servicio de soporte técnico de cliente de MSMQ Windows 2000 en este controlador de dominio.

### <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

Los usuarios que tienen equipos cliente de Windows 2000 que ejecutan MSMQ deben actualizar a una versión superior de Windows para aprovechar las ventajas de la implementación basada en Active Directory del servidor MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Los usuarios que tienen equipos cliente de Windows 2000 que ejecutan MSMQ en un dominio de Windows 7 con uno o varios controladores de dominio de nivel inferior deben comprobar que sus aplicaciones son funcionales en este dominio mixto.

 

 



