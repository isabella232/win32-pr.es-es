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
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885324"
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



 

## <a name="remarks"></a>Observaciones

Si **radio** se establece en true, todos los elementos **BUTTONELEMENT** de **BUTTONGROUP** serán permanentes, pero solo un botón a la vez estará en estado de inactividad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BUTTONELEMENT.sticky**](buttonelement-sticky.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





