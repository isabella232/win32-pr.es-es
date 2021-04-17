---
description: Un mensaje con doble cifrado es un mensaje cifrado para un destinatario o un conjunto de destinatarios.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Crear y recibir mensajes de datos con doble cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666422"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a><span data-ttu-id="51299-103">Crear y recibir mensajes de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="51299-103">Creating and Receiving Enveloped Data Messages</span></span>

<span data-ttu-id="51299-104">Un mensaje con doble cifrado es un mensaje cifrado para un conjunto de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="51299-104">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="51299-105">En el proceso de envoltura, se genera una clave de cifrado de sesión y se cifra el mensaje con esa clave.</span><span class="sxs-lookup"><span data-stu-id="51299-105">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="51299-106">La propia clave de cifrado se cifra entonces por separado para cada destinatario mediante las claves públicas de cada certificado de destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="51299-106">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="51299-107">El mensaje con doble cifrado consta del mensaje cifrado, los certificados de los destinatarios deseados y el conjunto de claves cifradas, uno para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="51299-107">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="51299-108">El mensaje generado está en formato [*PKCS \# 7*](../secgloss/p-gly.md)/CMS.</span><span class="sxs-lookup"><span data-stu-id="51299-108">The message generated is in [*PKCS \#7*](../secgloss/p-gly.md)/CMS format.</span></span>

<span data-ttu-id="51299-109">En las secciones siguientes se muestran procedimientos y ejemplos de tareas de mensajes con envoltura:</span><span class="sxs-lookup"><span data-stu-id="51299-109">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="51299-110">Codificación de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="51299-110">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)
-   [<span data-ttu-id="51299-111">Descodificar datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="51299-111">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)
-   [<span data-ttu-id="51299-112">Código alternativo para codificar un mensaje con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="51299-112">Alternate Code for Encoding an Enveloped Message</span></span>](alternate-code-for-encoding-an-enveloped-message.md)
-   [<span data-ttu-id="51299-113">Programa C de ejemplo: codificar un mensaje con signo de cifrado</span><span class="sxs-lookup"><span data-stu-id="51299-113">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
