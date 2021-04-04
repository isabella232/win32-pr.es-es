---
title: Señalización fuera de banda
description: Las aplicaciones cooperativas que comparten datos comunes mediante el directorio pueden usar señales fuera de banda para evitar el sesgo de versiones y las actualizaciones parciales.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075111"
---
# <a name="out-of-band-signaling"></a>Señalización fuera de banda

Las aplicaciones cooperativas que comparten datos comunes mediante el directorio pueden usar señales fuera de banda para evitar el sesgo de versiones y las actualizaciones parciales. En pocas palabras, las aplicaciones que cooperan usan un mecanismo independiente de la replicación de directorios para informar mutuamente de los cambios en los datos comunes compartidos. La señalización fuera de banda es más eficaz cuando se usa en combinación con un mecanismo de control de versiones, lo que permite al asociado detectar el cambio para notificar a los asociados remotos la versión de los datos compartidos que se debe esperar.

Volviendo al ejemplo de RPC proporcionado en la sección "sesgo de la versión" del comportamiento de la [replicación en Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), el servidor RPC podría volver a llamar a los clientes conectados para informarles del traslado a un nuevo servidor: "voy a mover. Por lo tanto, la replicación le llevará la nueva dirección en breve "para que el cliente pueda controlar el período de transición.

Las aplicaciones que requieren directivas idénticas para que se puedan comunicar entre sí pueden utilizar la señalización fuera de banda para asegurarse de que no se emplea una nueva Directiva hasta que todas las partes implicadas la hayan recibido. Por ejemplo, si se cambia la Directiva del Protocolo de seguridad de Internet (IPsec) entre dos equipos, un agente en el equipo de origen podría ponerse en contacto con un agente en el equipo de destino para negociar la aplicación de la directiva modificada, con la aplicación que retrasa la máquina de origen hasta que la máquina de destino haya recibido también la nueva Directiva.

 

 




