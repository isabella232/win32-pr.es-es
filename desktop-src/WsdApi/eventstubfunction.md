---
description: Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: elemento eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe353f43d02eec68f29f3075cc445c1314c9762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697305"
---
# <a name="eventstubfunction-element"></a>elemento eventStubFunction

Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.

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



## <a name="remarks"></a>Observaciones

Las referencias de funciones de código auxiliar se encuentran en escenarios de cliente para las operaciones de notificación (eventos).

Los valores válidos para este elemento son 1 (se incluyen las referencias de funciones TRUE/stub) y 0 (FALSE/no se incluyen las referencias de funciones de código auxiliar).

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




