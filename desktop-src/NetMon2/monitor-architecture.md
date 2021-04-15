---
description: En la siguiente ilustración se muestra la relación entre los monitores y otros componentes de la arquitectura de Monitor de red.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Arquitectura de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549919"
---
# <a name="monitor-architecture"></a><span data-ttu-id="3faf8-103">Arquitectura de monitor</span><span class="sxs-lookup"><span data-stu-id="3faf8-103">Monitor Architecture</span></span>

<span data-ttu-id="3faf8-104">En la siguiente ilustración se muestra la relación entre los [*monitores*](m.md) y otros componentes de la arquitectura de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="3faf8-104">The following figure shows the relationship between [*monitors*](m.md) and other components of the Network Monitor architecture.</span></span>

![relación entre monitores y otros componentes de monitor de red](images/nmarch2.png)

<span data-ttu-id="3faf8-106">El tráfico de red se recopila (como fotogramas individuales) del controlador NDIS.</span><span class="sxs-lookup"><span data-stu-id="3faf8-106">The network traffic is collected (as individual frames) from the NDIS driver.</span></span> <span data-ttu-id="3faf8-107">A continuación, el controlador de Monitor de red (Nmnt.sys) enruta los fotogramas a un proveedor de paquetes de red (NPP), que a su vez captura los datos en modo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="3faf8-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which in turn captures the data in real-time mode.</span></span> <span data-ttu-id="3faf8-108">NPP es una colección de interfaces COM que se utiliza para capturar datos.</span><span class="sxs-lookup"><span data-stu-id="3faf8-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="3faf8-109">En este caso, la interfaz [**IRTC**](irtc.md) se utiliza para realizar una captura en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="3faf8-109">In this case, the [**IRTC**](irtc.md) interface is used to perform a real-time capture.</span></span>

> [!Note]  
> <span data-ttu-id="3faf8-110">El NPP se utiliza para las capturas retrasadas y en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="3faf8-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="3faf8-111">En el caso de las capturas retrasadas usadas por expertos y analizadores, se usa la interfaz [**IDelaydC**](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="3faf8-111">For delayed captures used by experts and parsers, the [**IDelaydC**](idelaydc.md) interface is used.</span></span>

 

<span data-ttu-id="3faf8-112">A continuación, el monitor examina los datos capturados en modo en tiempo real, detectando condiciones de red específicas y generando eventos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="3faf8-112">The monitor then examines the captured data in real-time mode, detecting specific network conditions and generating events as required.</span></span>

<span data-ttu-id="3faf8-113">Las aplicaciones de supervisión usan otros tres componentes: la herramienta supervisar control, el servicio de control de supervisión (MCSVC) y el Visor de eventos:</span><span class="sxs-lookup"><span data-stu-id="3faf8-113">Three other components are used by monitor applications: the Monitor Control Tool, the Monitor Control Service (MCSVC), and the Event Viewer:</span></span>

-   <span data-ttu-id="3faf8-114">La herramienta supervisar control se utiliza para administrar las aplicaciones de supervisión.</span><span class="sxs-lookup"><span data-stu-id="3faf8-114">The Monitor Control Tool is used to manage your monitor applications.</span></span> <span data-ttu-id="3faf8-115">Esto incluye la configuración y ejecución de todas las aplicaciones de supervisión.</span><span class="sxs-lookup"><span data-stu-id="3faf8-115">This includes configuring and running all your monitor applications.</span></span>
-   <span data-ttu-id="3faf8-116">El servicio de control de supervisión (MCSVC) desencadena eventos, proporciona un vínculo de comunicaciones a WMI para la visualización de eventos y coordina el procesamiento de las operaciones de supervisión.</span><span class="sxs-lookup"><span data-stu-id="3faf8-116">The Monitor Control Service (MCSVC) fires events, provides a communications link to WMI for event viewing, and coordinates the processing of monitor operations.</span></span>
-   <span data-ttu-id="3faf8-117">El Visor de eventos muestra los eventos desencadenados por el servicio de control de supervisión.</span><span class="sxs-lookup"><span data-stu-id="3faf8-117">The Event Viewer displays the events fired by the Monitor Control Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3faf8-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3faf8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3faf8-119">**IMonitor**</span><span class="sxs-lookup"><span data-stu-id="3faf8-119">**IMonitor**</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="3faf8-120">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="3faf8-120">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="3faf8-121">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="3faf8-121">**IRTC**</span></span>](irtc.md)
</dt> </dl>

 

 



