---
title: AmbientAttributes. Enabled
description: El atributo Enabled especifica o recupera un valor que indica si el control está habilitado o deshabilitado.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbientAttributes. Enabled Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698636"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes. Enabled

El atributo **Enabled** especifica o recupera un valor que indica si el control está habilitado o deshabilitado.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción               |
|-------|---------------------------|
| true  | Predeterminada. Control habilitado. |
| false | Control deshabilitado.         |



 

## <a name="remarks"></a>Observaciones

Si el control está habilitado, puede tener una tabulación y recibirá todos los eventos de ambiente. Cuando está deshabilitado, el control no tiene una tabulación y no recibe ningún evento de mouse o teclado ambiente que se desencadene. (Sin embargo, seguirá recibiendo todos los demás eventos de ambiente que se le hayan desencadenado).

Este atributo no se admite para el elemento de la **subvista** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





