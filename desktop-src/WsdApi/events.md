---
description: Especifica si los eventos relacionados se incluyen en las funciones generadas.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea6d4d3c87ac15ee14864f7e12c419f13d97503eeab27d28c5bdec5dbcc1414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049693"
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



## <a name="remarks"></a>Comentarios

Los valores posibles son 1 (eventos incluidos) y 0 (valor predeterminado, eventos excluidos).

## <a name="element-information"></a>Información de elemento



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




