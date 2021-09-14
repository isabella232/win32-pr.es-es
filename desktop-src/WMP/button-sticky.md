---
title: BUTTON.sticky
description: El atributo permanente especifica o recupera un valor que indica si BUTTON es un botón de alternancia, es decir, si es un BUTTON de dos estados o de un solo estado.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- Button.sticky Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889396"
---
# <a name="buttonsticky"></a>BUTTON.sticky

El **atributo** permanente especifica o recupera un valor que indica si **BUTTON** es un botón de alternancia, es decir, si es un BUTTON de dos estados o de un solo **estado.**

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Value | Descripción                        |
|-------|------------------------------------|
| true  | **BUTTON** es permanente.              |
| false | Predeterminada. **BUTTON** no es permanente. |



 

## <a name="remarks"></a>Observaciones

Si **sticky** se establece en true, **el botón** cambiará al estado down cuando se haga clic en él y permanecerá en ese estado hasta que se vuelva a hacer clic en él. Cuando **el botón** está en estado de bajada, el atributo **down** será true y se **mostrará downImage.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.down**](button-down.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> </dl>

 

 





