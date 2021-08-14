---
title: Señalización fuera de banda
description: Las aplicaciones que comparten datos comunes mediante el directorio pueden usar la señalización fuera de banda para evitar la asimetría de versiones y las actualizaciones parciales.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06aab6482c9ad7af8e7c9b505b528b3559adb81f990b4d83681e44f418fadc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185422"
---
# <a name="out-of-band-signaling"></a>Señalización fuera de banda

Las aplicaciones que comparten datos comunes mediante el directorio pueden usar la señalización fuera de banda para evitar la asimetría de versiones y las actualizaciones parciales. En pocas palabras, las aplicaciones colaboradores usan un mecanismo independiente de la replicación de directorios para informar entre sí de los cambios en los datos comunes compartidos. La señalización fuera de banda es más eficaz cuando se usa en combinación con un mecanismo de control de versiones, lo que permite que el asociado detecte el cambio para notificar a los asociados remotos qué versión de los datos compartidos debe esperar.

Volviendo al ejemplo de RPC dado en la sección "Sesgo de versión" del comportamiento de replicación en Active Directory Domain Services , el servidor RPC podría llamar de nuevo [a](replication-behavior-in-active-directory-domain-services.md)los clientes conectados para informarles del traslado a un nuevo servidor: "Voy a mover. En espera, la replicación le llevará la nueva dirección en breve" para que el cliente pueda controlar el período de transición.

Las aplicaciones que requieren que haya directivas idénticas en vigor para comunicarse entre sí pueden usar la señalización fuera de banda para garantizar que no se emplee una nueva directiva hasta que todas las partes implicadas la reciban. Por ejemplo, si se cambia la directiva de seguridad de protocolo de Internet (IPsec) entre dos máquinas, un agente de la máquina de origen podría ponerse en contacto con un agente en la máquina de destino para negociar la aplicación de la directiva modificada, con la aplicación de retraso de la máquina de origen hasta que la máquina de destino también haya recibido la nueva directiva.

 

 




