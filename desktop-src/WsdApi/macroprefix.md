---
description: Define el prefijo que se va a usar en el código generado para los nombres de macros en el espacio de nombres .
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroPrefix, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 970232b86aa226f16fa06cf2d3c9de40c156702c802c6f6254e45157e1df58ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130717"
---
# <a name="macroprefix-element"></a>macroPrefix, elemento

Define el prefijo que se va a usar en el código generado para los nombres de macros en el espacio de nombres .

## <a name="usage"></a>Uso

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                   | Descripción                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**Nombres**](namespace.md)<br/> | Espacio de nombres que se usará para la generación de código.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Este elemento invalida el prefijo URI predeterminado utilizado para las macros generadas. Por ejemplo, si el prefijo de macro es "AV" y el nombre es "Tuner", la macro generada para el nombre completo \_ será "AV \_ Tuner".

De forma predeterminada, el código generado crea un prefijo de macro preferido a partir del URI.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




