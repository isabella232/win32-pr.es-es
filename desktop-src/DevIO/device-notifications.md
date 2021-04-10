---
description: El sistema difunde un conjunto de eventos de cambio de dispositivo predeterminados a todas las aplicaciones y servicios.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notificaciones de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153334"
---
# <a name="device-notifications"></a><span data-ttu-id="64994-103">Notificaciones de dispositivo</span><span class="sxs-lookup"><span data-stu-id="64994-103">Device Notifications</span></span>

<span data-ttu-id="64994-104">El sistema difunde un conjunto de eventos de cambio de dispositivo predeterminados a todas las aplicaciones y servicios.</span><span class="sxs-lookup"><span data-stu-id="64994-104">The system broadcasts a set of default device change events to all applications and services.</span></span> <span data-ttu-id="64994-105">No es necesario registrarse para recibir estos eventos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="64994-105">You do not need to register to receive these default events.</span></span> <span data-ttu-id="64994-106">Vea la sección Comentarios en [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="64994-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details.</span></span> <span data-ttu-id="64994-107">Para especificar otros eventos que debe recibir la aplicación o el servicio, utilice la función **RegisterDeviceNotification** .</span><span class="sxs-lookup"><span data-stu-id="64994-107">To specify other events your application or service should receive, use the **RegisterDeviceNotification** function.</span></span>

<span data-ttu-id="64994-108">Cuando una aplicación o un servicio llama a [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), también especifica la ventana que recibirá los eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="64994-108">When an application or service calls [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), it also specifies the window that will receive the notification events.</span></span> <span data-ttu-id="64994-109">Los servicios pueden especificar un identificador de estado de servicio en lugar de un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="64994-109">Services can specify a service status handle instead of a window handle.</span></span> <span data-ttu-id="64994-110">Si un servicio especifica su identificador de estado de servicio, su controlador de control de servicio recibirá los eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="64994-110">If a service specifies its service status handle, its service control handler will receive the notification events.</span></span> <span data-ttu-id="64994-111">Para obtener más información, vea [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="64994-111">For more information, see [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="64994-112">Asegúrese de controlar Plug and Play eventos de dispositivo lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="64994-112">Be sure to handle Plug and Play device events as quickly as possible.</span></span> <span data-ttu-id="64994-113">De lo contrario, es posible que el sistema deje de responder.</span><span class="sxs-lookup"><span data-stu-id="64994-113">Otherwise, the system may become unresponsive.</span></span> <span data-ttu-id="64994-114">Si el controlador de eventos va a realizar una operación que puede bloquear la ejecución (como e/s), es mejor iniciar otro subproceso para realizar la operación de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="64994-114">If your event handler is to perform an operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.</span></span>

<span data-ttu-id="64994-115">Los identificadores de notificación de dispositivo devueltos por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) deben cerrarse llamando a la función [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) cuando ya no se necesiten.</span><span class="sxs-lookup"><span data-stu-id="64994-115">Device notification handles returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) must be closed by calling the [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) function when they are no longer needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64994-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64994-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64994-117">Registro para recibir notificaciones del dispositivo</span><span class="sxs-lookup"><span data-stu-id="64994-117">Registering for device notification</span></span>](registering-for-device-notification.md)
</dt> </dl>

 

 
