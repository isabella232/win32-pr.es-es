---
description: Un monitor es una biblioteca de vínculos dinámicos (DLL) que examina las capturas en tiempo real del tráfico de red.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001230"
---
# <a name="monitors"></a><span data-ttu-id="d0d54-103">Monitores</span><span class="sxs-lookup"><span data-stu-id="d0d54-103">Monitors</span></span>

<span data-ttu-id="d0d54-104">Un monitor es una biblioteca de vínculos dinámicos (DLL) que examina las capturas en tiempo real del tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="d0d54-104">A monitor is a dynamic-link library (DLL) that examines real-time captures of network traffic.</span></span> <span data-ttu-id="d0d54-105">Busca condiciones predefinidas y, después, genera eventos cuando se detectan esas condiciones.</span><span class="sxs-lookup"><span data-stu-id="d0d54-105">It searches for pre-defined conditions and then generates events when those conditions are detected.</span></span> <span data-ttu-id="d0d54-106">Por ejemplo, se puede desencadenar un evento cuando se intenta un salto de red, cuando una estación de trabajo no autorizada está entregando las direcciones IP o cuando se produce un error en un enrutador.</span><span class="sxs-lookup"><span data-stu-id="d0d54-106">For example, an event may be fired when a network break-in is attempted, when a rogue workstation is handing out IP addresses, or when a router fails.</span></span>

> [!Note]  
> <span data-ttu-id="d0d54-107">Si necesita realizar análisis detallados de los datos de red que requieren un análisis posterior a la captura, debe usar aplicaciones de [*analizador*](p.md) y de [*expertos*](e.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d54-107">If you need to perform detailed analyses on network data that requires a post-capture analysis, you must use [*expert*](e.md) and [*parser*](p.md) applications.</span></span>

 

<span data-ttu-id="d0d54-108">El [*servicio de control de supervisión*](m.md) (MCSVC) proporciona el marco de trabajo para administrar los monitores.</span><span class="sxs-lookup"><span data-stu-id="d0d54-108">The [*Monitor Control Service*](m.md) (MCSVC) provides the framework for managing your monitors.</span></span> <span data-ttu-id="d0d54-109">Proporciona funciones para cargar los archivos DLL del monitor y una interfaz de comunicaciones con la herramienta de control de supervisión para que pueda crear, configurar, iniciar, detener y deshabilitar varias instancias de los monitores.</span><span class="sxs-lookup"><span data-stu-id="d0d54-109">It provides functions to load the monitor DLLs, and a communications interface to the Monitor Control Tool so that you can create, configure, start, stop, and disable multiple instances of your monitors.</span></span>

<span data-ttu-id="d0d54-110">Los monitores se ejecutan en dos subprocesos de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d0d54-110">Monitors run in two threads of execution.</span></span> <span data-ttu-id="d0d54-111">MCSVC proporciona el primer subproceso, que proporciona control directo del monitor.</span><span class="sxs-lookup"><span data-stu-id="d0d54-111">The MCSVC provides the first thread, which provides direct control of the monitor.</span></span> <span data-ttu-id="d0d54-112">El segundo subproceso lo proporciona el [*proveedor de paquetes de red*](n.md) (NPP), que proporciona una manera de pasar los datos capturados, las estadísticas y el estado de la captura del NPP de vuelta al monitor.</span><span class="sxs-lookup"><span data-stu-id="d0d54-112">The second thread is provided by the [*network packet provider*](n.md) (NPP), which provides a way to pass the captured network data, statistics, and the status of the capture from the NPP back to the monitor.</span></span>

<span data-ttu-id="d0d54-113">Puede haber más de una instancia del mismo monitor para cada interfaz NPP en tiempo de ejecución que se usa para capturar datos.</span><span class="sxs-lookup"><span data-stu-id="d0d54-113">More than one instance of the same monitor can exist for each run-time NPP interface used to capture data.</span></span>

 

 



