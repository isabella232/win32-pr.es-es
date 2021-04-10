---
title: Usar Administración remota de Windows
description: Administración remota de Windows está diseñado para mejorar la administración de hardware en un entorno de red con varios dispositivos que ejecutan diversos sistemas operativos.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149453"
---
# <a name="using-windows-remote-management"></a><span data-ttu-id="a5eb8-103">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="a5eb8-103">Using Windows Remote Management</span></span>

<span data-ttu-id="a5eb8-104">Administración remota de Windows está diseñado para mejorar la administración de hardware en un entorno de red con varios dispositivos que ejecutan diversos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="a5eb8-104">Windows Remote Management is intended to improve hardware management in a network environment with various devices running a variety of operating systems.</span></span> <span data-ttu-id="a5eb8-105">Todo el diseño del servicio está orientado a la monitorización y la administración de equipos remotos implementando un protocolo estándar interoperable.</span><span class="sxs-lookup"><span data-stu-id="a5eb8-105">The entire design of the service is focused on monitoring and managing remote computers by implementing an interoperable standard protocol.</span></span>

<span data-ttu-id="a5eb8-106">Dado que la [API de scripting de WinRM](winrm-scripting-api.md) y la API de C++ de [WinRM](winrm-c---api.md) implementan y modelan estrechamente las operaciones definidas para el protocolo de WS-Management, los scripts y las aplicaciones reciben secuencias de XML en respuesta a las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="a5eb8-106">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) implement and closely model the operations defined for the WS-Management protocol, scripts and applications receive streams of XML in response to requests.</span></span> <span data-ttu-id="a5eb8-107">Los parámetros de entrada para llamadas a métodos se deben construir en XML.</span><span class="sxs-lookup"><span data-stu-id="a5eb8-107">Input parameters to method calls must be constructed in XML.</span></span> <span data-ttu-id="a5eb8-108">Puede usar los métodos de la API de [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) para mostrar o construir cadenas XML.</span><span class="sxs-lookup"><span data-stu-id="a5eb8-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API to display or construct XML strings.</span></span> <span data-ttu-id="a5eb8-109">Para obtener un ejemplo, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="a5eb8-109">For an example, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="a5eb8-110">La lista siguiente incluye temas en los que se describe cómo usar el scripting de WinRM:</span><span class="sxs-lookup"><span data-stu-id="a5eb8-110">The following list includes topics that describe how to use WinRM scripting:</span></span>

-   [<span data-ttu-id="a5eb8-111">Detección de si un equipo remoto admite WS-Management protocolo</span><span class="sxs-lookup"><span data-stu-id="a5eb8-111">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [<span data-ttu-id="a5eb8-112">Obtención de datos del equipo local</span><span class="sxs-lookup"><span data-stu-id="a5eb8-112">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
-   [<span data-ttu-id="a5eb8-113">Obtención de datos de un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="a5eb8-113">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
-   [<span data-ttu-id="a5eb8-114">Enumerar o enumerar todas las instancias de un recurso</span><span class="sxs-lookup"><span data-stu-id="a5eb8-114">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
-   [<span data-ttu-id="a5eb8-115">Consultar instancias específicas de un recurso</span><span class="sxs-lookup"><span data-stu-id="a5eb8-115">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
-   [<span data-ttu-id="a5eb8-116">Mostrar la salida XML de los scripts de WinRM</span><span class="sxs-lookup"><span data-stu-id="a5eb8-116">Displaying XML Output from WinRM Scripts</span></span>](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a><span data-ttu-id="a5eb8-117">Seguimiento de la actividad de WinRM</span><span class="sxs-lookup"><span data-stu-id="a5eb8-117">Tracing WinRM Activity</span></span>

<span data-ttu-id="a5eb8-118">Dado que WinRM obtiene datos a través de [instrumental de administración de Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), puede realizar un seguimiento de la actividad de WMI resultante de los mensajes de WinRM.</span><span class="sxs-lookup"><span data-stu-id="a5eb8-118">Because WinRM obtains data through [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), you can trace WMI activity that results from WinRM messages.</span></span> <span data-ttu-id="a5eb8-119">A partir de Windows Vista, el servicio WMI ya no utiliza los [archivos de registro de WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="a5eb8-119">Starting with Windows Vista, the WMI service no longer uses the [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span> <span data-ttu-id="a5eb8-120">En su lugar, utiliza el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) y los eventos están disponibles a través de la interfaz de usuario de **visor de eventos** o la herramienta de línea de comandos Evtutil.</span><span class="sxs-lookup"><span data-stu-id="a5eb8-120">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Evtutil command line tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5eb8-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5eb8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5eb8-122">Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="a5eb8-122">Windows Remote Management</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="a5eb8-123">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="a5eb8-123">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="a5eb8-124">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="a5eb8-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="a5eb8-125">Scripting en Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="a5eb8-125">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 