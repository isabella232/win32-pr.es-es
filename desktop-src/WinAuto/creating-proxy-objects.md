---
title: Crear objetos proxy
description: Además de diseñar clases que implementan métodos y propiedades de IAccessible, los desarrolladores de servidores también pueden necesitar diseñar objetos proxy que supervisen la duración de los objetos accesibles.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774089"
---
# <a name="creating-proxy-objects"></a><span data-ttu-id="274f2-103">Crear objetos proxy</span><span class="sxs-lookup"><span data-stu-id="274f2-103">Creating Proxy Objects</span></span>

<span data-ttu-id="274f2-104">Además de diseñar clases que implementan métodos y propiedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , los desarrolladores de servidores también pueden necesitar diseñar objetos *proxy* que supervisen la duración de los objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="274f2-104">In addition to designing classes that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods, server developers may also need to design *proxy* objects that monitor the life span of accessible objects.</span></span> <span data-ttu-id="274f2-105">Si un objeto accesible en una aplicación está disponible todo el tiempo que se ejecuta la aplicación, no es necesario crear un objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="274f2-105">If an accessible object in an application is available the entire time the application is running, then you do not need to create a proxy object.</span></span> <span data-ttu-id="274f2-106">Si es posible destruir el objeto accesible mientras la aplicación se está ejecutando, debe crear un objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="274f2-106">If it is possible to destroy the accessible object while the application is running, then you must create a proxy object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="274f2-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="274f2-107">In this section</span></span>

-   [<span data-ttu-id="274f2-108">¿Qué son los objetos proxy?</span><span class="sxs-lookup"><span data-stu-id="274f2-108">What Are Proxy Objects?</span></span>](what-are-proxy-objects.md)
-   [<span data-ttu-id="274f2-109">Por qué se necesitan objetos proxy</span><span class="sxs-lookup"><span data-stu-id="274f2-109">Why Proxy Objects Are Needed</span></span>](why-proxy-objects-are-needed.md)
-   [<span data-ttu-id="274f2-110">Consideraciones de diseño para objetos proxy</span><span class="sxs-lookup"><span data-stu-id="274f2-110">Design Considerations for Proxy Objects</span></span>](design-considerations-for-proxy-objects.md)

 

 




