---
title: " in, out, size_is prototipo"
description: '\ in, out, size \_ es \ prototype usa una matriz de caracteres de un solo recuento que se pasa desde el cliente al servidor y desde el servidor al cliente.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359053"
---
# <a name="in-out-size_is-prototype"></a>\[in, out, el tamaño \_ es \] prototype

El prototipo de función siguiente usa una matriz de caracteres de un solo recuento que se pasa de ambas maneras: de cliente a servidor y de servidor a cliente:

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

Como parámetro \[ [**in**](/windows/desktop/Midl/in) \] , *achInOut* debe apuntar a un almacenamiento válido en el lado cliente. El desarrollador asigna la memoria asociada a la matriz en el lado cliente antes de efectuar la llamada a procedimiento remoto.

El código auxiliar usa el \[ parámetro [**size \_**](/windows/desktop/Midl/size-is) \] *strsize* para asignar memoria en el servidor y, a continuación, usar la \[ [**longitud \_ es**](/windows/desktop/Midl/length-is) el \] parámetro *PCB* para transmitir los elementos de la matriz a esta memoria. El desarrollador debe asegurarse de que el código de cliente establece la **\[ longitud \_ \]** de la variable antes de llamar al procedimiento remoto.

En algunas situaciones, el uso de parámetros independientes en lugar de una sola cadena para la entrada y la salida es más eficaz y proporciona flexibilidad. Esto se muestra en el ejemplo siguiente:

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

En el ejemplo anterior, la matriz de caracteres achInOut también se utiliza como \[ parámetro [**out**](/windows/desktop/Midl/out-idl) \] . En C, el nombre de la matriz es equivalente al uso de un puntero. De forma predeterminada, todos los punteros de nivel superior son punteros de referencia; no cambian de valor y apuntan a la misma área de memoria en el cliente antes y después de la llamada. Toda la memoria a la que el procedimiento remoto tiene acceso debe ajustarse al tamaño que el cliente especifica antes de la llamada, o el código auxiliar generará una excepción.

Antes de volver, la función Analyze en el servidor debe restablecer el parámetro *PCB* para indicar el número de elementos que el servidor transmitirá al cliente, como se muestra a continuación:

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 