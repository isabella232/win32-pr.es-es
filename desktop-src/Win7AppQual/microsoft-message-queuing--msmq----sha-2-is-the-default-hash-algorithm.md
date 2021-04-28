---
description: 'Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado'
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2b73e347f5d5a768780afc5d2153909c6f5a9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088103"
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

-   MSMQ en Windows 2003 o una versión inferior no aceptará mensajes firmados que se origine en MSMQ en Windows 7
-   MSMQ en Windows 7 no aceptará mensajes firmados procedentes de Windows 2008 o inferiores

## <a name="mitigation"></a>Mitigación

Los usuarios deben considerar la posibilidad de actualizar a Windows 7 para aprovechar el algoritmo de firma más seguro. Para habilitar el intercambio de mensajes firmados sin problemas entre Windows 7 y cualquier sistema operativo de nivel inferior, el administrador debe agregar las excepciones adecuadas en los equipos MSMQ.

 

 



