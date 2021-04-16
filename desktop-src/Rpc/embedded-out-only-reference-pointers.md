---
title: Punteros de referencia de Out-Only insertados
description: Punteros de referencia de Out-Only insertados
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072e9aa3cc3f0f673e4bb737016bc035a3ac496
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676473"
---
# <a name="embedded-out-only-reference-pointers"></a>Punteros de referencia de Out-Only insertados

Cuando se usan \[ [](/windows/desktop/Midl/out-idl) \] punteros de referencia de solo salida en Microsoft RPC, el código auxiliar del servidor generado asigna solo el primer nivel de punteros accesible desde el puntero de referencia. Los punteros en niveles más profundos no se asignan mediante el código auxiliar, sino que deben asignarse mediante el nivel de aplicación de servidor. Por ejemplo, supongamos que una interfaz especifica una \[  \] matriz de punteros de referencia de solo salida:

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

En este ejemplo, el código auxiliar del servidor asigna memoria para 10 punteros y establece el valor de cada puntero en NULL. La aplicación de servidor debe asignar la memoria para los 10 enteros [**cortos**](/windows/desktop/Midl/short) a los que hacen referencia los punteros y, a continuación, establecer los 10 punteros para que apunten a los enteros.

Cuando la \[ [](/windows/desktop/Midl/out-idl) \] estructura de datos de solo salida incluye punteros de referencia anidados, el código auxiliar del servidor asigna solo el primer puntero accesible desde el puntero de referencia. Por ejemplo:

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

En el ejemplo anterior, el código auxiliar del servidor asigna el puntero *psTop* y **el \_ \_ tipo de struct** de estructura superior. El puntero de referencia *PS1* del **\_ \_ tipo Top de struct** se establece en NULL. El código auxiliar del servidor no asigna todos los niveles de la estructura de datos, ni asigna **el \_ tipo STRUCT1** ni su puntero incrustado, *psValue*.

 

 