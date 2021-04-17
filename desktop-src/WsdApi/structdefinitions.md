---
description: Genera definiciones de estructura de C para los tipos conocidos.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706555"
---
# <a name="structdefinitions-element"></a>elemento structDefinitions

Genera definiciones de estructura de C para los tipos conocidos.

## <a name="usage"></a>Uso

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

La mayoría del código generado y el código de aplicación hacen referencia a las estructuras de los tipos conocidos. Este elemento se usa para generar archivos de inclusión. Este elemento debe aparecer después de un elemento [**structDeclarations**](structdeclarations.md) para que las referencias entre estructuras se controlen correctamente.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




