---
description: Los monitores están diseñados para usar Instrumental de administración de Windows (WMI) para activar eventos en equipos locales o remotos.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Supervisar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497614"
---
# <a name="monitor-events"></a><span data-ttu-id="06c9b-103">Supervisar eventos</span><span class="sxs-lookup"><span data-stu-id="06c9b-103">Monitor Events</span></span>

<span data-ttu-id="06c9b-104">Los monitores están diseñados para usar [instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para activar eventos en equipos locales o remotos.</span><span class="sxs-lookup"><span data-stu-id="06c9b-104">Monitors are designed to use [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to fire events to local or remote computers.</span></span>

> [!Note]  
> <span data-ttu-id="06c9b-105">Dado que los monitores usan una captura en tiempo real, solo pueden capturar datos en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="06c9b-105">Because monitors use a real-time capture they can only capture data at the local computer.</span></span> <span data-ttu-id="06c9b-106">Se trata de una limitación de la interfaz **IRTC** del proveedor de paquetes de red.</span><span class="sxs-lookup"><span data-stu-id="06c9b-106">This is a limitation of the network packet provider's **IRTC** interface.</span></span> <span data-ttu-id="06c9b-107">Sin embargo, mediante el uso de eventos de WMI, los datos capturados se pueden examinar localmente mientras se pueden enviar eventos a equipos locales o remotos.</span><span class="sxs-lookup"><span data-stu-id="06c9b-107">However, by using WMI events, the captured data can be examined locally while events can be sent to local or remote computers.</span></span>

 

<span data-ttu-id="06c9b-108">Los monitores no se comunican directamente con WMI.</span><span class="sxs-lookup"><span data-stu-id="06c9b-108">Monitors do not communicate directly with WMI.</span></span> <span data-ttu-id="06c9b-109">El [*servicio de control de supervisión*](m.md) (MCSVC) proporciona una interfaz (denominada [IMonitorEventer](imonitoreventer.md)) que el monitor puede utilizar para obtener una estructura de datos de evento y rellenarla con la información pertinente.</span><span class="sxs-lookup"><span data-stu-id="06c9b-109">The [*Monitor Control Service*](m.md) (MCSVC) provides an interface (called [IMonitorEventer](imonitoreventer.md)), which the monitor can use to obtain an event data structure and fill it with the relevant information.</span></span> <span data-ttu-id="06c9b-110">A continuación, MCSVC puede enviar la estructura de datos de evento a WMI, que a su vez activa el evento.</span><span class="sxs-lookup"><span data-stu-id="06c9b-110">The MCSVC can then send the event data structure to WMI, which in turn fires the event.</span></span>

 

 
