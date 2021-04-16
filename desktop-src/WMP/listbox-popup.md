---
title: LISTBOX. popUp
description: El atributo popUp especifica un valor que indica si el elemento representa un control popUp o de cuadro de lista.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX. popUp Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708843"
---
# <a name="listboxpopup"></a>LISTBOX. popUp

El atributo **popUp** especifica un valor que indica si el elemento representa un control popUp o de cuadro de lista.

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** especificado solo en tiempo de diseño.



| Value | Descripción                                |
|-------|--------------------------------------------|
| true  | El elemento representa un control Popup.    |
| false | El elemento representa un control de cuadro de lista. |



 

## <a name="remarks"></a>Observaciones

El elemento **popup** representa un control de cuadro de lista que se muestra solo cuando es necesario. Es idéntico al elemento **ListBox** excepto el valor predeterminado de este atributo, que cambia el comportamiento de presentación. En el caso de los elementos **ListBox** , el valor predeterminado es false. En el caso de los elementos **emergentes** , el valor predeterminado es true. En lugar de especificar este atributo, el **cuadro de lista** o elemento **emergente** debe usarse en función del comportamiento deseado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**Elemento POPUP**](popup-element.md)
</dt> </dl>

 

 





