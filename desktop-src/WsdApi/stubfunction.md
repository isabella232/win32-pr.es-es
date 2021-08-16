---
description: Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para operaciones un solo sentido y dos.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9304aa33bd193edc631949a93e1d770a1fade3d0c5726a9f2d897ea1862476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552431"
---
# <a name="stubfunction-element"></a>elemento stubFunction

Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para operaciones un solo sentido y dos.

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
| [**portTypeDefinitions**](porttypedefinitions.md)<br/> | Genera constantes de C para tipos de puerto.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Las referencias de función de código auxiliar se usan en escenarios de hospedaje para operaciones un solo sentido y dos.

Los valores válidos para este elemento son 1 (se incluyen referencias de función TRUE/stub) y 0 (se incluyen las referencias de función FALSE/no stub).

## <a name="element-information"></a>Información de elemento



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




