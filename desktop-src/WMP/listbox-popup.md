---
title: LISTBOX.popUp
description: El atributo popUp especifica un valor que indica si el elemento representa un control emergente o de cuadro de lista.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- ListBOX.popUp Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a755a4fc8f5e1451ee118f718a9b6618e75875789faef7318164f7f2add2069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996445"
---
# <a name="listboxpopup"></a>LISTBOX.popUp

El **atributo popUp** especifica un valor que indica si el elemento representa un control emergente o de cuadro de lista.

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** especificado solo en tiempo de diseño.



| Value | Descripción                                |
|-------|--------------------------------------------|
| true  | El elemento representa un control emergente.    |
| false | El elemento representa un control de cuadro de lista. |



 

## <a name="remarks"></a>Comentarios

El **elemento POPUP** representa un control de cuadro de lista que solo se muestra cuando es necesario. Es idéntico al elemento **LISTBOX,** excepto el valor predeterminado de este atributo, que cambia el comportamiento de presentación. Para **los elementos LISTBOX,** el valor predeterminado es false. Para **los elementos POPUP,** el valor predeterminado es true. En lugar de especificar este atributo, se debe usar **el elemento LISTBOX** o **POPUP** según el comportamiento deseado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**Elemento POPUP**](popup-element.md)
</dt> </dl>

 

 





