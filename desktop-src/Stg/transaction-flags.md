---
title: Marcas de transacción
description: Un objeto se puede abrir en modo directo o de transacción.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268944"
---
# <a name="transaction-flags"></a><span data-ttu-id="2dddf-103">Marcas de transacción</span><span class="sxs-lookup"><span data-stu-id="2dddf-103">Transaction Flags</span></span>

<span data-ttu-id="2dddf-104">Un objeto se puede abrir en modo directo o de transacción.</span><span class="sxs-lookup"><span data-stu-id="2dddf-104">An object can be opened in either direct or transacted mode.</span></span> <span data-ttu-id="2dddf-105">Cuando un objeto se abre en modo directo, los cambios se realizan de forma inmediata y permanente.</span><span class="sxs-lookup"><span data-stu-id="2dddf-105">When an object is opened in direct mode, changes are made immediately and permanently.</span></span> <span data-ttu-id="2dddf-106">Cuando se abre un objeto en modo de transacción, los cambios se almacenan en búfer para que se puedan confirmar o revertir explícitamente una vez completada la edición.</span><span class="sxs-lookup"><span data-stu-id="2dddf-106">When an object is opened in transacted mode, changes are buffered so they can be explicitly committed or reverted once editing is complete.</span></span> <span data-ttu-id="2dddf-107">Los cambios confirmados se guardan en el objeto mientras se descartan los cambios revertidos.</span><span class="sxs-lookup"><span data-stu-id="2dddf-107">Committed changes are saved to the object while reverted changes are discarded.</span></span> <span data-ttu-id="2dddf-108">El modo directo es el modo de acceso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2dddf-108">Direct mode is the default access mode.</span></span>

<span data-ttu-id="2dddf-109">No es necesario el modo de transacción en un objeto de almacenamiento primario para poder usarlo en un elemento anidado.</span><span class="sxs-lookup"><span data-stu-id="2dddf-109">Transacted mode is not required on a parent storage object in order to use it on a nested element.</span></span> <span data-ttu-id="2dddf-110">Sin embargo, una transacción para un elemento anidado está anidada dentro de la transacción para su objeto de almacenamiento primario.</span><span class="sxs-lookup"><span data-stu-id="2dddf-110">A transaction for a nested element, however, is nested within the transaction for its parent storage object.</span></span> <span data-ttu-id="2dddf-111">Por lo tanto, los cambios realizados en un objeto secundario no se pueden confirmar hasta que se confirmen los que se realizan en el elemento primario y ambos permanecen sin confirmar hasta que el objeto de almacenamiento raíz (el primario de nivel superior) se escribe realmente en el disco.</span><span class="sxs-lookup"><span data-stu-id="2dddf-111">Therefore, changes made to a child object cannot be committed until those made to the parent are committed, and both remain uncommitted until the root storage object (the top-level parent) is actually written to disk.</span></span> <span data-ttu-id="2dddf-112">En otras palabras, los cambios se mueven hacia fuera: los objetos internos publican los cambios en las transacciones de sus contenedores inmediatos.</span><span class="sxs-lookup"><span data-stu-id="2dddf-112">In other words, the changes move outward: inner objects publish changes to the transactions of their immediate containers.</span></span>

 

 




