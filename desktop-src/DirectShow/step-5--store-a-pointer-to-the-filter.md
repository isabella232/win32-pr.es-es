---
description: Paso 5.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Paso 5. Almacenar un puntero al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278287"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Paso 5. Almacenar un puntero al filtro

Invalide el método [**CBasePropertyPage:: alconnect**](cbasepropertypage-onconnect.md) para almacenar un puntero al filtro. En el ejemplo siguiente se consulta el parámetro *pUnk* de la interfaz ISaturation personalizada del filtro:


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



Siguiente: [paso 6. Inicialice el cuadro de diálogo](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



