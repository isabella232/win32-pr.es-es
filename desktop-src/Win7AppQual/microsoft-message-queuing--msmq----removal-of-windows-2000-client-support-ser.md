---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): quitar el servicio de compatibilidad con clientes de Windows 2000'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083176"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ): quitar el servicio de compatibilidad con clientes de Windows 2000

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores** : Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** alta  
**Frecuencia** : baja  

## <a name="description"></a>Descripción

El servicio de soporte técnico de cliente de Windows 2000 es un componente opcional del servidor de Message Queue Server que puede instalar en un equipo de controlador de dominio de Windows 2003 o Windows 2008. Este servicio permite a los clientes de Windows 2000 funcionar en un modo integrado en el dominio con cualquier servidor de Message Queue Server instalado en máquinas con Windows 2003/2008. Los clientes MSMQ que operan en Windows XP en adelante no necesitan este servicio.

### <a name="manifestation-of-impact"></a>Manifiesto de impacto

Este cambio afecta a Windows 2000 al interoperar en un dominio de Windows 7 donde todos los controladores de dominio son Windows Server 2008 R2. Si un cliente se actualiza al dominio de Windows 7, las aplicaciones MSMQ existentes en cualquier equipo con Windows 2000 del dominio no podrán funcionar en un modo integrado en el dominio a menos que estos clientes actualicen a una versión posterior de Windows.

### <a name="mitigation"></a>Mitigación

Los usuarios que tienen equipos cliente de Windows 2000 en un dominio de Windows 7 pueden configurar un controlador de dominio de Windows 2003/2008 en el dominio e instalar el servicio de soporte técnico de cliente de Windows 2000 MSMQ en este controlador de dominio.

### <a name="leveraging-feature-capabilities"></a>Aprovechar las capacidades de características

Los usuarios que tienen equipos cliente de Windows 2000 con MSMQ deben actualizarse a una versión posterior de Windows para poder aprovechar la implementación basada en Active Directory del servidor de MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Los usuarios que tienen equipos cliente de Windows 2000 con MSMQ en un dominio de Windows 7 con uno o más controladores de dominio de nivel inferior deben comprobar que sus aplicaciones son funcionales en este dominio mixto.

 

 



