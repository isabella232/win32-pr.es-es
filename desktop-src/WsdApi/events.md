---
description: Especifica si los eventos relacionados se incluyen en las funciones generadas.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973691"
---
# <a name="events-element"></a>elemento events

Especifica si los eventos relacionados se incluyen en las funciones generadas.

## <a name="usage"></a>Uso

``` syntax
<events/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                         | Descripción                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                 | Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/> |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>           | Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>            |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/> | Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                         | Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>                 |
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>              |



## <a name="remarks"></a>Observaciones

Los valores posibles son 1 (eventos incluidos) y 0 (valor predeterminado, eventos excluidos).

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




