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
ms.openlocfilehash: ec9c6a2cf1523cf2384142bd6ffd47cb5e42e7851dc96b6e236343c5ba670aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342751"
---
# <a name="buttonsticky"></a>BUTTON.sticky

El **atributo** permanente especifica o recupera un valor que indica si **BUTTON** es un botón de alternancia, es decir, si es un BUTTON de dos estados o de un solo **estado.**

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Valor | Descripción                        |
|-------|------------------------------------|
| true  | **BUTTON** es permanente.              |
| false | Predeterminada. **BUTTON** no es permanente. |



 

## <a name="remarks"></a>Comentarios

Si **sticky** se establece en true, **el botón** cambiará al estado down cuando se haga clic en él y permanecerá en ese estado hasta que se vuelva a hacer clic en él. Cuando **el botón** está en estado de bajada, el atributo **down** será true y se **mostrará downImage.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





