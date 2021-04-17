---
title: attribute_onchange
description: Cuando un atributo de máscara cambia de valor, se produce un evento que se puede controlar mediante un controlador de eventos. El nombre del controlador de eventos es el nombre del atributo seguido por un carácter de subrayado y \ 0034; onchange \ 0034;, como \ 0034; valor \_ onchange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699976"
---
# <a name="attribute_onchange"></a>atributo \_ onchange

Cuando un atributo de máscara cambia de valor, se produce un evento que se puede controlar mediante un controlador de eventos. El nombre del controlador de eventos es el nombre del atributo seguido por un carácter de subrayado y "onchange", como "valor onchange \_ ".

``` syntax
        attribute_onchange
```

## <a name="examples"></a>Ejemplos


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controladores de eventos de ambiente**](ambient-event-handlers.md)
</dt> </dl>

 

 





