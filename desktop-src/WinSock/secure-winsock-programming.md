---
description: La siguiente es una guía para proteger la programación Windows Sockets.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Programación segura de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c3644e18a45da4a1d4fa9c20bd2d023ba41d02fed3014f2992c219601bf963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559723"
---
# <a name="secure-winsock-programming"></a>Programación segura de Winsock

La siguiente es una guía para proteger la programación Windows Sockets. Está diseñado para proporcionar una comprensión de la seguridad de Winsock y las opciones disponibles para el desarrollador de aplicaciones de red segura.

-   [Uso de SO \_ REUSEADDR y SO \_ EXCLUSIVEADDRUSE](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [Extensiones de socket seguro de Winsock](winsock-secure-socket-extensions.md)

Las comunicaciones que usan sockets también se pueden cifrar mediante los estándares SSL/TLS mediante el canal seguro, también conocido como tecnología Schannel. Schannel es un proveedor de soporte técnico de seguridad (SSP) que contiene un conjunto de protocolos de seguridad que proporcionan autenticación de identidad y comunicación privada segura a través del cifrado. Schannel se usa principalmente para aplicaciones de Internet que requieren comunicaciones seguras del Protocolo de transferencia de hipertexto (HTTP). Para obtener más información, vea [Canal seguro](../secauthn/secure-channel.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canal seguro](../secauthn/secure-channel.md)
</dt> </dl>

 

 
