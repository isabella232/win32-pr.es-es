---
description: El protocolo de registro seguridad de la capa de transporte (TLS) protege los datos de la aplicación mediante las claves creadas durante el protocolo de enlace.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Protocolo de registro TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160919"
---
# <a name="tls-record-protocol"></a>Protocolo de registro TLS

El [*protocolo de registro seguridad de*](../secgloss/t-gly.md) la capa de transporte (TLS) protege los datos de la aplicación mediante las claves creadas durante el protocolo de [enlace.](tls-handshake-protocol.md) El protocolo de registro es responsable de proteger los datos de la aplicación y comprobar su [*integridad y*](../secgloss/i-gly.md) origen. Administra lo siguiente:

-   Dividir los mensajes salientes en bloques administrables y volver a reemelar los mensajes entrantes.
-   Comprimir bloques salientes y descomprimir bloques entrantes (opcional).
-   Aplicar un código [*de autenticación de*](../secgloss/m-gly.md) mensajes (MAC) a los mensajes salientes y comprobar los mensajes entrantes mediante mac.
-   Cifrar los mensajes salientes y descifrar los mensajes entrantes.

Una vez completado el protocolo de registro, los datos cifrados salientes se pasan a la capa del Protocolo de control de transmisión (TCP) para el transporte.

 

 
