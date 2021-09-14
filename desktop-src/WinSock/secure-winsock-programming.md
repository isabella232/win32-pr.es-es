---
description: La siguiente es una guía para proteger la programación Windows Sockets.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Programación segura de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063968"
---
# <a name="secure-winsock-programming"></a>Programación segura de Winsock

La siguiente es una guía para proteger la programación Windows Sockets. Está diseñado para proporcionar una comprensión de la seguridad de Winsock y las opciones disponibles para el desarrollador de aplicaciones de red seguras.

-   [Uso de SO \_ REUSEADDR y SO \_ EXCLUSIVEADDRUSE](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [Extensiones de socket seguro de Winsock](winsock-secure-socket-extensions.md)

Las comunicaciones que usan sockets también se pueden cifrar mediante los estándares SSL/TLS mediante El canal seguro, también conocido como tecnología Schannel. Schannel es un proveedor de soporte técnico de seguridad (SSP) que contiene un conjunto de protocolos de seguridad que proporcionan autenticación de identidad y comunicación privada segura a través del cifrado. Schannel se usa principalmente para aplicaciones de Internet que requieren comunicaciones seguras del Protocolo de transferencia de hipertexto (HTTP). Para obtener más información, vea [Secure Channel](../secauthn/secure-channel.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canal seguro](../secauthn/secure-channel.md)
</dt> </dl>

 

 
