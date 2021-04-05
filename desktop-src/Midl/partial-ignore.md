---
title: partial_ignore atributo)
description: El atributo ACF \ \_ Ignore parcial \ define una versión especializada de los punteros \ Unique \ que proporciona la semántica opcional.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore el atributo MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419673"
---
# <a name="partial_ignore-attribute"></a>\_omitir el atributo parcial

El atributo ACF **\[ \_ Ignore \] parcial** define una versión especializada de punteros **\[ únicos \]** que proporciona la semántica opcional de salida.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Observaciones

Al crear una función, es habitual permitir que los usuarios especifiquen un puntero no **nulo** a los datos devueltos opcionales, que a menudo se denominan punteros de salida opcionales. Normalmente no es necesario inicializar la memoria a la que apunta el usuario. Esta técnica representa un problema cuando la función se utiliza en RPC.

Si el puntero de salida opcional es válido, pero apunta a datos no inicializados, RPC intenta calcular las referencias de los datos y enviarlos al servidor, lo que puede provocar un error en el cálculo de referencias y anular la llamada. Incluso si el cálculo de referencias se realiza correctamente, se envía al servidor una cantidad potencialmente grande de datos inútiles.

Estos problemas se resuelven marcando el puntero como **\[ in, out, Unique y \_ parcial \] Ignore**. Los cuatro atributos deben estar presentes. Cuando se calculan las referencias de un puntero **\[ \_ \] parcial** en el lado del cliente, los únicos datos que se envían al servidor son un indicador que muestra si el puntero es **null**. Si el puntero no es **null**, la rutina del lado servidor recibe un puntero válido a un bloque de memoria que se ha inicializado con ceros. Si el puntero es **null**, la rutina del lado servidor recibe un puntero **nulo** .

En esta situación, el tamaño máximo del puntero debe estar bien definido en tiempo de compilación o en función de los parámetros de entrada, ya que el servidor debe asignar espacio para la ubicación de memoria a la que se apunta. Por ejemplo, un puntero de **\[ cadena \]** simple no tiene un tamaño bien definido porque la cadena termina implícitamente con un carácter nulo. En este caso, si **\[ \_ se \]** especifica el tamaño máximo de la cadena mediante la adición de un tamaño, el atributo lograría el requisito de tamaño bien definido.

## <a name="examples"></a>Ejemplos

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 




