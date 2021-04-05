---
description: La siguiente es una guía para proteger la programación de Windows Sockets.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Programación de Winsock segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812457"
---
# <a name="secure-winsock-programming"></a>Programación de Winsock segura

La siguiente es una guía para proteger la programación de Windows Sockets. Está diseñado para proporcionar una descripción de la seguridad de Winsock y las opciones disponibles para el desarrollador de aplicaciones de red segura.

-   [Usar SO \_ REUSEADDR y so \_ EXCLUSIVEADDRUSE](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [Extensiones Winsock Secure Socket](winsock-secure-socket-extensions.md)

Las comunicaciones que usan Sockets también se pueden cifrar mediante los estándares SSL/TLS mediante el canal seguro, también conocido como tecnología Schannel. Schannel es un proveedor de compatibilidad para seguridad (SSP) que contiene un conjunto de protocolos de seguridad que proporcionan autenticación de identidad y comunicación privada segura a través del cifrado. Schannel se usa principalmente para aplicaciones de Internet que requieren comunicaciones del protocolo seguro de transferencia de hipertexto (HTTP). Para obtener más información, consulte [canal seguro](../secauthn/secure-channel.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canal seguro](../secauthn/secure-channel.md)
</dt> </dl>

 

 
