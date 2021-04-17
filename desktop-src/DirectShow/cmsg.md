---
description: La clase CMsgThread proporciona compatibilidad con un subproceso de trabajo al que se pueden publicar solicitudes de forma asincrónica en lugar de enviarse directamente.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: Clase CMsg
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666123"
---
# <a name="cmsg-class"></a><span data-ttu-id="32b3c-103">Clase CMsg</span><span class="sxs-lookup"><span data-stu-id="32b3c-103">CMsg class</span></span>

<span data-ttu-id="32b3c-104">La clase [**CMsgThread**](cmsgthread.md) proporciona compatibilidad con un subproceso de trabajo al que se pueden publicar solicitudes de forma asincrónica en lugar de enviarse directamente.</span><span class="sxs-lookup"><span data-stu-id="32b3c-104">The [**CMsgThread**](cmsgthread.md) class provides support for a worker thread to which requests can be posted asynchronously instead of sent directly.</span></span> <span data-ttu-id="32b3c-105">La clase [**CAMThread**](camthread.md) proporciona un subproceso de trabajo al que se pueden enviar solicitudes individuales.</span><span class="sxs-lookup"><span data-stu-id="32b3c-105">The [**CAMThread**](camthread.md) class provides a worker thread to which single requests can be sent.</span></span> <span data-ttu-id="32b3c-106">Solo un cliente puede realizar una solicitud a la vez y el cliente se bloquea hasta que el subproceso de trabajo haya completado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32b3c-106">Only one client can make a request at a time, and the client blocks until the worker thread has completed the request.</span></span> <span data-ttu-id="32b3c-107">Por el contrario, la clase **CMsgThread** proporciona un subproceso de trabajo en el que se puede publicar cualquier número de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="32b3c-107">By contrast, the **CMsgThread** class provides a worker thread to which any number of requests can be posted.</span></span> <span data-ttu-id="32b3c-108">Las solicitudes (en forma de `CMsg` objeto) se ponen en cola y se ejecutan en orden, de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="32b3c-108">The requests (in the form of a `CMsg` object) are queued and executed in order, asynchronously.</span></span> <span data-ttu-id="32b3c-109">No se recibe ninguna respuesta o valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="32b3c-109">No reply or return value is received.</span></span>



| <span data-ttu-id="32b3c-110">Miembros de datos</span><span class="sxs-lookup"><span data-stu-id="32b3c-110">Data Members</span></span>              | <span data-ttu-id="32b3c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="32b3c-111">Description</span></span>                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b3c-112">dwFlags</span><span class="sxs-lookup"><span data-stu-id="32b3c-112">dwFlags</span></span>                   | <span data-ttu-id="32b3c-113">Parámetro de marca para el código de solicitud.</span><span class="sxs-lookup"><span data-stu-id="32b3c-113">Flag parameter to the request code.</span></span>                                                                                                                                               |
| <span data-ttu-id="32b3c-114">lpParam</span><span class="sxs-lookup"><span data-stu-id="32b3c-114">lpParam</span></span>                   | <span data-ttu-id="32b3c-115">Datos requeridos por el subproceso de trabajo como parámetros o valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="32b3c-115">Data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="32b3c-116">Estos datos no deberían estar basados en la pila, ya que se hará referencia a él después de completar la operación de puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="32b3c-116">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span> |
| <span data-ttu-id="32b3c-117">As</span><span class="sxs-lookup"><span data-stu-id="32b3c-117">pEvent</span></span>                    | <span data-ttu-id="32b3c-118">Objeto de evento que un subproceso de trabajo puede señalar para indicar la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="32b3c-118">Event object that a worker thread can signal to indicate the completion of the operation.</span></span>                                                                                         |
| <span data-ttu-id="32b3c-119">uMsg</span><span class="sxs-lookup"><span data-stu-id="32b3c-119">uMsg</span></span>                      | <span data-ttu-id="32b3c-120">Código de solicitud definido por el cliente de la clase de subproceso y comprensible por la función de subproceso de trabajo invalidada.</span><span class="sxs-lookup"><span data-stu-id="32b3c-120">Request code that is defined by the client of the thread class and understood by the overridden worker thread function.</span></span>                                                           |
| <span data-ttu-id="32b3c-121">Funciones de miembro</span><span class="sxs-lookup"><span data-stu-id="32b3c-121">Member Functions</span></span>          | <span data-ttu-id="32b3c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="32b3c-122">Description</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="32b3c-123">**CMsg**</span><span class="sxs-lookup"><span data-stu-id="32b3c-123">**CMsg**</span></span>](cmsg-cmsg.md) | <span data-ttu-id="32b3c-124">Construye un objeto [**CMsg**](cmsg-cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="32b3c-124">Constructs a [**CMsg**](cmsg-cmsg.md) object.</span></span>                                                                                                                                    |



 

 

 



