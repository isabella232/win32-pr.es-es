---
description: Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277319"
---
# <a name="faultinfo-element"></a>elemento faultInfo

Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.

## <a name="usage"></a>Uso

``` syntax
<faultInfo/>
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
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>              |



## <a name="remarks"></a>Observaciones

Los valores posibles son 1 (parámetros de error incluidos) y 0 (parámetros de error excluidos). De forma predeterminada, se excluyen los parámetros de error.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




