---
description: Pausando
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Pausando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07f6f610c3cfac9361e1db40c0fcd37b90645b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152500"
---
# <a name="pausing"></a><span data-ttu-id="67246-103">Pausando</span><span class="sxs-lookup"><span data-stu-id="67246-103">Pausing</span></span>

<span data-ttu-id="67246-104">Todos los cambios de estado del filtro deben mantener el bloqueo del filtro.</span><span class="sxs-lookup"><span data-stu-id="67246-104">All filter state changes must hold the filter lock.</span></span> <span data-ttu-id="67246-105">En el método **PAUSE** , cree los recursos que necesite el filtro:</span><span class="sxs-lookup"><span data-stu-id="67246-105">In the **Pause** method, create any resources the filter needs:</span></span>


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



<span data-ttu-id="67246-106">El método [**CBaseFilter::P ause**](cbasefilter-pause.md) establece el estado correcto en el filtro (estado \_ pausado) y llama al método [**CBasePin:: Active**](cbasepin-active.md) en cada pin conectado del filtro.</span><span class="sxs-lookup"><span data-stu-id="67246-106">The [**CBaseFilter::Pause**](cbasefilter-pause.md) method sets the correct state on the filter (State\_Paused) and calls the [**CBasePin::Active**](cbasepin-active.md) method on every connected pin in the filter.</span></span> <span data-ttu-id="67246-107">El método **activo** informa al pin de que el filtro se ha vuelto activo.</span><span class="sxs-lookup"><span data-stu-id="67246-107">The **Active** method informs the pin that the filter has become active.</span></span> <span data-ttu-id="67246-108">Si el PIN crea recursos, invalide el método **activo** de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="67246-108">If the pin creates resources, override the **Active** method, as follows:</span></span>


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



