---
title: Puntos de sincronización
description: Cuando se admiten conjuntos de propiedades en el mismo objeto que IStorage, es importante tener en cuenta los puntos de sincronización entre el almacenamiento base y el almacenamiento de propiedades.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780101"
---
# <a name="synchronization-points"></a><span data-ttu-id="e2a75-103">Puntos de sincronización</span><span class="sxs-lookup"><span data-stu-id="e2a75-103">Synchronization Points</span></span>

<span data-ttu-id="e2a75-104">Cuando se admiten conjuntos de propiedades en el mismo objeto que [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), es importante tener en cuenta los puntos de sincronización entre el almacenamiento base y el almacenamiento de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e2a75-104">When property sets are supported on the same object as [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), it is important to be aware of synchronization points between the base storage and the property storage.</span></span>

<span data-ttu-id="e2a75-105">El almacenamiento del conjunto de propiedades contiene el flujo del conjunto de propiedades en un búfer interno hasta que dicho búfer se confirma a través del método [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) .</span><span class="sxs-lookup"><span data-stu-id="e2a75-105">The property set storage holds the property set stream in an internal buffer until that buffer is committed through the [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) method.</span></span> <span data-ttu-id="e2a75-106">Esto es así si [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) se abrió en modo de transacción o en modo directo.</span><span class="sxs-lookup"><span data-stu-id="e2a75-106">This is true whether [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) was opened in transacted mode or in direct mode.</span></span>

 

 




