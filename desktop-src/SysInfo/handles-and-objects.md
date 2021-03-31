---
description: Un objeto es una estructura de datos que representa un recurso del sistema, como un archivo, un subproceso o una imagen gráfica.
ms.assetid: 26aaad09-c1e1-46e8-9cd3-7d795a10d900
title: Identificadores y objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b5a35d55571a01f2f186f4e756401582474949f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912785"
---
# <a name="handles-and-objects"></a><span data-ttu-id="8c3cd-103">Identificadores y objetos</span><span class="sxs-lookup"><span data-stu-id="8c3cd-103">Handles and Objects</span></span>

<span data-ttu-id="8c3cd-104">Un *objeto* es una estructura de datos que representa un recurso del sistema, como un archivo, un subproceso o una imagen gráfica.</span><span class="sxs-lookup"><span data-stu-id="8c3cd-104">An *object* is a data structure that represents a system resource, such as a file, thread, or graphic image.</span></span> <span data-ttu-id="8c3cd-105">Una aplicación no puede tener acceso directamente a los datos de objeto o al recurso del sistema que representa un objeto.</span><span class="sxs-lookup"><span data-stu-id="8c3cd-105">An application cannot directly access object data or the system resource that an object represents.</span></span> <span data-ttu-id="8c3cd-106">En su lugar, una aplicación debe obtener un *identificador* de objeto, que puede usar para examinar o modificar el recurso del sistema.</span><span class="sxs-lookup"><span data-stu-id="8c3cd-106">Instead, an application must obtain an object *handle*, which it can use to examine or modify the system resource.</span></span> <span data-ttu-id="8c3cd-107">Cada controlador tiene una entrada en una tabla mantenida internamente.</span><span class="sxs-lookup"><span data-stu-id="8c3cd-107">Each handle has an entry in an internally maintained table.</span></span> <span data-ttu-id="8c3cd-108">Estas entradas contienen las direcciones de los recursos y los medios para identificar el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="8c3cd-108">These entries contain the addresses of the resources and the means to identify the resource type.</span></span>

-   [<span data-ttu-id="8c3cd-109">Acerca de los identificadores y objetos</span><span class="sxs-lookup"><span data-stu-id="8c3cd-109">About Handles and Objects</span></span>](about-handles-and-objects.md)
-   [<span data-ttu-id="8c3cd-110">Categorías de objetos</span><span class="sxs-lookup"><span data-stu-id="8c3cd-110">Object Categories</span></span>](object-categories.md)
-   [<span data-ttu-id="8c3cd-111">Referencia de identificador y objeto</span><span class="sxs-lookup"><span data-stu-id="8c3cd-111">Handle and Object Reference</span></span>](handle-and-object-reference.md)

 

 



