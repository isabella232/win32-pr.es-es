---
description: Almacene un puntero a un filtro como parte de la creación de una página de propiedades de filtro para un filtro DirectShow personalizado.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Paso 5. Almacenar un puntero al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63becf4cb98f401a4810f0f9a2604ef65387a58d08d84b9f670c09b51fe9acd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078775"
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

 

 



