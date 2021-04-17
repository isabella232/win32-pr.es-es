---
description: El protocolo de registro de seguridad de la capa de transporte (TLS) protege los datos de la aplicación mediante las claves creadas durante el protocolo de enlace.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Protocolo de registro TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652927"
---
# <a name="tls-record-protocol"></a>Protocolo de registro TLS

El protocolo de registro de seguridad de la [*capa de transporte*](../secgloss/t-gly.md) (TLS) protege los datos de la aplicación mediante las claves creadas durante el [Protocolo de enlace](tls-handshake-protocol.md). El protocolo de registro es responsable de proteger los datos de aplicación y comprobar su [*integridad*](../secgloss/i-gly.md) y origen. Administra lo siguiente:

-   Dividir los mensajes salientes en bloques administrables y reensamblar los mensajes entrantes.
-   Comprimir los bloques salientes y descomprimir los bloques entrantes (opcional).
-   Aplicar un [*código de autentificación de mensajes (Mac)*](../secgloss/m-gly.md) (Mac) a los mensajes salientes y comprobar los mensajes entrantes con el equipo Mac.
-   Cifrar los mensajes salientes y descifrar los mensajes entrantes.

Cuando se completa el protocolo de registro, los datos cifrados salientes se pasan a la capa del Protocolo de control de transmisión (TCP) para el transporte.

 

 
