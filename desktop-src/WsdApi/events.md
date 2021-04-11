---
description: Especifica si los eventos relacionados se incluyen en las funciones generadas.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276239"
---
# <a name="events-element"></a>elemento Events

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

Los valores posibles son 1 (eventos incluidos) y 0 (predeterminado, eventos excluidos).

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




