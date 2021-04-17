---
title: BUTTONGROUP. radio
description: El atributo de radio especifica o recupera un valor que indica si BUTTONGROUP se compone de botones de radio.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP. radio Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699946"
---
# <a name="buttongroupradio"></a>BUTTONGROUP. radio

El atributo de **radio** especifica o recupera un valor que indica si **BUTTONGROUP** se compone de botones de radio.

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                      |
|-------|--------------------------------------------------|
| true  | **BUTTONGROUP** es el estilo de radio.              |
| false | Predeterminada. **BUTTONGROUP** no es el estilo de radio. |



 

## <a name="remarks"></a>Observaciones

Si el valor de **radio** está establecido en true, todos los elementos **BUTTONELEMENT** del **BUTTONGROUP** serán persistentes, pero solo un botón a la vez estará en estado desactivado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BUTTONELEMENT. adhesiva**](buttonelement-sticky.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





