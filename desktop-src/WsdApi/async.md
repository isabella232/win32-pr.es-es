---
description: Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: Async (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083249"
---
# <a name="async-element"></a>Async (elemento)

Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.

## <a name="usage"></a>Uso

``` syntax
<async/>
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



## <a name="remarks"></a>Observaciones

Los valores posibles son 1 (operaciones asincrónicas incluidas) y 0 (valor predeterminado, se excluyen las operaciones asincrónicas).

Un proxy puede tener tanto versiones asincrónicas como sincrónicas de las mismas operaciones.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




