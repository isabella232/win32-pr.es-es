---
description: Procedimientos recomendados para minimizar los servicios que no responde
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Procedimientos recomendados para minimizar los servicios que no responde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90416e8256383e16fd78c436dfaa8d6a2186c540
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088003"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="ef812-103">Procedimientos recomendados para minimizar los servicios que no responde</span><span class="sxs-lookup"><span data-stu-id="ef812-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="ef812-104">Plataforma afectada</span><span class="sxs-lookup"><span data-stu-id="ef812-104">Affected Platform</span></span>

 <span data-ttu-id="ef812-105">**Clientes:** Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef812-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="ef812-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef812-106">Description</span></span>

<span data-ttu-id="ef812-107">Los servicios que no responden pueden dar lugar a tiempos de espera, sesiones terminadas e incluso pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="ef812-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="ef812-108">El empleo de procedimientos recomendados puede reducir considerablemente la aparición de servicios que no responden.</span><span class="sxs-lookup"><span data-stu-id="ef812-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="ef812-109">Prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="ef812-109">Best Practices</span></span>

<span data-ttu-id="ef812-110">Asegúrese de que las aplicaciones y todos sus servicios y controladores dependientes responden a las notificaciones de encendido y apagado del sistema.</span><span class="sxs-lookup"><span data-stu-id="ef812-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="ef812-111">Todas las aplicaciones deben responder de forma rápida y adecuada a los mensajes de apagado, como WM \_ QUERYENDSESSION y WM ENDSESSION, que indican que hay un apagado \_ en curso.</span><span class="sxs-lookup"><span data-stu-id="ef812-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="ef812-112">Todos los servicios deben responder rápidamente a las notificaciones de cierre de SCM.</span><span class="sxs-lookup"><span data-stu-id="ef812-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="ef812-113">Si no lo hacen, la máquina los trata como no responde e inicia un tiempo de espera de 20 segundos y los detiene, lo que abre la posibilidad de que se pierdan datos.</span><span class="sxs-lookup"><span data-stu-id="ef812-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="ef812-114">Esto también agrega 20 segundos al tiempo de apagado de una máquina.</span><span class="sxs-lookup"><span data-stu-id="ef812-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="ef812-115">Todos los servicios que tienen dependencias del controlador de dispositivo kernel deben responder de forma rápida y adecuada a la notificación \_ IRP MJ SHUTDOWN en \_ sus rutinas DispatchShutdown.</span><span class="sxs-lookup"><span data-stu-id="ef812-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ef812-116">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="ef812-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="ef812-117">Kit de herramientas de rendimiento de Windows</span><span class="sxs-lookup"><span data-stu-id="ef812-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



