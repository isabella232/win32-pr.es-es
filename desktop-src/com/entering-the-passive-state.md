---
title: Entrar en el estado pasivo
description: Entrar en el estado pasivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903792"
---
# <a name="entering-the-passive-state"></a><span data-ttu-id="8136e-103">Entrar en el estado pasivo</span><span class="sxs-lookup"><span data-stu-id="8136e-103">Entering the Passive State</span></span>

<span data-ttu-id="8136e-104">El cierre de objetos fuerza un objeto incrustado o vinculado en el estado pasivo.</span><span class="sxs-lookup"><span data-stu-id="8136e-104">Object closure forces an embedded or linked object into the passive state.</span></span> <span data-ttu-id="8136e-105">Normalmente se inicia desde la interfaz de usuario de la aplicación de servidor OLE, como cuando el usuario selecciona el comando de cierre de archivo.</span><span class="sxs-lookup"><span data-stu-id="8136e-105">It is typically initiated from the OLE server application's user interface, such as when the user selects the File Close command.</span></span> <span data-ttu-id="8136e-106">En este caso, la aplicación de servidor OLE notifica al contenedor, que libera su recuento de referencias en el objeto.</span><span class="sxs-lookup"><span data-stu-id="8136e-106">In this case, the OLE server application notifies the container, which releases its reference count on the object.</span></span> <span data-ttu-id="8136e-107">Cuando se han liberado todas las referencias al objeto, se puede liberar el objeto.</span><span class="sxs-lookup"><span data-stu-id="8136e-107">When all references to the object have been released, the object can be freed.</span></span> <span data-ttu-id="8136e-108">Cuando se han liberado todos los objetos, la aplicación de servidor OLE puede terminar de forma segura.</span><span class="sxs-lookup"><span data-stu-id="8136e-108">When all objects have been freed, the OLE server application can safely terminate.</span></span>

<span data-ttu-id="8136e-109">Una aplicación contenedora también puede iniciar el cierre de objetos.</span><span class="sxs-lookup"><span data-stu-id="8136e-109">A container application can also initiate object closure.</span></span> <span data-ttu-id="8136e-110">Para cerrar un objeto, el contenedor libera su recuento de referencias después de completar una operación de guardar opcional.</span><span class="sxs-lookup"><span data-stu-id="8136e-110">To close an object, the container releases its reference count after completing an optional save operation.</span></span> <span data-ttu-id="8136e-111">Puede diseñar contenedores para liberar objetos cuando se desactivan después de una sesión de activación en contexto, lo que permite al usuario hacer clic fuera del objeto sin perder la sesión de edición activa.</span><span class="sxs-lookup"><span data-stu-id="8136e-111">You can design containers to release objects when they are deactivating after an in-place activation session, allowing the user to click outside the object without losing the active editing session.</span></span>

 

 




