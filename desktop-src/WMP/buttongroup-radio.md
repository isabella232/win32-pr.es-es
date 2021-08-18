---
title: BUTTONGROUP.radio
description: El atributo de radio especifica o recupera un valor que indica si BUTTONGROUP se compone de botones de radio.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- ButtonGROUP.radio Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a8a9f85a3dce5ef070519f436c28ec157f7aa467a9115bcd8e2ccefa6444f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997775"
---
# <a name="buttongroupradio"></a>BUTTONGROUP.radio

El **atributo de** radio especifica o recupera un valor que indica si **BUTTONGROUP** se compone de botones de radio.

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                                      |
|-------|--------------------------------------------------|
| true  | **BUTTONGROUP es** un estilo de radio.              |
| false | Predeterminada. **BUTTONGROUP no** es un estilo de radio. |



 

## <a name="remarks"></a>Comentarios

Si **radio** se establece en true, todos los elementos **BUTTONELEMENT** de **BUTTONGROUP** serán permanentes, pero solo un botón a la vez estará en estado de inactividad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BUTTONELEMENT.sticky**](buttonelement-sticky.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





