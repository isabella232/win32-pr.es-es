---
description: A veces, un mensaje firmado requiere una contrafirma.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Contrafirmas de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810244"
---
# <a name="message-countersignatures"></a><span data-ttu-id="36b3f-103">Contrafirmas de mensaje</span><span class="sxs-lookup"><span data-stu-id="36b3f-103">Message Countersignatures</span></span>

<span data-ttu-id="36b3f-104">A veces, un mensaje firmado requiere una [*contrafirma*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="36b3f-104">Sometimes a signed message requires a [*countersignature*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="36b3f-105">Por ejemplo, el usuario A puede enviar un mensaje de datos firmados al usuario B, esperando que B confirme el acuerdo con los términos contenidos en el documento.</span><span class="sxs-lookup"><span data-stu-id="36b3f-105">For example, user A may send a signed-data message to user B, expecting B to confirm agreement with the terms contained in the document.</span></span> <span data-ttu-id="36b3f-106">El usuario B descodifica el mensaje, Lee los términos y, si está en acuerdo, contrafirma el mensaje.</span><span class="sxs-lookup"><span data-stu-id="36b3f-106">User B decodes the message, reads the terms and, if in agreement, countersigns the message.</span></span> <span data-ttu-id="36b3f-107">A continuación, el mensaje con firma se devuelve al usuario a. el usuario A ahora sabe y puede demostrar que el usuario B aceptó los términos.</span><span class="sxs-lookup"><span data-stu-id="36b3f-107">The countersigned message is then sent back to user A. User A now knows, and can prove, that user B agreed to the terms.</span></span>

<span data-ttu-id="36b3f-108">En la tabla siguiente se muestran las secciones que contienen descripciones de procedimientos o ejemplos de programas de C de contrafirma de mensajes.</span><span class="sxs-lookup"><span data-stu-id="36b3f-108">The following table lists sections that contain procedure descriptions or C program examples of message countersigning.</span></span>



| <span data-ttu-id="36b3f-109">Sección</span><span class="sxs-lookup"><span data-stu-id="36b3f-109">Section</span></span>                                                                                                                                 | <span data-ttu-id="36b3f-110">Contenido</span><span class="sxs-lookup"><span data-stu-id="36b3f-110">Contents</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="36b3f-111">Funciones de mensajes</span><span class="sxs-lookup"><span data-stu-id="36b3f-111">Message Functions</span></span>](cryptography-functions.md)                                                                       | <span data-ttu-id="36b3f-112">Enumera las funciones de firma de contadores.</span><span class="sxs-lookup"><span data-stu-id="36b3f-112">Lists the counter signature functions.</span></span>                             |
| [<span data-ttu-id="36b3f-113">Contrafirmar un mensaje</span><span class="sxs-lookup"><span data-stu-id="36b3f-113">Countersigning a Message</span></span>](countersigning-a-message.md)                                                                                | <span data-ttu-id="36b3f-114">Detalla el proceso de firma de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="36b3f-114">Details the process of counter signing a message.</span></span>                  |
| [<span data-ttu-id="36b3f-115">Comprobar una contrafirma</span><span class="sxs-lookup"><span data-stu-id="36b3f-115">Verifying a Countersignature</span></span>](verifying-a-countersignature.md)                                                                        | <span data-ttu-id="36b3f-116">Detalla el procedimiento para comprobar una firma de contador.</span><span class="sxs-lookup"><span data-stu-id="36b3f-116">Details the procedure for verifying a counter signature.</span></span>           |
| [<span data-ttu-id="36b3f-117">Comprobación de un mensaje firmado</span><span class="sxs-lookup"><span data-stu-id="36b3f-117">Verifying a Signed Message</span></span>](verifying-a-signed-message.md)                                                                            | <span data-ttu-id="36b3f-118">Detalla un proceso para comprobar la firma de un mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="36b3f-118">Details a process for verifying the signature on a signed message.</span></span> |
| [<span data-ttu-id="36b3f-119">Programa C de ejemplo: codificar y descodificar un mensaje con signo</span><span class="sxs-lookup"><span data-stu-id="36b3f-119">Example C Program: Encoding and Decoding a CounterSigned Message</span></span>](example-c-program-encoding-and-decoding-a-countersigned-message.md) | <span data-ttu-id="36b3f-120">Programa de ejemplo C que codifica y descodifica un mensaje con signo.</span><span class="sxs-lookup"><span data-stu-id="36b3f-120">Sample C program that encodes and decodes a countersigned message.</span></span> |



 

 

 
