---
title: Atributos de longitud, tamaño y direccional
description: Al pasar matrices entre el cliente y el servidor, los atributos relacionados con el tamaño \ max is\ y \ size is\ determinan cuántos elementos de matriz asigna el \_ \_ código auxiliar del servidor.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e91424a93a53fe710c945011d19f8f97dc0f65e4899bc3305be5725d5a08e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020136"
---
# <a name="length-size-and-directional-attributes"></a>Atributos de longitud, tamaño y direccional

Al pasar matrices entre el cliente y el servidor, el tamaño máximo de los atributos relacionados con el tamaño es y el tamaño determina cuántos elementos de matriz asigna el código auxiliar \[ [**\_**](/windows/desktop/Midl/max-is) \] del \[ [**\_**](/windows/desktop/Midl/size-is) \] servidor. La longitud de los atributos relacionados con la longitud es , la primera es y la última es determinar cuántos elementos se transmiten al \[ [**\_**](/windows/desktop/Midl/length-is)servidor \] y al \[ [**\_**](/windows/desktop/Midl/first-is) \] \[ [**\_**](/windows/desktop/Midl/last-is) \] cliente.

Se pueden aplicar atributos direccionales diferentes a los parámetros. Sin embargo, algunas combinaciones de atributos direccionales pueden provocar errores. Por ejemplo, supongamos que está escribiendo una interfaz que especifica un procedimiento con dos parámetros, una matriz y la longitud transmitida de la matriz. El término *dir \_ attr* hace referencia al atributo direccional aplicado al parámetro como:

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

El comportamiento del compilador MIDL para cada combinación de atributos direccionales se describe en la tabla siguiente.



| Array                                          | Parámetro Length                               | Acciones de código auxiliar durante la llamada del cliente al servidor                                                                                                                                                                                                                          | Acciones de código auxiliar en la devolución del servidor al cliente                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**En**](/windows/desktop/Midl/in)\]                          | \[[**En**](/windows/desktop/Midl/in)\]                          | Transmita la longitud y el número de elementos indicados por el parámetro .                                                                                                                                                                                              | No se transmiten datos.                                                                                                                                                                                                 |
| \[[**En**](/windows/desktop/Midl/in)\]                          | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | No es legal; Error del compilador MIDL.                                                                                                                                                                                                                                         | No es legal; Error del compilador MIDL.                                                                                                                                                                                      |
| \[[**En**](/windows/desktop/Midl/in)\]                          | \[[**en**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita la longitud y el número de elementos indicados por el parámetro length.                                                                                                                                                                                       | Transmita solo la longitud.                                                                                                                                                                                            |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**En**](/windows/desktop/Midl/in)\]                          | Transmita la longitud.<br/> Si el tamaño de la matriz es fijo, asigne el tamaño de la matriz en el servidor, pero no transmita ningún elemento.<br/> Si el tamaño de la matriz no está enlazado, no es legal: error del compilador MIDL.<br/>                                                              | Transmita el número de elementos indicados por la longitud.<br/> Tenga en cuenta que la longitud se puede cambiar y puede tener un valor diferente del valor en el cliente. No transmita la longitud.<br/>          |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Asigne espacio para el parámetro length en el servidor, pero no transmita el parámetro . Si el tamaño de la matriz es fijo, asigne el tamaño de la matriz en el servidor, pero no transmita ningún elemento.<br/> Si el tamaño de la matriz no es fijo, no es legal: error del compilador MIDL.<br/> | Transmita la longitud y el número de elementos indicados por la longitud establecida por la aplicación de servidor.                                                                                                             |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**en**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita el parámetro length. Si el tamaño de la matriz está enlazado, asigne el tamaño de la matriz en el servidor, pero no transmita ningún elemento.<br/> Si el tamaño de la matriz no está enlazado, no es legal: error del compilador MIDL.<br/>                                                           | Transmita la longitud. Transmita el número de elementos de matriz indicados por la longitud.<br/>                                                                                                                       |
| \[[**en**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**En**](/windows/desktop/Midl/in)\]                          | Transmita la longitud y el número de elementos indicados por el parámetro .                                                                                                                                                                                              | No transmita la longitud. Transmita el número de elementos indicados por la longitud.<br/> Tenga en cuenta que la longitud se puede cambiar y puede tener un valor diferente del valor original en el cliente.<br/> |
| \[[**en**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | No es legal; Error del compilador MIDL.                                                                                                                                                                                                                                         | No es legal; Error del compilador MIDL.                                                                                                                                                                                      |
| \[[**en**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**en**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita la longitud y el número de elementos indicados por el parámetro .                                                                                                                                                                                              | Transmita la longitud y el número de elementos indicados por el parámetro .                                                                                                                                           |



 

En general, no debe modificar los parámetros de longitud o tamaño en el lado servidor. Si cambia el parámetro length, puede huérfana de memoria. Para obtener más información, vea [Memoria huérfana.](memory-orphaning.md)

 

