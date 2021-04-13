---
description: El mensaje con doble cifrado consta del mensaje cifrado, los certificados de los destinatarios deseados y el conjunto de claves cifradas, uno para cada destinatario. El mensaje generado está en \# formato PKCS 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Crear y recibir mensajes de datos con doble cifrado en CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360229"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a><span data-ttu-id="bc46e-104">Crear y recibir mensajes de datos con doble cifrado en CAPICOM</span><span class="sxs-lookup"><span data-stu-id="bc46e-104">Creating and Receiving Enveloped Data Messages in CAPICOM</span></span>

<span data-ttu-id="bc46e-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc46e-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bc46e-106">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bc46e-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="bc46e-107">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="bc46e-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="bc46e-108">Un mensaje con doble cifrado es un mensaje cifrado para un conjunto de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="bc46e-108">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="bc46e-109">En el proceso de envoltura, se genera una clave de cifrado de sesión y se cifra el mensaje con esa clave.</span><span class="sxs-lookup"><span data-stu-id="bc46e-109">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="bc46e-110">La propia clave de cifrado se cifra entonces por separado para cada destinatario mediante las claves públicas de cada certificado de destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="bc46e-110">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="bc46e-111">El mensaje con doble cifrado consta del mensaje cifrado, los certificados de los destinatarios deseados y el conjunto de claves cifradas, uno para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="bc46e-111">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="bc46e-112">El mensaje generado está en \# formato PKCS 7/CMS.</span><span class="sxs-lookup"><span data-stu-id="bc46e-112">The message generated is in PKCS \#7/CMS format.</span></span>

<span data-ttu-id="bc46e-113">En las secciones siguientes se muestran procedimientos y ejemplos de tareas de mensajes con envoltura:</span><span class="sxs-lookup"><span data-stu-id="bc46e-113">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="bc46e-114">Envío de un mensaje de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="bc46e-114">Sending an Enveloped Data Message</span></span>](sending-an-enveloped-data-message.md)
-   [<span data-ttu-id="bc46e-115">Recibir un mensaje de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="bc46e-115">Receiving an Enveloped Data Message</span></span>](receiving-an-enveloped-data-message.md)

 

 



