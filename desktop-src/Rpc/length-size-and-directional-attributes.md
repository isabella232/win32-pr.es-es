---
title: Longitud, tamaño y atributos direccionales
description: Al pasar matrices entre el cliente y el servidor, los atributos relacionados con el tamaño \ Max \_ es \ y \ size \_ es \ determina cuántos elementos de matriz asigna el código auxiliar del servidor.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ffbf1ac75ad82a89e258ab595590fce2190b9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793131"
---
# <a name="length-size-and-directional-attributes"></a>Longitud, tamaño y atributos direccionales

Al pasar matrices entre el cliente y el servidor, los atributos relacionados con el tamaño \[ [**Max \_ es**](/windows/desktop/Midl/max-is) \] y \[ [**size \_**](/windows/desktop/Midl/size-is) \] determina cuántos elementos de matriz asigna el código auxiliar del servidor. La longitud de los atributos relacionados con la longitud \[ [**\_ es**](/windows/desktop/Midl/length-is) \] , el \[ [**primero \_ es**](/windows/desktop/Midl/first-is) \] y \[ el [**último \_**](/windows/desktop/Midl/last-is) determina el \] número de elementos que se transmiten al servidor y al cliente.

Se pueden aplicar atributos direccionales diferentes a los parámetros. Sin embargo, algunas combinaciones de atributos direccionales pueden producir errores. Por ejemplo, supongamos que está escribiendo una interfaz que especifica un procedimiento con dos parámetros, una matriz y la longitud transmitida de la matriz. El término *dir \_ ATTR* hace referencia al atributo direccional que se aplica al parámetro como:

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

En la tabla siguiente se describe el comportamiento del compilador de MIDL para cada combinación de atributos direccionales.



| Array                                          | Parámetro de longitud                               | Acciones de código auxiliar durante la llamada desde el cliente al servidor                                                                                                                                                                                                                          | Acciones de código auxiliar en la devolución del servidor al cliente                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**de**](/windows/desktop/Midl/in)\]                          | \[[**de**](/windows/desktop/Midl/in)\]                          | Transmita la longitud y el número de elementos indicados por el parámetro.                                                                                                                                                                                              | No se transmite ningún dato.                                                                                                                                                                                                 |
| \[[**de**](/windows/desktop/Midl/in)\]                          | \[[**enuncia**](/windows/desktop/Midl/out-idl)\]                    | No es legal; Error del compilador de MIDL.                                                                                                                                                                                                                                         | No es legal; Error del compilador de MIDL.                                                                                                                                                                                      |
| \[[**de**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita la longitud y el número de elementos indicados por el parámetro de longitud.                                                                                                                                                                                       | Transmita la longitud únicamente.                                                                                                                                                                                            |
| \[[**enuncia**](/windows/desktop/Midl/out-idl)\]                    | \[[**de**](/windows/desktop/Midl/in)\]                          | Transmita la longitud.<br/> Si el tamaño de la matriz es fijo, se asigna el tamaño de la matriz en el servidor, pero no se transmite ningún elemento.<br/> Si el tamaño de la matriz no está enlazado, no es válido: error del compilador de MIDL.<br/>                                                              | Transmita el número de elementos indicado por la longitud.<br/> Tenga en cuenta que la longitud se puede cambiar y puede tener un valor diferente del valor en el cliente. No transmita la longitud.<br/>          |
| \[[**enuncia**](/windows/desktop/Midl/out-idl)\]                    | \[[**enuncia**](/windows/desktop/Midl/out-idl)\]                    | Asigne espacio para el parámetro de longitud en el servidor pero no transmita el parámetro. Si el tamaño de la matriz es fijo, se asigna el tamaño de la matriz en el servidor, pero no se transmite ningún elemento.<br/> Si el tamaño de la matriz no es fijo, no es válido: error del compilador de MIDL.<br/> | Transmita la longitud y el número de elementos indicados por la longitud establecida por la aplicación de servidor.                                                                                                             |
| \[[**enuncia**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita el parámetro de longitud. Si el tamaño de la matriz está enlazado, se asigna el tamaño de la matriz en el servidor, pero no se transmite ningún elemento.<br/> Si el tamaño de la matriz no está enlazado, no es válido: error del compilador de MIDL.<br/>                                                           | Transmita la longitud. Transmita el número de elementos de matriz indicados por la longitud.<br/>                                                                                                                       |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**de**](/windows/desktop/Midl/in)\]                          | Transmita la longitud y el número de elementos indicados por el parámetro.                                                                                                                                                                                              | No transmita la longitud. Transmita el número de elementos indicado por la longitud.<br/> Tenga en cuenta que la longitud se puede cambiar y puede tener un valor distinto del valor original en el cliente.<br/> |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**enuncia**](/windows/desktop/Midl/out-idl)\]                    | No es legal; Error del compilador de MIDL.                                                                                                                                                                                                                                         | No es legal; Error del compilador de MIDL.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita la longitud y el número de elementos indicados por el parámetro.                                                                                                                                                                                              | Transmita la longitud y el número de elementos indicados por el parámetro.                                                                                                                                           |



 

En general, no debe modificar los parámetros de longitud o tamaño en el lado del servidor. Si cambia el parámetro de longitud, puede obtener una memoria huérfana. Para obtener más información, consulte [memoria huérfana](memory-orphaning.md).

 

