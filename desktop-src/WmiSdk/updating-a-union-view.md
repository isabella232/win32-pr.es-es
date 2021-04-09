---
description: Puede actualizar los valores de las propiedades sin clave de las instancias de clase de vista de Unión. Los cambios que realice en la instancia de la clase de vista se propagarán de nuevo a las instancias de la clase de origen que forman la clase de vista Union.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Actualizar una vista de Unión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155805"
---
# <a name="updating-a-union-view"></a><span data-ttu-id="21b6f-104">Actualizar una vista de Unión</span><span class="sxs-lookup"><span data-stu-id="21b6f-104">Updating a Union View</span></span>

<span data-ttu-id="21b6f-105">Puede actualizar los valores de las propiedades sin clave de las instancias de clase de vista de Unión.</span><span class="sxs-lookup"><span data-stu-id="21b6f-105">You can update the values of nonkey properties of union view class instances.</span></span> <span data-ttu-id="21b6f-106">Los cambios que realice en la instancia de la clase de vista se propagarán de nuevo a las instancias de la clase de origen que forman la clase de vista Union.</span><span class="sxs-lookup"><span data-stu-id="21b6f-106">The changes you make to the view class instance will be propagated back to the source class instances that form the union view class.</span></span>

<span data-ttu-id="21b6f-107">Las siguientes restricciones se aplican a los cambios en las instancias de la clase de vista:</span><span class="sxs-lookup"><span data-stu-id="21b6f-107">The following restrictions apply to changes to view class instances:</span></span>

-   <span data-ttu-id="21b6f-108">No se pueden crear nuevas instancias de clases de vista.</span><span class="sxs-lookup"><span data-stu-id="21b6f-108">You cannot create new instances of view classes.</span></span>
-   <span data-ttu-id="21b6f-109">Solo las clases Union admiten actualizaciones; las vistas de combinación y de asociación crean instancias de vista de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="21b6f-109">Only union classes support updates; join and association views create read-only view instances.</span></span>
-   <span data-ttu-id="21b6f-110">El éxito de una actualización depende de si una instancia de origen es actualizable.</span><span class="sxs-lookup"><span data-stu-id="21b6f-110">Success of an update depends on whether a source instance is updateable.</span></span> <span data-ttu-id="21b6f-111">Si una propiedad de instancia de vista se asigna a una propiedad de solo lectura de una instancia de origen, se producirá un error al intentar modificar la propiedad de vista.</span><span class="sxs-lookup"><span data-stu-id="21b6f-111">If a view instance property maps to a read-only property of a source instance, attempts to modify the view property fail.</span></span>

 

 



