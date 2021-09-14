---
description: Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: async, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6cbc68d0a5dea30f4b4d179a54539ac3f9516a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973707"
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



## <a name="remarks"></a>Observaciones

Los valores posibles son 1 (operaciones asincrónicas incluidas) y 0 (valor predeterminado, operaciones asincrónicas excluidas).

Un proxy puede tener versiones asincrónicas y sincrónicas de las mismas operaciones.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




