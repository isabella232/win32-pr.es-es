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
# <a name="pausing"></a>Pausando

Todos los cambios de estado del filtro deben mantener el bloqueo del filtro. En el método **PAUSE** , cree los recursos que necesite el filtro:


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



El método [**CBaseFilter::P ause**](cbasefilter-pause.md) establece el estado correcto en el filtro (estado \_ pausado) y llama al método [**CBasePin:: Active**](cbasepin-active.md) en cada pin conectado del filtro. El método **activo** informa al pin de que el filtro se ha vuelto activo. Si el PIN crea recursos, invalide el método **activo** de la manera siguiente:


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



