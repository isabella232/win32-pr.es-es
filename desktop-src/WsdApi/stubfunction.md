---
description: Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones un sentido y dos.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f37aed20dae4f04eea087e3d1eac2d23369af
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994152"
---
# <a name="stubfunction-element"></a>elemento stubFunction

Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones un sentido y dos.

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



## <a name="remarks"></a>Comentarios

Las referencias de función de código auxiliar se usan en escenarios de hospedaje para operaciones un solo sentido y dos.

Los valores válidos para este elemento son 1 (referencias de función TRUE/stub incluidas) y 0 (se incluyen referencias de función FALSE/no stub).

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




