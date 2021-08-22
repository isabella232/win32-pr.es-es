---
description: Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: async, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2597e0ed22fe9ccefa053891c0bd67ee76fae567847925de74faa1513de5faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049723"
---
# <a name="async-element"></a>async, elemento

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



## <a name="remarks"></a>Comentarios

Los valores posibles son 1 (operaciones asincrónicas incluidas) y 0 (valor predeterminado, operaciones asincrónicas excluidas).

Un proxy puede tener versiones asincrónicas y sincrónicas de las mismas operaciones.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




