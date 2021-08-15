---
title: partial_ignore atributo
description: El atributo ACF \ partial ignore\ define una versión especializada de \unique\ punteros que proporciona semántica \_ de salida opcional.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore atributo MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac751e5b3bdb4a93c003e170333af8956048c9793630419fff0857d61f8c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641978"
---
# <a name="partial_ignore-attribute"></a>atributo \_ partial ignore

El atributo ACF **\[ partial \_ ignore \]** define una **\[ \]** versión especializada de punteros únicos que proporciona semántica opcional.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Comentarios

Al crear una función, es habitual permitir a los usuarios especificar un puntero que no sea **NULL** para los datos devueltos opcionales, a menudo denominados punteros opcionales. La memoria a la que apunta el usuario no suele ser necesaria para inicializarse. Esta técnica representa un problema cuando la función se usa sobre RPC.

Si el puntero opcional de salida es válido, pero apunta a datos sin inicializar, RPC intenta serializar los datos y enviarlos al servidor, lo que puede provocar un error en la serialización y anular la llamada. Incluso si la serialización se realiza correctamente, se envía al servidor una cantidad potencialmente grande de datos inutilizados.

Estos problemas se resuelven marcando el puntero como **\[ in, out, unique, partial \_ ignore \]**. Los cuatro atributos deben estar presentes. Cuando se **\[ serializa \_ un \]** puntero de ignore parcial en el lado cliente, los únicos datos enviados al servidor son un indicador que muestra si el puntero es **NULL.** Si el puntero no es **NULL,** la rutina del lado servidor recibe un puntero válido a un bloque de memoria que se ha inicializado con ceros. Si el puntero es **NULL,** la rutina del lado servidor recibe un **puntero** NULL.

En esta situación, el tamaño máximo del puntero debe definirse correctamente en tiempo de compilación o en función de los parámetros de entrada, ya que el servidor debe asignar espacio para la ubicación de memoria a la que se apunta. Por ejemplo, un puntero **\[ de cadena \]** simple no tiene un tamaño bien definido porque la cadena termina implícitamente con un carácter NULL. En este caso, si se especifica el tamaño máximo de la cadena mediante la adición de un atributo **\[ size \_ \] is,** se lograría el requisito de tamaño bien definido.

## <a name="examples"></a>Ejemplos

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 




