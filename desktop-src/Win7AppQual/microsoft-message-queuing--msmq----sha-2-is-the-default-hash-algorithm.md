---
description: 'Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado'
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3c54832d953e50f3b912fdf36374faa8ff9ed0466587f7ac3fed2572eb3b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053043"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes:** Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

En Windows 7, MSMQ usa SHA-2 como valor predeterminado al firmar un mensaje saliente. Además, todos los mensajes entrantes deben estar firmados con SHA-2. Puede habilitar la compatibilidad con un algoritmo de cifrado inferior a través de una clave del Registro accesible para el administrador.

## <a name="manifestation-of-impact"></a>Demostración de impacto

-   MSMQ en Windows 2003 o inferior no aceptará mensajes firmados procedentes de MSMQ en Windows 7
-   MSMQ en Windows 7 no aceptará mensajes firmados procedentes de Windows 2008 o inferior

## <a name="mitigation"></a>Mitigación

Los usuarios deben considerar la posibilidad de actualizar Windows 7 para aprovechar el algoritmo de firma más seguro. Para habilitar el intercambio de mensajes firmados sin problemas entre Windows 7 y cualquier sistema operativo de nivel inferior, el administrador debe agregar las excepciones adecuadas en las máquinas MSMQ.

 

 



