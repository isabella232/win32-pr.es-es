---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Prácticas recomendadas para minimizar los servicios que no responden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913213"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="25392-103">Prácticas recomendadas para minimizar los servicios que no responden</span><span class="sxs-lookup"><span data-stu-id="25392-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="25392-104">Plataforma afectada</span><span class="sxs-lookup"><span data-stu-id="25392-104">Affected Platform</span></span>

 <span data-ttu-id="25392-105">**Clientes** : Windows Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="25392-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="25392-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="25392-106">Description</span></span>

<span data-ttu-id="25392-107">Los servicios que no responden pueden dar lugar a tiempos de espera, sesiones terminadas e incluso pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="25392-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="25392-108">La utilización de prácticas recomendadas puede reducir en gran medida la aparición de servicios que no responden.</span><span class="sxs-lookup"><span data-stu-id="25392-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="25392-109">Prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="25392-109">Best Practices</span></span>

<span data-ttu-id="25392-110">Asegúrese de que las aplicaciones y todos sus servicios y controladores dependientes responden a las notificaciones de encendido y apagado del sistema.</span><span class="sxs-lookup"><span data-stu-id="25392-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="25392-111">Todas las aplicaciones deben responder rápidamente y adecuadamente para cerrar mensajes como WM \_ QUERYENDSESSION y WM \_ ENDSESSION que indican que hay un apagado en curso.</span><span class="sxs-lookup"><span data-stu-id="25392-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="25392-112">Todos los servicios deben responder rápidamente a las notificaciones de apagado de SCM.</span><span class="sxs-lookup"><span data-stu-id="25392-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="25392-113">Si no lo hacen, el equipo los trata como si no respondiera e inicia un tiempo de espera de 20 segundos y los detiene, lo que abre la posibilidad de pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="25392-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="25392-114">Esto también agrega 20 segundos a la hora de cierre de un apagado del equipo.</span><span class="sxs-lookup"><span data-stu-id="25392-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="25392-115">Todos los servicios que tienen dependencias de controlador de dispositivo de kernel deben responder rápidamente y adecuadamente \_ a \_ la notificación de cierre de IRP MJ en sus rutinas de DispatchShutdown.</span><span class="sxs-lookup"><span data-stu-id="25392-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="25392-116">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="25392-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="25392-117">Kit de herramientas de rendimiento de Windows</span><span class="sxs-lookup"><span data-stu-id="25392-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



