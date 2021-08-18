---
title: Punteros Out-Only referencia insertados
description: Punteros Out-Only referencia insertados
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36fc6229c0b155e3fa9a7f66e6cd1fbd742d7ec876264a8706ce81c4150d6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930534"
---
# <a name="embedded-out-only-reference-pointers"></a>Punteros Out-Only referencia insertados

Cuando se usan punteros de referencia out -only en RPC de Microsoft, los códigos auxiliares de servidor generados asignan solo el primer nivel de \[ [](/windows/desktop/Midl/out-idl) \] punteros accesibles desde el puntero de referencia. Los códigos auxiliares no asignan punteros en niveles más profundos, pero el nivel de aplicación de servidor debe asignar los punteros. Por ejemplo, suponga que una interfaz especifica una \[ **matriz out** \] -only de punteros de referencia:

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

En este ejemplo, el código auxiliar del servidor asigna memoria para 10 punteros y establece el valor de cada puntero en NULL. La aplicación de servidor debe asignar [](/windows/desktop/Midl/short) la memoria para los 10 enteros cortos a los que hacen referencia los punteros y, a continuación, establecer los 10 punteros para que apunten a los enteros.

Cuando la estructura de datos out -only incluye punteros de referencia anidados, los códigos auxiliares del servidor asignan solo el primer puntero accesible \[ [](/windows/desktop/Midl/out-idl) \] desde el puntero de referencia. Por ejemplo:

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

En el ejemplo anterior, los códigos auxiliares del servidor asignan el *puntero psTop* y la estructura **STRUCT \_ TOP \_ TYPE**. El puntero de *referencia ps1* en **STRUCT \_ TOP \_ TYPE** se establece en null. El código auxiliar del servidor no asigna todos los niveles de la estructura de datos, ni asigna el **tipo \_ STRUCT1** o su puntero incrustado, *psValue*.

 

 