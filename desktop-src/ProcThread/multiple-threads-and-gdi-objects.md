---
description: Para mejorar el rendimiento, el acceso a los objetos de la interfaz de dispositivo gráfico (GDI) (como las paletas, los contextos de dispositivo, las regiones y el like) no se serializan.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Varios subprocesos y objetos GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677856"
---
# <a name="multiple-threads-and-gdi-objects"></a><span data-ttu-id="608f0-103">Varios subprocesos y objetos GDI</span><span class="sxs-lookup"><span data-stu-id="608f0-103">Multiple Threads and GDI Objects</span></span>

<span data-ttu-id="608f0-104">Para mejorar el rendimiento, el acceso a los objetos de la interfaz de dispositivo gráfico (GDI) (como las paletas, los contextos de dispositivo, las regiones y el like) no se serializan.</span><span class="sxs-lookup"><span data-stu-id="608f0-104">To enhance performance, access to graphics device interface (GDI) objects (such as palettes, device contexts, regions, and the like) is not serialized.</span></span> <span data-ttu-id="608f0-105">Esto crea un riesgo potencial para los procesos que tienen varios subprocesos que comparten estos objetos.</span><span class="sxs-lookup"><span data-stu-id="608f0-105">This creates a potential danger for processes that have multiple threads sharing these objects.</span></span> <span data-ttu-id="608f0-106">Por ejemplo, si un subproceso elimina un objeto GDI mientras otro subproceso lo está usando, los resultados son imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="608f0-106">For example, if one thread deletes a GDI object while another thread is using it, the results are unpredictable.</span></span> <span data-ttu-id="608f0-107">Este peligro se puede evitar simplemente si no se comparten objetos GDI.</span><span class="sxs-lookup"><span data-stu-id="608f0-107">This danger can be avoided simply by not sharing GDI objects.</span></span> <span data-ttu-id="608f0-108">Si el uso compartido es inevitable (o deseable), la aplicación debe proporcionar sus propios mecanismos para sincronizar el acceso.</span><span class="sxs-lookup"><span data-stu-id="608f0-108">If sharing is unavoidable (or desirable), the application must provide its own mechanisms for synchronizing access.</span></span> <span data-ttu-id="608f0-109">Para obtener más información sobre cómo sincronizar el acceso, vea [sincronizar la ejecución de varios subprocesos](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="608f0-109">For more information about synchronizing access, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

 

 



