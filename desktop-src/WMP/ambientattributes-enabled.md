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
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889980"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes.enabled

El **atributo enabled** especifica o recupera un valor que indica si el control está habilitado o deshabilitado.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Value | Descripción               |
|-------|---------------------------|
| true  | Predeterminada. Control habilitado. |
| false | Control deshabilitado.         |



 

## <a name="remarks"></a>Observaciones

Si el control está habilitado, puede tener una tabulación de detenerse y recibirá todos los eventos ambientales. Cuando se deshabilita, el control no tiene una tabulación de detenerse y no recibe ningún evento ambiente del mouse o del teclado que se haya desencadenado en él. (Sin embargo, seguirá recibiendo todos los demás eventos de ambiente que se desencadenan en él).

Este atributo no se admite para el **elemento SUBVIEW.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





