---
title: Cómo funcionan las notificaciones
description: Cómo funcionan las notificaciones
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421477"
---
# <a name="how-notifications-work"></a><span data-ttu-id="5ec25-103">Cómo funcionan las notificaciones</span><span class="sxs-lookup"><span data-stu-id="5ec25-103">How Notifications Work</span></span>

<span data-ttu-id="5ec25-104">Las notificaciones se originan en la aplicación de objetos y fluyen al contenedor mediante el controlador de objetos.</span><span class="sxs-lookup"><span data-stu-id="5ec25-104">Notifications originate in the object application and flow to the container by way of the object handler.</span></span> <span data-ttu-id="5ec25-105">Si el objeto es un objeto vinculado, el objeto vinculado intercepta las notificaciones desde el controlador de objetos y notifica al contenedor directamente.</span><span class="sxs-lookup"><span data-stu-id="5ec25-105">If the object is a linked object, the linked object intercepts the notifications from the object handler and notifies the container directly.</span></span>

<span data-ttu-id="5ec25-106">Una aplicación de objeto debe administrar las solicitudes de registro, realizando un seguimiento del lugar en el que se enviarán las notificaciones y el envío de las notificaciones cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5ec25-106">An object application must manage registration requests, keeping track of where to send which notifications and sending those notifications when appropriate.</span></span> <span data-ttu-id="5ec25-107">OLE proporciona dos objetos de componente para simplificar esta tarea: OleAdviseHolder para las notificaciones de documentos compuestos y DataAdviseHolder para las notificaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="5ec25-107">OLE provides two component objects to simplify this task: the OleAdviseHolder for compound document notifications and the DataAdviseHolder for data notifications.</span></span>

<span data-ttu-id="5ec25-108">Las aplicaciones de objeto determinan las condiciones que solicitan el envío de cada notificación específica y la frecuencia con la que debe enviarse cada notificación.</span><span class="sxs-lookup"><span data-stu-id="5ec25-108">Object applications determine the conditions that prompt the sending of each specific notification and the frequency with which each notification should be sent.</span></span> <span data-ttu-id="5ec25-109">Cuando es adecuado para enviar varias notificaciones, no importa qué notificación se envía en primer lugar; se pueden enviar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="5ec25-109">When it is appropriate for multiple notifications to be sent, it does not matter which notification is sent first; they can be sent in any order.</span></span>

<span data-ttu-id="5ec25-110">Los intervalos de las notificaciones afectan al rendimiento y la coordinación entre una aplicación de objeto y sus contenedores.</span><span class="sxs-lookup"><span data-stu-id="5ec25-110">The timing of notifications affects the performance and coordination between an object application and its containers.</span></span> <span data-ttu-id="5ec25-111">Mientras que las notificaciones enviadas con demasiada frecuencia se ralentizan el procesamiento, las notificaciones se envían con poca frecuencia en un contenedor fuera de sincronización.</span><span class="sxs-lookup"><span data-stu-id="5ec25-111">Whereas notifications sent too frequently slow processing, notifications sent too infrequently result in an out-of-sync container.</span></span> <span data-ttu-id="5ec25-112">La frecuencia de notificación puede compararse con la velocidad a la que se repinta una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ec25-112">Notification frequency can be compared with the rate at which an application repaints.</span></span> <span data-ttu-id="5ec25-113">Por lo tanto, es aconsejable utilizar una lógica similar para el control de tiempo de las notificaciones (como se usa para la repintado).</span><span class="sxs-lookup"><span data-stu-id="5ec25-113">Therefore, using similar logic for the timing of notifications (as is used for repainting) is wise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ec25-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ec25-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec25-115">**CreateDataAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="5ec25-115">**CreateDataAdviseHolder**</span></span>](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[<span data-ttu-id="5ec25-116">**CreateOleAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="5ec25-116">**CreateOleAdviseHolder**</span></span>](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[<span data-ttu-id="5ec25-117">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="5ec25-117">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 