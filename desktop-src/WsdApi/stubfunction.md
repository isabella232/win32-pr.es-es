---
description: Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones unidireccionales y bidireccionales.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7282e7280c8d701710094b70b84a65756f7230ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278409"
---
# <a name="stubfunction-element"></a>elemento stubFunction

Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones unidireccionales y bidireccionales.

## <a name="usage"></a>Uso

``` syntax
<stubFunction/>
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

Las referencias de funciones de código auxiliar se usan en escenarios de hospedaje para las operaciones unidireccionales y bidireccionales.

Los valores válidos para este elemento son 1 (se incluyen las referencias de funciones TRUE/stub) y 0 (FALSE/no se incluyen las referencias de funciones de código auxiliar).

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




