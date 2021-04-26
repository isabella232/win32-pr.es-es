---
description: Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: Elemento eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80777a53d37e7651559a09b8e8445d4314aaca63
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995892"
---
# <a name="eventstubfunction-element"></a>Elemento eventStubFunction

Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.

## <a name="usage"></a>Uso

``` syntax
<eventStubFunction/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                       | Descripción                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [**portTypeDefinitions**](porttypedefinitions.md)<br/> | Genera constantes de C para los tipos de puerto.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Las referencias de función de código auxiliar se encuentran en escenarios de cliente para operaciones de notificación (eventos).

Los valores válidos para este elemento son 1 (referencias de función TRUE/stub incluidas) y 0 (se incluyen referencias de función FALSE/no stub).

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




