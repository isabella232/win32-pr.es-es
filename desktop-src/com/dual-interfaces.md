---
title: Interfaces duales (COM)
description: Interfaces duales
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078480"
---
# <a name="dual-interfaces"></a><span data-ttu-id="648bf-103">Interfaces duales</span><span class="sxs-lookup"><span data-stu-id="648bf-103">Dual Interfaces</span></span>

<span data-ttu-id="648bf-104">OLE Automation permite que un objeto exponga un conjunto de métodos de dos maneras: a través de la interfaz **IDispatch** y a través del enlace vtable OLE directo.</span><span class="sxs-lookup"><span data-stu-id="648bf-104">OLE Automation enables an object to expose a set of methods in two ways: via the **IDispatch** interface, and through direct OLE VTable binding.</span></span> <span data-ttu-id="648bf-105">La mayoría de las herramientas disponibles en la actualidad usan **IDispatch** y ofrece compatibilidad para el enlace en tiempo de ejecución a propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="648bf-105">**IDispatch** is used by most tools available today, and offers support for late binding to properties and methods.</span></span>

<span data-ttu-id="648bf-106">El enlace VTable ofrece un rendimiento mucho mayor porque se llama directamente a este método en lugar de a través de **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="648bf-106">VTable binding offers much higher performance because this method is called directly instead of through **IDispatch::Invoke**.</span></span> <span data-ttu-id="648bf-107">**IDispatch** ofrece compatibilidad con enlace en tiempo de ejecución, donde el enlace vtable directo ofrece un aumento significativo del rendimiento. ambas técnicas son valiosas e importantes en diferentes escenarios.</span><span class="sxs-lookup"><span data-stu-id="648bf-107">**IDispatch** offers late bound support, where direct VTable binding offers a significant performance gain; both techniques are valuable and important in different scenarios.</span></span> <span data-ttu-id="648bf-108">Al etiquetar una interfaz como \[ [**dual**](/windows/desktop/Midl/dual) \] en la biblioteca de tipos, se puede utilizar una interfaz de automatización OLE mediante **IDispatch**, o bien se puede enlazar directamente.</span><span class="sxs-lookup"><span data-stu-id="648bf-108">By labeling an interface as \[[**dual**](/windows/desktop/Midl/dual)\] in the type library, an OLE Automation interface can be used either via **IDispatch**, or it can be bound to directly.</span></span> <span data-ttu-id="648bf-109">Por lo tanto, los contenedores pueden elegir la técnica más adecuada.</span><span class="sxs-lookup"><span data-stu-id="648bf-109">Containers can thus choose the most appropriate technique.</span></span> <span data-ttu-id="648bf-110">Se recomienda encarecidamente la compatibilidad con interfaces duales para controles y contenedores.</span><span class="sxs-lookup"><span data-stu-id="648bf-110">Support for dual interfaces is strongly recommended for both controls and containers.</span></span>

 

 