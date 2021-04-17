---
title: BOTÓN. permanente
description: El atributo de permanencia especifica o recupera un valor que indica si el botón es un botón de alternancia, es decir, si es un botón de dos Estados o de un solo Estado.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BOTÓN. Media Player de ventanas adhesivas
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698726"
---
# <a name="buttonsticky"></a>BOTÓN. permanente

El atributo de **permanencia** especifica o recupera un valor que indica si el **botón** es un botón de alternancia, es decir, si es un **botón** de dos Estados o de un solo Estado.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                        |
|-------|------------------------------------|
| true  | El **botón** es permanente.              |
| false | Predeterminada. El **botón** no es permanente. |



 

## <a name="remarks"></a>Observaciones

Si la **permanencia** está establecida en true, el **botón** cambiará al estado desactivado cuando se haga clic en él y permanecerá en ese estado hasta que se vuelva a hacer clic. Cuando el **botón** está en estado inactivo, el atributo **Down** será true y se mostrará el **downImage** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÓN. abajo**](button-down.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> </dl>

 

 





