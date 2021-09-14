---
title: Porting IRIS GL Get Functions
description: IRIS GL \ 0034;get \ 0034; Las funciones toman la forma siguiente
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Porte de IRIS GL, obtener funciones
- porting from IRIS GL,get functions
- porte a OpenGL desde IRIS GL, obtener funciones
- Porte de OpenGL desde IRIS GL, obtener funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074021"
---
# <a name="porting-iris-gl-get-functions"></a>Porting IRIS GL Get Functions

Las funciones "get" de IRIS GL toman la forma siguiente:

``` syntax
int getthing();
```

y

``` syntax
int getthings( int *a, int *b);
```

El código GL de IRIS probablemente incluya llamadas de función get que tienen un aspecto parecido al siguiente:

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

En OpenGL se usa uno de los cuatro tipos siguientes de [**funciones glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) en lugar de funciones get de IRIS GL equivalentes:

-   **glGetBooleanv**
-   **glGetIntegerv**
-   **glGetFloatv**
-   **glGetDoublev**

Las funciones tienen la sintaxis siguiente:

``` syntax
glGet<Datatype>v( value, *data );
```

donde *value* es de tipo **GLenum y** data es de tipo **GLdatatype.** Cuando se llama **a glGet** y devuelve un tipo diferente del tipo esperado, el tipo se convierte correctamente. Para obtener una lista completa de **los parámetros glGet,** [**vea glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 




