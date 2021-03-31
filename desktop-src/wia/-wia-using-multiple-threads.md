---
description: Cuando se usa una interfaz de adquisición de imágenes de Windows (WIA) en más de un subproceso dentro de un único proceso, una aplicación debe proporcionar la serialización de la interfaz.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Usar varios subprocesos en una aplicación WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154382"
---
# <a name="using-multiple-threads-in-a-wia-application"></a><span data-ttu-id="376e3-103">Usar varios subprocesos en una aplicación WIA</span><span class="sxs-lookup"><span data-stu-id="376e3-103">Using Multiple Threads in a WIA Application</span></span>

<span data-ttu-id="376e3-104">Cuando se usa una interfaz de adquisición de imágenes de Windows (WIA) en más de un subproceso dentro de un único proceso, una aplicación debe proporcionar la serialización de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="376e3-104">When using a Windows Image Acquisition (WIA) interface in more than one thread within a single process, an application must provide marshalling for that interface.</span></span> <span data-ttu-id="376e3-105">Si un subproceso crea un puntero de interfaz, no puede usar ese puntero en un subproceso diferente sin serialización.</span><span class="sxs-lookup"><span data-stu-id="376e3-105">If one thread creates an interface pointer, you cannot use that pointer in a different thread without marshalling.</span></span>

<span data-ttu-id="376e3-106">Por ejemplo, si un subproceso de una aplicación obtiene un puntero a la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) , un subproceso independiente no puede usar ese puntero de interfaz sin serialización.</span><span class="sxs-lookup"><span data-stu-id="376e3-106">For example, if one thread in an application obtains a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface, a separate thread cannot use that interface pointer without marshalling.</span></span>

<span data-ttu-id="376e3-107">Una técnica común que se usa para realizar esta serialización es usar la tabla de interfaz global.</span><span class="sxs-lookup"><span data-stu-id="376e3-107">A common technique used to accomplish this marshalling is to use the global interface table.</span></span> <span data-ttu-id="376e3-108">La tabla de interfaz global es una tabla que se mantiene en todos los subprocesos dentro de un único proceso.</span><span class="sxs-lookup"><span data-stu-id="376e3-108">The global interface table is a table maintained across all threads within a single process.</span></span> <span data-ttu-id="376e3-109">Todos los subprocesos que se ejecutan dentro del proceso pueden recuperar interfaces registradas en la tabla de interfaz global.</span><span class="sxs-lookup"><span data-stu-id="376e3-109">All threads running within the process can retrieve interfaces that are registered to the global interface table.</span></span> <span data-ttu-id="376e3-110">Esta técnica evita la necesidad de crear secuencias para pasar interfaces entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="376e3-110">This technique avoids the need to create streams for passing interfaces between threads.</span></span>

<span data-ttu-id="376e3-111">Para obtener información sobre cómo usar la tabla de interfaz global, vea [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="376e3-111">For information on how to use the global interface table, see [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="376e3-112">Incluso si no piensa usar varios subprocesos en una aplicación WIA, debe suponer que todas las funciones de devolución de llamada de eventos de dispositivo o de transferencia de datos se ejecutan en subprocesos independientes.</span><span class="sxs-lookup"><span data-stu-id="376e3-112">Even if you do not intend to use multiple threads in a WIA application, you must assume that all data transfer or device event callback functions run in separate threads.</span></span>

 

 
