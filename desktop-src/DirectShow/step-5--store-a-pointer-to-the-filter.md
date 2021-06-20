---
description: Almacene un puntero a un filtro como parte de la creación de una página de propiedades de filtro para un filtro directShow personalizado.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Paso 5. Almacenar un puntero al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406798"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Paso 5. Almacenar un puntero al filtro

Invalide [**el método CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) para almacenar un puntero al filtro. En el ejemplo siguiente se consulta *el parámetro pUnk* para la interfaz de ISaturation personalizada del filtro:


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



Siguiente: [Paso 6. Inicialice el cuadro de diálogo](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



