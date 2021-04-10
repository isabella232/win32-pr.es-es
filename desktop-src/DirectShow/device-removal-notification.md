---
description: Notificación de eliminación de dispositivo
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notificación de eliminación de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103998039"
---
# <a name="device-removal-notification"></a><span data-ttu-id="a6df8-103">Notificación de eliminación de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a6df8-103">Device Removal Notification</span></span>

<span data-ttu-id="a6df8-104">Si el usuario quita un Plug and Play dispositivo que estaba usando el gráfico, el administrador de gráficos de filtros envía un evento de [**\_ \_ pérdida de dispositivo EC**](ec-device-lost.md) .</span><span class="sxs-lookup"><span data-stu-id="a6df8-104">If the user removes a Plug and Play device that the graph was using, the filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event.</span></span> <span data-ttu-id="a6df8-105">Si el dispositivo vuelve a estar disponible, el administrador de gráficos de filtros expone otro evento de **dispositivo de EC \_ \_ perdido** .</span><span class="sxs-lookup"><span data-stu-id="a6df8-105">If the device becomes available again, the filter graph manager posts another **EC\_DEVICE\_LOST** event.</span></span> <span data-ttu-id="a6df8-106">Sin embargo, el estado anterior del filtro de captura ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="a6df8-106">However, the previous state of the capture filter is no longer valid.</span></span> <span data-ttu-id="a6df8-107">La aplicación debe volver a generar el gráfico para usar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6df8-107">The application must rebuild the graph to use the device.</span></span>

<span data-ttu-id="a6df8-108">DirectShow no envía ningún evento cuando se conecta un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6df8-108">DirectShow does not send any event when a new device is plugged in.</span></span> <span data-ttu-id="a6df8-109">Para saber cuándo está disponible un nuevo dispositivo, la aplicación puede supervisar los mensajes de la ventana de WM \_ DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="a6df8-109">To learn when a new device is available, the application can monitor WM\_DEVICECHANGE window messages.</span></span> <span data-ttu-id="a6df8-110">Para obtener más información, vea "administración de dispositivos" en la documentación de Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="a6df8-110">For more information, see "Device Management" in the Platform SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6df8-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6df8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6df8-112">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a6df8-112">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



