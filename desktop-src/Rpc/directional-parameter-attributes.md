---
title: Atributos direccionales (parámetro)
description: Los atributos direccionales describen si los datos se transmiten de cliente a servidor, de servidor a cliente o de ambos.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Llamada a procedimiento remoto RPC, atributos descritos y direccionales
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e08e9ff23e7e12acbd5cf301afe6786599268d2e149878a326a62f79cd91f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930661"
---
# <a name="directional-parameter-attributes"></a>Atributos direccionales (parámetro)

Los atributos direccionales describen si los datos se transmiten de cliente a servidor, de servidor a cliente o de ambos. Todos los parámetros del prototipo de función deben estar asociados a atributos direccionales. Las tres combinaciones posibles de atributos direccionales son: 1) \[ [**en**](/windows/desktop/Midl/in) \] , 2) fuera y \[ [](/windows/desktop/Midl/out-idl) \] 3) \[ **en**, **out** \] . Estos describen la forma en que se pasan los parámetros entre los procedimientos de llamada y los procedimientos a los que se llama. Cuando se compila en el modo predeterminado (modo extendido de Microsoft) y se omite un atributo direccional para un parámetro, el compilador midL asume un valor predeterminado de \[ **en** \] .

Un \[ [**parámetro out**](/windows/desktop/Midl/out-idl) \] debe ser un puntero. De hecho, el atributo out no es significativo cuando se aplica a parámetros que no actúan como punteros porque los parámetros de función \[  \] de C se pasan por valor. En C, la función llamada recibe una copia privada del valor del parámetro; no puede cambiar el valor de la función de llamada para ese parámetro. Sin embargo, si el parámetro actúa como puntero, se puede usar para acceder a la memoria y modificarla. El atributo out indica que la función de servidor debe devolver el valor a la función de llamada del cliente y que la memoria asociada al puntero debe devolverse de acuerdo con los atributos \[  \] asignados al puntero.

En la interfaz siguiente se muestran las tres combinaciones posibles de atributos direccionales que se pueden aplicar a un parámetro. La función **InOutProc** se define en el archivo IDL como:

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

El primer parámetro, *s1*, solo \[ [**está en**](/windows/desktop/Midl/in) \] . Su valor se transmite al equipo remoto, pero no se devuelve al procedimiento de llamada. Aunque la aplicación de servidor puede cambiar su valor para *s1*, el valor de *s1* en el cliente es el mismo antes y después de la llamada.

El segundo parámetro, *ps2*, se define en el prototipo de función como un puntero con atributos \[ [**de entrada**](/windows/desktop/Midl/in) \] \[ [**y**](/windows/desktop/Midl/out-idl) \] salida. El atributo in indica que el valor del parámetro se pasa \[  \] desde el cliente al servidor. El \[ **atributo out** \] indica que el valor al que apunta *ps2* se devuelve al cliente.

El tercer parámetro es \[ [**solo out.**](/windows/desktop/Midl/out-idl) \] Se asigna espacio para el parámetro en el servidor, pero el valor no está definido en la entrada. Como se mencionó anteriormente, \[ **todos los** \] parámetros de salida deben ser punteros.

El procedimiento remoto cambia el valor de los tres parámetros, pero solo los nuevos valores de los parámetros out y \[ [](/windows/desktop/Midl/out-idl) \] \[ [**in**](/windows/desktop/Midl/in) \] están disponibles para el cliente.


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



Al devolver de la llamada a **InOutProc**, se modifican los parámetros segundo y tercero. El primer parámetro, que \[ [**solo está en**](/windows/desktop/Midl/in) , no se \] modifica.

![en parámetros](images/prog-a22.png)

![out (parámetros)](images/prog-a23.png)

![parámetros de entrada y salida](images/prog-a21.png)

 

 