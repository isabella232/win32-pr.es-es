---
description: Paso 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Paso 8. Aplicar cambios de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678264"
---
# <a name="step-8-apply-property-changes"></a>Paso 8. Aplicar cambios de propiedad

Invalide el método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) para confirmar cualquier cambio de propiedad. En este ejemplo, la \_ variable m lNewVal se actualiza cada vez que el usuario se desplaza por la barra deslizante. El método **OnApplyChanges** copia este valor en la \_ variable lVal de m, sobrescribiendo el valor original:


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Siguiente: [paso 9. Desconecte la página de propiedades](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



