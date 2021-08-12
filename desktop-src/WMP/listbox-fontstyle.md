---
title: LISTBOX.fontStyle
description: El atributo fontStyle especifica o recupera el estilo de fuente para el control de cuadro de lista.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX.fontStyle Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258064ca4ee97fc33bb98bf64d8e3dcf305c5d7e045282a5218a060e904aff50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575042"
---
# <a name="listboxfontstyle"></a>LISTBOX.fontStyle

El **atributo fontStyle** especifica o recupera el estilo de fuente para el control de cuadro de lista.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene uno o varios de los valores siguientes.



| Valor     | Descripción           |
|-----------|-----------------------|
| Negrita      | Estilo de fuente en negrita.      |
| Cursiva    | Estilo de fuente cursiva.    |
| Subrayado | Estilo de fuente de subrayado. |
| Tachado | Estilo de fuente de tachón. |
| Normal    | Estilo de fuente normal.    |



 

## <a name="remarks"></a>Comentarios

Se puede usar cualquier combinación de los valores, separados por espacios. El estilo Normal tiene prioridad sobre todos los demás valores y se omitirán los demás especificados junto con Normal.

Con fines de representación, Normal es el estilo de fuente predeterminado. El valor predeterminado recuperado de este atributo es "" (cadena vacía).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**LISTBOX.fontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





