---
description: Pausando
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Pausando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f113bdaa41709055202886112d678c2a1fbb172d99e880ceaafc997817412a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997285"
---
# <a name="pausing"></a>Pausando

Todos los cambios de estado de filtro deben contener el bloqueo del filtro. En el **método Pause,** cree los recursos que necesite el filtro:


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



El [**método CBaseFilter::P ause**](cbasefilter-pause.md) establece el estado correcto en el filtro (Estado en pausa) y llama al método \_ [**CBasePin::Active**](cbasepin-active.md) en cada pin conectado del filtro. El **método Active** informa al pin de que el filtro se ha activado. Si el pin crea recursos, invalide **el método Active,** como se muestra a continuación:


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



