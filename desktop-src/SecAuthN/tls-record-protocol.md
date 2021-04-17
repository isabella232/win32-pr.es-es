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
# <a name="tls-record-protocol"></a><span data-ttu-id="83bf3-103">Protocolo de registro TLS</span><span class="sxs-lookup"><span data-stu-id="83bf3-103">TLS Record Protocol</span></span>

<span data-ttu-id="83bf3-104">El protocolo de registro de seguridad de la [*capa de transporte*](../secgloss/t-gly.md) (TLS) protege los datos de la aplicación mediante las claves creadas durante el [Protocolo de enlace](tls-handshake-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="83bf3-104">The [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Record protocol secures application data using the keys created during the [Handshake](tls-handshake-protocol.md).</span></span> <span data-ttu-id="83bf3-105">El protocolo de registro es responsable de proteger los datos de aplicación y comprobar su [*integridad*](../secgloss/i-gly.md) y origen.</span><span class="sxs-lookup"><span data-stu-id="83bf3-105">The Record Protocol is responsible for securing application data and verifying its [*integrity*](../secgloss/i-gly.md) and origin.</span></span> <span data-ttu-id="83bf3-106">Administra lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="83bf3-106">It manages the following:</span></span>

-   <span data-ttu-id="83bf3-107">Dividir los mensajes salientes en bloques administrables y reensamblar los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="83bf3-107">Dividing outgoing messages into manageable blocks, and reassembling incoming messages.</span></span>
-   <span data-ttu-id="83bf3-108">Comprimir los bloques salientes y descomprimir los bloques entrantes (opcional).</span><span class="sxs-lookup"><span data-stu-id="83bf3-108">Compressing outgoing blocks and decompressing incoming blocks (optional).</span></span>
-   <span data-ttu-id="83bf3-109">Aplicar un [*código de autentificación de mensajes (Mac)*](../secgloss/m-gly.md) (Mac) a los mensajes salientes y comprobar los mensajes entrantes con el equipo Mac.</span><span class="sxs-lookup"><span data-stu-id="83bf3-109">Applying a [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) to outgoing messages, and verifying incoming messages using the MAC.</span></span>
-   <span data-ttu-id="83bf3-110">Cifrar los mensajes salientes y descifrar los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="83bf3-110">Encrypting outgoing messages and decrypting incoming messages.</span></span>

<span data-ttu-id="83bf3-111">Cuando se completa el protocolo de registro, los datos cifrados salientes se pasan a la capa del Protocolo de control de transmisión (TCP) para el transporte.</span><span class="sxs-lookup"><span data-stu-id="83bf3-111">When the Record Protocol is complete, the outgoing encrypted data is passed down to the Transmission Control Protocol (TCP) layer for transport.</span></span>

 

 
