---
title: Atributos direccionales (parámetro)
description: Los atributos direccionales describen si los datos se transmiten entre el cliente y el servidor, el servidor al cliente o ambos.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- RPC de llamada a procedimiento remoto, descripción, atributos direccionales
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149448"
---
# <a name="directional-parameter-attributes"></a>Atributos direccionales (parámetro)

Los atributos direccionales describen si los datos se transmiten entre el cliente y el servidor, el servidor al cliente o ambos. Todos los parámetros del prototipo de función deben estar asociados a atributos direccionales. Las tres combinaciones posibles de atributos direccionales son: 1) \[ [**in**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] y 3) \[ **in**, **out** \] . Estos describen la manera en que se pasan los parámetros entre los procedimientos de llamada y los que se llaman. Al compilar en el valor predeterminado (modo extendido de Microsoft) y omitir un atributo direccional para un parámetro, el compilador MIDL supone un valor predeterminado de \[ **en** \] .

Un \[ parámetro [**out**](/windows/desktop/Midl/out-idl) \] debe ser un puntero. De hecho, el \[  \] atributo out no es significativo cuando se aplica a parámetros que no actúan como punteros, ya que los parámetros de la función de C se pasan por valor. En C, la función a la que se llama recibe una copia privada del valor del parámetro. no puede cambiar el valor de la función de llamada para ese parámetro. Sin embargo, si el parámetro actúa como un puntero, se puede utilizar para tener acceso a la memoria y modificarla. El \[ atributo **out** \] indica que la función de servidor debe devolver el valor a la función de llamada del cliente y que se debe devolver la memoria asociada al puntero de acuerdo con los atributos asignados al puntero.

La interfaz siguiente muestra las tres combinaciones posibles de atributos direccionales que se pueden aplicar a un parámetro. La función **InOutProc** se define en el archivo IDL como:

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

El primer parámetro, *S1*, es \[ solo [**en**](/windows/desktop/Midl/in) \] . Su valor se transmite al equipo remoto, pero no se devuelve al procedimiento que realiza la llamada. Aunque la aplicación de servidor puede cambiar su valor para *S1*, el valor de *S1* en el cliente es el mismo antes y después de la llamada.

El segundo parámetro, *PS2*, se define en el prototipo de función como un puntero con \[ [](/windows/desktop/Midl/in) \] los atributos in y \[ [**out**](/windows/desktop/Midl/out-idl) \] . El \[ atributo **in** \] indica que el valor del parámetro se pasa desde el cliente al servidor. El \[ atributo **out** \] indica que el valor al que apunta *PS2* se devuelve al cliente.

El tercer parámetro es \[ solo [**out**](/windows/desktop/Midl/out-idl) \] . Se asigna espacio para el parámetro en el servidor, pero el valor no está definido en la entrada. Como se mencionó anteriormente, todos los \[ parámetros **out** \] deben ser punteros.

El procedimiento remoto cambia el valor de los tres parámetros, pero solo los nuevos valores de los \[ [](/windows/desktop/Midl/out-idl) \] parámetros out y \[ [**in**](/windows/desktop/Midl/in) \] están disponibles para el cliente.


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



En la devolución de la llamada a **InOutProc**, se modifican los parámetros segundo y tercero. El primer parámetro, que solo es \[ [**en**](/windows/desktop/Midl/in) \] , no cambia.

![in (parámetros)](images/prog-a22.png)

![out (parámetros)](images/prog-a23.png)

![parámetros de salida](images/prog-a21.png)

 

 