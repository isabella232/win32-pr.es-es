---
title: Por qué se necesitan objetos proxy
description: Con objetos accesibles, cuando un cliente establece una función de enlace en contexto, la DLL en la que se implementa la función de enlace del cliente se carga en el espacio de direcciones del servidor.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357082"
---
# <a name="why-proxy-objects-are-needed"></a><span data-ttu-id="5ce85-103">Por qué se necesitan objetos proxy</span><span class="sxs-lookup"><span data-stu-id="5ce85-103">Why Proxy Objects Are Needed</span></span>

<span data-ttu-id="5ce85-104">Con objetos accesibles, cuando un cliente establece una [función de enlace en contexto](in-context-and-out-of-context-hook-functions.md), la dll en la que se implementa la función de enlace del cliente se carga en el espacio de direcciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="5ce85-104">With accessible objects, when a client sets an [in-context hook function](in-context-and-out-of-context-hook-functions.md), the DLL in which the client's hook function is implemented is loaded into the server's address space.</span></span> <span data-ttu-id="5ce85-105">En este caso, cuando el cliente llama a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) desde dentro de la función de enlace, el puntero de interfaz que se devuelve apunta directamente al código en el espacio de direcciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="5ce85-105">In this case, when the client calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) from within the hook function, the interface pointer that is returned points directly to code in the server's address space.</span></span> <span data-ttu-id="5ce85-106">Cuando el cliente llama a una propiedad de interfaz mediante este puntero, la biblioteca del modelo de objetos componentes (COM) no está implicada en la serialización o la desserialización, y no puede detectar si se destruye un objeto.</span><span class="sxs-lookup"><span data-stu-id="5ce85-106">When the client calls an interface property using this pointer, the Component Object Model (COM) library is not involved with marshaling or unmarshaling and cannot detect if an object is destroyed.</span></span> <span data-ttu-id="5ce85-107">Por lo tanto, el servidor debe detectar esta situación y devolver un código de error al cliente.</span><span class="sxs-lookup"><span data-stu-id="5ce85-107">Therefore, the server must detect this situation and return an error code to the client.</span></span>

 

 




