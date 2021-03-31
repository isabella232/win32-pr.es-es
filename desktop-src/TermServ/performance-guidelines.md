---
title: Directrices de rendimiento
description: Directrices para desarrollar aplicaciones que funcionan bien en un entorno de Servicios de Escritorio remoto.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419120"
---
# <a name="performance-guidelines"></a><span data-ttu-id="561bd-103">Directrices de rendimiento</span><span class="sxs-lookup"><span data-stu-id="561bd-103">Performance guidelines</span></span>

<span data-ttu-id="561bd-104">En las secciones siguientes se proporcionan instrucciones para desarrollar aplicaciones que funcionan bien en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="561bd-104">The following sections provide guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="561bd-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="561bd-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="561bd-106">Efectos gráficos</span><span class="sxs-lookup"><span data-stu-id="561bd-106">Graphic effects</span></span>](graphic-effects.md)
</dt> <dd>

<span data-ttu-id="561bd-107">Una lista de características que deben deshabilitarse cuando se ejecuta como una sesión remota en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="561bd-107">A list of features that should be disabled when running as a remote session in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="561bd-108">Instrucciones para tareas en segundo plano en Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="561bd-108">Guidelines for background tasks in Remote Desktop Services</span></span>](background-tasks.md)
</dt> <dd>

<span data-ttu-id="561bd-109">Para maximizar la disponibilidad de la CPU para todos los usuarios, deshabilite las tareas en segundo plano cuando se ejecute en un entorno de Servicios de Escritorio remoto o cree tareas en segundo plano eficaces que no consuman muchos recursos.</span><span class="sxs-lookup"><span data-stu-id="561bd-109">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

</dd> <dt>

[<span data-ttu-id="561bd-110">Uso de subprocesos</span><span class="sxs-lookup"><span data-stu-id="561bd-110">Thread usage</span></span>](thread-usage.md)
</dt> <dd>

<span data-ttu-id="561bd-111">Debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno de Servicios de Escritorio remoto multiusuario y multiprocesador.</span><span class="sxs-lookup"><span data-stu-id="561bd-111">You should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="561bd-112">Detección del entorno de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="561bd-112">Detecting the Remote Desktop Services environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="561bd-113">Para optimizar el rendimiento, es recomendable que las aplicaciones detecten si se ejecutan en una sesión de cliente Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="561bd-113">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span>

</dd> </dl>

<span data-ttu-id="561bd-114">Compruebe si hay pérdidas de memoria en la aplicación y resuelva los problemas.</span><span class="sxs-lookup"><span data-stu-id="561bd-114">Check your application for memory leaks and resolve any problems.</span></span> <span data-ttu-id="561bd-115">Por supuesto, esto es un buen consejo para cualquier aplicación, pero en un entorno de Servicios de Escritorio remoto, una aplicación se puede ejecutar varias veces por varios usuarios, lo que aumenta rápidamente el efecto de una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="561bd-115">Of course this is good advice for any application, but in a Remote Desktop Services environment, an application can be run multiple times by multiple users, thus rapidly magnifying the effect of a memory leak.</span></span>

<span data-ttu-id="561bd-116">Las animaciones, imágenes de gran tamaño, audio y otros servicios con un uso intensivo de ancho de banda deben ser configurables.</span><span class="sxs-lookup"><span data-stu-id="561bd-116">Animations, large images, audio, and other bandwidth-intensive services must be configurable.</span></span> <span data-ttu-id="561bd-117">Cuando estos servicios no son la función principal, pueden desactivarse de forma predeterminada para las sesiones remotas, pero se habilitan cuando una sesión se ejecuta localmente o a través de una conexión de ancho de banda alto.</span><span class="sxs-lookup"><span data-stu-id="561bd-117">When these services are not the primary function, they can be off by default for remote sessions, but enabled when a session is running locally or over a high bandwidth connection.</span></span> <span data-ttu-id="561bd-118">Si el propósito de una aplicación es proporcionar servicios de gran ancho de banda, como la transmisión por secuencias de vídeo, el servicio no tiene que estar desactivado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="561bd-118">If the purpose of an application is to provide high bandwidth services, such as streaming video broadcasts, the service does not have to be off by default.</span></span>

 

 




