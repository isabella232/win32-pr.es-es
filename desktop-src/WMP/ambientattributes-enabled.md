---
title: AmbientAttributes.enabled
description: El atributo enabled especifica o recupera un valor que indica si el control está habilitado o deshabilitado.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbientAttributes.enabled Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d8e000d64ef92212cd7c6cf37c7fd79036107e1d3be0d7669d73b40c759de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055183"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes.enabled

El **atributo enabled** especifica o recupera un valor que indica si el control está habilitado o deshabilitado.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Valor | Descripción               |
|-------|---------------------------|
| true  | Predeterminada. Control habilitado. |
| false | Control deshabilitado.         |



 

## <a name="remarks"></a>Comentarios

Si el control está habilitado, puede tener una tabulación y recibirá todos los eventos de ambiente. Cuando está deshabilitado, el control no tiene un tabulador y no recibe ningún evento de mouse ambiente o teclado que se haya desencadenado en él. (Sin embargo, seguirá recibiendo todos los demás eventos de ambiente que se desencadenan en él).

Este atributo no se admite para el **elemento SUBVIEW.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





