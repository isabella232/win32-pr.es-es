---
title: Portabilidad de funciones Get de GL de IRIS
description: 'IRIS GL \ 0034; Get \ 0034; las funciones tienen el formato siguiente:'
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Migración de la contabilidad de IRIS, funciones Get
- portabilidad de IRIS GL, funciones Get
- trasladar a OpenGL desde IRIS GL, obtener funciones
- Exportación de OpenGL desde IRIS GL, obtener funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665696"
---
# <a name="porting-iris-gl-get-functions"></a>Portabilidad de funciones Get de GL de IRIS

Las funciones de "obtener" de la contabilidad de IRIS tienen el formato siguiente:

``` syntax
int getthing();
```

y

``` syntax
int getthings( int *a, int *b);
```

Probablemente, el código de la contabilidad de IRIS incluye llamadas a funciones Get que tienen un aspecto similar al siguiente:

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

En OpenGL, se usa uno de los cuatro tipos siguientes de funciones de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) en lugar de funciones equivalentes Get GL de iris:

-   **glGetBooleanv**
-   **glGetIntegerv**
-   **glGetFloatv**
-   **glGetDoublev**

Las funciones tienen la siguiente sintaxis:

``` syntax
glGet<Datatype>v( value, *data );
```

donde *valor* es de tipo **GLenum** y los datos son de tipo **GLdatatype**. Cuando se llama a **glGet** y devuelve un tipo diferente del tipo esperado, el tipo se convierte adecuadamente. Para obtener una lista completa de los parámetros de **glGet** , consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 




