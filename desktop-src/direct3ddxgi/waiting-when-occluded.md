---
description: Las aplicaciones pueden esperar en un evento cuando no es necesario representar en la pantalla (es decir, mientras se ocluidos).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Esperar en un evento cuando no es necesaria la representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686264"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a><span data-ttu-id="bc42f-103">Esperar en un evento cuando no es necesaria la representación</span><span class="sxs-lookup"><span data-stu-id="bc42f-103">Waiting on an event when rendering is unnecessary</span></span>

<span data-ttu-id="bc42f-104">Las aplicaciones pueden esperar en un evento cuando no es necesario representar en la pantalla (es decir, mientras se ocluidos).</span><span class="sxs-lookup"><span data-stu-id="bc42f-104">Apps can wait on an event when rendering to the screen is unnecessary (that is, while they are occluded).</span></span> <span data-ttu-id="bc42f-105">Cuando el Administrador de ventanas de escritorio (DWM) o una aplicación es ocluidos, no es necesario realizar ninguna representación y el sistema operativo puede permanecer en un estado de energía inferior durante períodos de tiempo más largos.</span><span class="sxs-lookup"><span data-stu-id="bc42f-105">When the Desktop Window Manager (DWM) or an app is occluded, no rendering is necessary and the operating system can stay in lower power states for longer periods of time.</span></span> <span data-ttu-id="bc42f-106">Esto ahorra energía y amplía la duración de la batería.</span><span class="sxs-lookup"><span data-stu-id="bc42f-106">This saves power and extends battery life.</span></span>

<span data-ttu-id="bc42f-107">Una aplicación puede esperar en un evento cuando:</span><span class="sxs-lookup"><span data-stu-id="bc42f-107">An app can wait on an event when:</span></span>

-   <span data-ttu-id="bc42f-108">Todos los monitores están desactivados.</span><span class="sxs-lookup"><span data-stu-id="bc42f-108">All the monitors are off.</span></span>
-   <span data-ttu-id="bc42f-109">La sesión en la que se ejecuta la aplicación está desconectada.</span><span class="sxs-lookup"><span data-stu-id="bc42f-109">The session that the app runs in is disconnected.</span></span>
-   <span data-ttu-id="bc42f-110">La aplicación se ejecuta en pantalla completa exclusivamente en una única configuración de monitor.</span><span class="sxs-lookup"><span data-stu-id="bc42f-110">The app runs in full screen exclusively on a single monitor configuration.</span></span>
-   <span data-ttu-id="bc42f-111">La aplicación se ejecuta en un escritorio diferente que el escritorio activo y no tiene permiso para representarse en el escritorio activo.</span><span class="sxs-lookup"><span data-stu-id="bc42f-111">The app runs on a different desktop than the active desktop and does not have permission to render on the active desktop.</span></span>

<span data-ttu-id="bc42f-112">El sistema operativo desencadena el evento cuando la aplicación puede representarse de nuevo.</span><span class="sxs-lookup"><span data-stu-id="bc42f-112">The operating system triggers the event when the app is able to render again.</span></span> <span data-ttu-id="bc42f-113">El evento no se borra durante la actualización de un controlador o el proceso de detección y recuperación (TDR) de tiempo de espera, pero se borra cuando el nuevo adaptador y los monitores se activan.</span><span class="sxs-lookup"><span data-stu-id="bc42f-113">The event is not cleared during a driver upgrade, or timeout detection and recovery (TDR) procession, however it is cleared when the new adapter and monitors become active.</span></span>

<span data-ttu-id="bc42f-114">Si desea que la aplicación reciba notificaciones sobre los cambios de estado de la oclusión, la aplicación debe registrarse para estos cambios.</span><span class="sxs-lookup"><span data-stu-id="bc42f-114">If you want your app to be notified about changes of occlusion status, the app must register for these changes.</span></span> <span data-ttu-id="bc42f-115">Una aplicación puede registrarse para recibir notificaciones sobre los cambios de estado de la oclusión a través de un mensaje a una ventana o a través de la señalización de eventos.</span><span class="sxs-lookup"><span data-stu-id="bc42f-115">An app can register to be notified about changes of occlusion status through a message to a window or through event signaling.</span></span> <span data-ttu-id="bc42f-116">Para registrarse para recibir mensajes de notificación en una ventana sobre los cambios de estado de la oclusión, una aplicación llama al método [**IDXGIFactory2:: RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) .</span><span class="sxs-lookup"><span data-stu-id="bc42f-116">To register to receive notification messages to a window about occlusion status changes, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) method.</span></span> <span data-ttu-id="bc42f-117">Para registrarse para recibir notificaciones de los cambios de estado de la oclusión a través de la señalización de eventos, una aplicación llama al método [**IDXGIFactory2:: RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) .</span><span class="sxs-lookup"><span data-stu-id="bc42f-117">To register to receive notification of occlusion status changes via event signaling, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) method.</span></span> <span data-ttu-id="bc42f-118">Ambos métodos devuelven un puntero a un valor de clave que la aplicación puede usar para anular el registro de la notificación.</span><span class="sxs-lookup"><span data-stu-id="bc42f-118">Both methods return a pointer to a key value that the app can use to unregister the notification.</span></span> <span data-ttu-id="bc42f-119">Para anular el registro de la notificación, la aplicación pasa este valor de clave al método [**IDXGIFactory2:: UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .</span><span class="sxs-lookup"><span data-stu-id="bc42f-119">To unregister the notification, the app passes this key value to the [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc42f-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc42f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc42f-121">Mejoras en DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="bc42f-121">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



