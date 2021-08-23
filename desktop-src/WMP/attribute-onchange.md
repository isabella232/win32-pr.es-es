---
title: attribute_onchange
description: Cuando un atributo de máscara cambia de valor, se produce un evento que un controlador de eventos puede controlar. El nombre del controlador de eventos es el nombre del atributo seguido de un carácter de subrayado y \ 0034;onchange \ 0034;, como \ 0034;value \_ onchange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Reproductor de Windows Media
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c707b04587b6e975f81c8a0d0918b14c8e193d303f82c61b5220796bb6975b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573765"
---
# <a name="attribute_onchange"></a>attribute \_ onchange

Cuando un atributo de máscara cambia de valor, se produce un evento que un controlador de eventos puede controlar. El nombre del controlador de eventos es el nombre del atributo seguido de un carácter de subrayado y "onchange", como "value \_ onchange".

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
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controladores de eventos ambiente**](ambient-event-handlers.md)
</dt> </dl>

 

 





