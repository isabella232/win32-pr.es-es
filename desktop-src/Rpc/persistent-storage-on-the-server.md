---
title: Almacenamiento persistente en el servidor
description: Puede optimizar la aplicación para que el código auxiliar del servidor no libere memoria en el servidor en el momento de la finalización de una llamada a procedimiento remoto.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994409"
---
# <a name="persistent-storage-on-the-server"></a><span data-ttu-id="757ec-103">Almacenamiento persistente en el servidor</span><span class="sxs-lookup"><span data-stu-id="757ec-103">Persistent Storage on the Server</span></span>

<span data-ttu-id="757ec-104">Puede optimizar la aplicación para que el código auxiliar del servidor no libere memoria en el servidor en el momento de la finalización de una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="757ec-104">You can optimize your application so the server stub does not free memory on the server at the conclusion of a remote procedure call.</span></span> <span data-ttu-id="757ec-105">Por ejemplo, cuando un identificador de contexto se manipulará mediante varios procedimientos remotos, puede usar el atributo ACF **\[ allocate (no \_ disponible) \]** para conservar la memoria asignada en el servidor.</span><span class="sxs-lookup"><span data-stu-id="757ec-105">For example, when a context handle will be manipulated by several remote procedures, you can use the ACF attribute **\[allocate(dont\_free)\]** to retain the allocated memory on the server.</span></span>

<span data-ttu-id="757ec-106">El atributo **\[ allocate (no \_ Free) \]** se agrega a la declaración de **definición** de tipo ACF en ACF.</span><span class="sxs-lookup"><span data-stu-id="757ec-106">The **\[allocate(dont\_free)\]** attribute is added to the ACF **typedef** declaration in the ACF.</span></span> <span data-ttu-id="757ec-107">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="757ec-107">For example:</span></span>

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

<span data-ttu-id="757ec-108">Cuando se especifica el atributo **\[ allocate (no \_ Free) \]** , el código auxiliar de servidor asigna la estructura de datos de árbol, pero no la libera.</span><span class="sxs-lookup"><span data-stu-id="757ec-108">When the **\[allocate(dont\_free)\]** attribute is specified, the tree data structure is allocated, but not freed, by the server stub.</span></span> <span data-ttu-id="757ec-109">Al hacer que los punteros a estas áreas de datos persistentes estén disponibles para otras rutinas, por ejemplo, copiando los punteros a variables globales, los datos retenidos son accesibles para otras funciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="757ec-109">When you make the pointers to such persistent data areas available to other routines—for example, by copying the pointers to global variables—the retained data is accessible to other server functions.</span></span> <span data-ttu-id="757ec-110">El atributo **\[ allocate (no \_ gratuito) \]** es especialmente útil para mantener estructuras de puntero persistentes como parte de la información de estado del servidor asociada a un tipo de identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="757ec-110">The **\[allocate(dont\_free)\]** attribute is particularly useful for maintaining persistent pointer structures as part of the server state information associated with a context-handle type.</span></span>

 

 




