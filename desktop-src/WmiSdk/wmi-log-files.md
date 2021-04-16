---
description: WMI utiliza el seguimiento de eventos (ETW) y los eventos se pueden obtener a través de la interfaz de usuario Visor de eventos o la herramienta de línea de comandos wevtutil. Para obtener más información, vea seguimiento de la actividad WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Archivos de registro de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696781"
---
# <a name="wmi-log-files"></a><span data-ttu-id="55841-104">Archivos de registro de WMI</span><span class="sxs-lookup"><span data-stu-id="55841-104">WMI Log Files</span></span>

<span data-ttu-id="55841-105">WMI utiliza el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) y los eventos se pueden obtener a través de la interfaz de usuario **visor de eventos** o la herramienta de línea de comandos wevtutil.</span><span class="sxs-lookup"><span data-stu-id="55841-105">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events can be obtained through the **Event Viewer** user interface or the Wevtutil command line tool.</span></span> <span data-ttu-id="55841-106">Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="55841-106">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

-   [<span data-ttu-id="55841-107">Seguimiento de eventos en lugar de registros de texto</span><span class="sxs-lookup"><span data-stu-id="55841-107">Event Tracing Instead of Text Logs</span></span>](#event-tracing-instead-of-text-logs)
-   [<span data-ttu-id="55841-108">Archivos de registro de WMI</span><span class="sxs-lookup"><span data-stu-id="55841-108">WMI Log Files</span></span>](#wmi-log-files)
-   [<span data-ttu-id="55841-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55841-109">Related topics</span></span>](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a><span data-ttu-id="55841-110">Seguimiento de eventos en lugar de registros de texto</span><span class="sxs-lookup"><span data-stu-id="55841-110">Event Tracing Instead of Text Logs</span></span>

<span data-ttu-id="55841-111">La actividad del servicio WMI se registra en el archivo WMITracing. log.</span><span class="sxs-lookup"><span data-stu-id="55841-111">WMI service activity is recorded in the WMITracing.log file.</span></span> <span data-ttu-id="55841-112">Para obtener más información sobre la habilitación del seguimiento de eventos WMI y el acceso al archivo WMITracing. log, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="55841-112">For more information about enabling WMI event tracing and accessing the WMITracing.log file, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span> <span data-ttu-id="55841-113">Los proveedores Modelo de controlador de Windows (WDM) continúan registrando en el archivo Wbemprov. log.</span><span class="sxs-lookup"><span data-stu-id="55841-113">Windows Driver Model (WDM) providers continue to log in the Wbemprov.log file.</span></span>

## <a name="wmi-log-files"></a><span data-ttu-id="55841-114">Archivos de registro de WMI</span><span class="sxs-lookup"><span data-stu-id="55841-114">WMI Log Files</span></span>

<span data-ttu-id="55841-115">El servicio WMI y algunos proveedores escriben archivos de registro de texto en los eventos de registro.</span><span class="sxs-lookup"><span data-stu-id="55841-115">The WMI service and some providers write text log files to record events.</span></span>

<dl> <dt>

<span data-ttu-id="55841-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Archivos de registro del proveedor WMI](wmi-provider-log-files.md)</span><span class="sxs-lookup"><span data-stu-id="55841-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI Provider Log Files](wmi-provider-log-files.md)</span></span>
</dt> <dd>

<span data-ttu-id="55841-117">Los proveedores WMI también pueden mantener registros.</span><span class="sxs-lookup"><span data-stu-id="55841-117">WMI providers also may maintain logs.</span></span> <span data-ttu-id="55841-118">Los archivos de registro que aparecen en un sistema dependen de los proveedores instalados.</span><span class="sxs-lookup"><span data-stu-id="55841-118">Which log files appear on a system depends on which providers are installed.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="55841-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55841-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55841-120">Referencia de WMI</span><span class="sxs-lookup"><span data-stu-id="55841-120">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="55841-121">Seguimiento de la actividad WMI</span><span class="sxs-lookup"><span data-stu-id="55841-121">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> <dt>

[<span data-ttu-id="55841-122">Registrar la actividad WMI</span><span class="sxs-lookup"><span data-stu-id="55841-122">Logging WMI Activity</span></span>](logging-wmi-activity.md)
</dt> </dl>

 

 
