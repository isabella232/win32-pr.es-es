---
title: EFFECTS.currentEffect
description: El atributo currentEffect especifica o recupera la visualización actual.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTS.currentEffect Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242535"
---
# <a name="effectscurrenteffect"></a>EFFECTS.currentEffect

El **atributo currentEffect** especifica o recupera la visualización actual.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un objeto de lectura y **escritura.** El valor predeterminado es la primera visualización en el orden de creación. Si no hay visualizaciones que se han escrito en la máscara, el valor predeterminado es la primera visualización del registro.

## <a name="remarks"></a>Observaciones

Puede usar este objeto para acceder a las visualizaciones personalizadas que ha creado. Por ejemplo, podría exponer una propiedad a través de la **interfaz IDispatch** en la visualización. A continuación, puede cambiar el valor de propiedad de la máscara haciendo que la visualización sea el efecto actual y, a continuación, usando el **objeto currentEffect** para establecer un nuevo valor para la propiedad. Por ejemplo, si la visualización expone una propiedad denominada backgroundColor, el siguiente código JScript especifica un nuevo valor:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTS, elemento**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





