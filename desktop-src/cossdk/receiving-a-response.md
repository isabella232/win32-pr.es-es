---
description: Recibir una respuesta
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Recibir una respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539286"
---
# <a name="receiving-a-response"></a><span data-ttu-id="01396-103">Recibir una respuesta</span><span class="sxs-lookup"><span data-stu-id="01396-103">Receiving a Response</span></span>

<span data-ttu-id="01396-104">Dado que los componentes en cola están diseñados para funcionar de forma asincrónica, las aplicaciones cliente no deben bloquearse mientras se espera una respuesta de una solicitud en cola.</span><span class="sxs-lookup"><span data-stu-id="01396-104">Because queued components are designed to work asynchronously, client applications should not block while waiting for a response from a queued request.</span></span> <span data-ttu-id="01396-105">No obstante, a menudo resulta útil para la aplicación cliente o una aplicación relacionada en el equipo cliente para recibir una respuesta a la larga.</span><span class="sxs-lookup"><span data-stu-id="01396-105">Nevertheless, it is often useful for the client application or a related application on the client machine to receive a response eventually.</span></span> <span data-ttu-id="01396-106">Por ejemplo, es posible que un cliente desee recibir una notificación cuando se haya completado correctamente una transacción solicitada.</span><span class="sxs-lookup"><span data-stu-id="01396-106">For example, a client may want to be notified when a requested transaction has been completed successfully.</span></span>

<span data-ttu-id="01396-107">Hay varias maneras de que un componente en cola envíe una respuesta de vuelta a su llamador de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="01396-107">There are a variety of ways for a queued component to send a response back to its caller asynchronously.</span></span> <span data-ttu-id="01396-108">Por ejemplo, podría enviar un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="01396-108">For example, it could send an email.</span></span> <span data-ttu-id="01396-109">Como alternativa, el servidor podría publicar eventos débilmente acoplados a los que el cliente podría suscribirse.</span><span class="sxs-lookup"><span data-stu-id="01396-109">Alternatively, the server could publish loosely coupled events to which the client could subscribe.</span></span>

<span data-ttu-id="01396-110">Otra forma de que un cliente obtenga una respuesta de un componente en cola que se ejecuta en un servidor es para que el cliente pase el método llamado a un objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="01396-110">Another way for a client to obtain a response from a queued component that runs on a server is for the client to pass the called method a notification object.</span></span> <span data-ttu-id="01396-111">Un objeto de notificación es una instancia de un componente en cola que se ejecuta en el cliente.</span><span class="sxs-lookup"><span data-stu-id="01396-111">A notification object is an instance of a queued component that runs on the client.</span></span> <span data-ttu-id="01396-112">Este tipo de objeto de notificación podría ser bastante sencillo, que solo contiene un entero que se usa para representar un valor de error, o podría ser bastante complejo, con toda la información necesaria para revertir una transacción en el cliente.</span><span class="sxs-lookup"><span data-stu-id="01396-112">Such a notification object might be quite simple, containing only an integer that is used to represent an error value, or it might be quite complex, containing all the information necessary to roll back a transaction on the client.</span></span> <span data-ttu-id="01396-113">En cualquier caso, el cliente que realiza la llamada pasa un objeto de notificación como parámetro de entrada siempre que se espera una respuesta de un componente en cola que se ejecuta en un servidor.</span><span class="sxs-lookup"><span data-stu-id="01396-113">In either case, the calling client passes a notification object as an input parameter whenever it desires a response from a queued component that runs on a server.</span></span> <span data-ttu-id="01396-114">Dado que el objeto de notificación está en cola, el servidor puede llamar a en sus métodos para modificar su estado, que el cliente puede leer posteriormente.</span><span class="sxs-lookup"><span data-stu-id="01396-114">Because the notification object is queued, the server can call on its methods to alter its state, which can subsequently be read out by the client.</span></span> <span data-ttu-id="01396-115">En este escenario, el servicio de componentes en cola de COM+ se utiliza tanto en el cliente como en el servidor para permitir la comunicación asincrónica en ambas direcciones.</span><span class="sxs-lookup"><span data-stu-id="01396-115">In this scenario, the COM+ queued components service is used on both the client and the server to allow asynchronous communication in both directions.</span></span>

 

 



