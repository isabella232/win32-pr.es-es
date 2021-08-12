---
description: Paso 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Paso 8. Aplicar cambios de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2292d9f294711129b2edba50ef6fb623d767dfba4122295222d08eb1ad21dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652061"
---
# <a name="step-8-apply-property-changes"></a>Paso 8. Aplicar cambios de propiedad

Invalide [**el método CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) para confirmar los cambios de propiedad. En este ejemplo, la variable m \_ lNewVal se actualiza cada vez que el usuario desplaza la barra deslizante. El **método OnApplyChanges** copia este valor en la \_ variable m lVal y sobrescribe el valor original:


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Siguiente: [Paso 9. Desconecte la página de propiedades](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



