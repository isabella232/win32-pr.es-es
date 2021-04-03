---
description: Las funciones de mensaje de bajo nivel codifican datos para la transmisión y descodificación de datos que se han recibido. Las funciones de mensaje de bajo nivel también descifran y comprueban las firmas de los mensajes recibidos.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Funciones de mensajes de bajo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810249"
---
# <a name="low-level-message-functions"></a><span data-ttu-id="6fd46-104">Funciones de mensajes de bajo nivel</span><span class="sxs-lookup"><span data-stu-id="6fd46-104">Low-level Message Functions</span></span>

<span data-ttu-id="6fd46-105">Las [*funciones de mensaje de bajo nivel*](../secgloss/l-gly.md) codifican datos para la transmisión y descodificación de datos que se han recibido.</span><span class="sxs-lookup"><span data-stu-id="6fd46-105">The [*low-level message functions*](../secgloss/l-gly.md) encode data for transmission and decode data that has been received.</span></span> <span data-ttu-id="6fd46-106">Las funciones de mensaje de bajo nivel también descifran y comprueban las firmas de los mensajes recibidos.</span><span class="sxs-lookup"><span data-stu-id="6fd46-106">Low-level message functions also decrypt and verify the signatures of received messages.</span></span>

<span data-ttu-id="6fd46-107">Cuando se abre un mensaje mediante una función de apertura de mensaje de bajo nivel, permanece abierto y disponible (mantiene su [*Estado*](../secgloss/s-gly.md)) hasta que se cierra.</span><span class="sxs-lookup"><span data-stu-id="6fd46-107">When a message is opened using a low-level message open function, it remains open and available (maintains its [*state*](../secgloss/s-gly.md)) until it is closed.</span></span> <span data-ttu-id="6fd46-108">Esto permite que un mensaje se construya por etapas mediante varias llamadas a la función [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .</span><span class="sxs-lookup"><span data-stu-id="6fd46-108">This allows a message to be constructed piecemeal using multiple calls to the [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) function.</span></span>

<span data-ttu-id="6fd46-109">El uso de funciones de mensaje de bajo nivel requiere más llamadas a funciones que el uso de funciones de mensaje simplificadas (vea [mensajes simplificados](simplified-messages.md)).</span><span class="sxs-lookup"><span data-stu-id="6fd46-109">Using low-level message functions requires more function calls than using simplified message functions (see [Simplified Messages](simplified-messages.md)).</span></span> <span data-ttu-id="6fd46-110">Si se usan las funciones de mensaje simplificado, se realiza más trabajo dentro de las funciones de la API.</span><span class="sxs-lookup"><span data-stu-id="6fd46-110">If the simplified message functions are used, more of the work is done inside the functions of the API.</span></span>

<span data-ttu-id="6fd46-111">El uso de funciones de mensaje de bajo nivel implica el trabajo adicional de realizar llamadas a otras funciones criptográficas o de certificado.</span><span class="sxs-lookup"><span data-stu-id="6fd46-111">Using low-level message functions involves the additional work of making calls to other certificate or cryptographic functions.</span></span> <span data-ttu-id="6fd46-112">Por ejemplo, es posible que se necesiten datos de llamadas a funciones de certificado para inicializar estructuras utilizadas por estas funciones de mensaje de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="6fd46-112">For example, data from calls to certificate functions may be needed to initialize structures used by these low-level message functions.</span></span> <span data-ttu-id="6fd46-113">Las funciones de mensaje simplificadas inicializan muchas de estas estructuras internamente.</span><span class="sxs-lookup"><span data-stu-id="6fd46-113">Simplified message functions initialize many of these structures internally.</span></span>

<span data-ttu-id="6fd46-114">En la tabla siguiente se enumeran las secciones con descripciones de procedimientos y ejemplos de código de C del uso de las funciones de mensaje de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="6fd46-114">The following table lists sections with procedure descriptions and C code examples of using the low-level message functions.</span></span>



| <span data-ttu-id="6fd46-115">Sección</span><span class="sxs-lookup"><span data-stu-id="6fd46-115">Section</span></span>                                                                               | <span data-ttu-id="6fd46-116">Contenido</span><span class="sxs-lookup"><span data-stu-id="6fd46-116">Contents</span></span>                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="6fd46-117">Funciones de mensajes de bajo nivel</span><span class="sxs-lookup"><span data-stu-id="6fd46-117">Low-level Message Functions</span></span>](cryptography-functions.md) | <span data-ttu-id="6fd46-118">Muestra las funciones de mensaje de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="6fd46-118">Lists the low-level message functions.</span></span>             |
| [<span data-ttu-id="6fd46-119">Firmar datos</span><span class="sxs-lookup"><span data-stu-id="6fd46-119">Signing Data</span></span>](signing-data.md)                                                      | <span data-ttu-id="6fd46-120">Detalla las tareas necesarias para firmar los datos.</span><span class="sxs-lookup"><span data-stu-id="6fd46-120">Details the tasks needed to sign data.</span></span>             |
| [<span data-ttu-id="6fd46-121">Codificación de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="6fd46-121">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)                                | <span data-ttu-id="6fd46-122">Detalla las tareas necesarias para codificar los datos con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="6fd46-122">Details the tasks needed to encode enveloped data.</span></span> |
| [<span data-ttu-id="6fd46-123">Descodificar datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="6fd46-123">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)                                | <span data-ttu-id="6fd46-124">Detalla las tareas necesarias para descodificar los datos con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="6fd46-124">Details the tasks needed to decode enveloped data.</span></span> |



 

 

 
