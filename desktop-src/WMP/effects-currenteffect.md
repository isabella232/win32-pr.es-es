---
title: EFFECTs. currentEffect
description: El atributo currentEffect especifica o recupera la visualización actual.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTs. currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699379"
---
# <a name="effectscurrenteffect"></a>EFFECTs. currentEffect

El atributo **currentEffect** especifica o recupera la visualización actual.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **objeto** de lectura/escritura. El valor predeterminado es la primera visualización del orden de creación. Si no se crean visualizaciones en la máscara, el valor predeterminado es la primera visualización del registro.

## <a name="remarks"></a>Observaciones

Puede usar este objeto para tener acceso a las visualizaciones personalizadas que ha creado. Por ejemplo, puede exponer una propiedad a través de la interfaz **IDispatch** en la visualización. Después, puede cambiar el valor de la propiedad de la máscara haciendo que la visualización sea el efecto actual y usando el objeto **currentEffect** para establecer un nuevo valor para la propiedad. Por ejemplo, si la visualización expone una propiedad denominada backgroundColor, el código JScript siguiente especifica un nuevo valor:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTs, elemento**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTs. currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





