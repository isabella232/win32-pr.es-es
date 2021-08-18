---
title: EFFECTS.currentEffect
description: El atributo currentEffect especifica o recupera la visualización actual.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- Effects.currentEffect Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9ac47ef88d1a0bce4982f71ce2e20e33f48933c9916bbb1e62085b5a1e5178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996875"
---
# <a name="effectscurrenteffect"></a>EFFECTS.currentEffect

El **atributo currentEffect** especifica o recupera la visualización actual.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un objeto de lectura **y escritura.** El valor predeterminado es la primera visualización en el orden de creación. Si no hay visualizaciones que se han escrito en la máscara, el valor predeterminado es la primera visualización en el registro.

## <a name="remarks"></a>Comentarios

Puede usar este objeto para acceder a las visualizaciones personalizadas que ha creado. Por ejemplo, podría exponer una propiedad a través de la **interfaz IDispatch** en la visualización. A continuación, puede cambiar el valor de propiedad de la máscara haciendo que la visualización sea el efecto actual y, a continuación, usando el **objeto currentEffect** para establecer un nuevo valor para la propiedad. Por ejemplo, si la visualización expone una propiedad denominada backgroundColor, el código JScript siguiente especifica un nuevo valor:


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

[**ELEMENTO EFFECTS**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





