---
title: " in, out, size_is Prototype"
description: '\in, out, size is\ prototype usa una matriz de caracteres de recuento único que se pasa de cliente a servidor y de \_ servidor a cliente.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623dc39e9bd18fdd0c7bc02f008ccc1c16919362fd2a52e373abdde762eb726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073645"
---
# <a name="in-out-size_is-prototype"></a>\[in, out, size \_ is \] Prototype

El siguiente prototipo de función usa una matriz de caracteres de recuento único que se pasa de ambas maneras: de cliente a servidor y de servidor a cliente:

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

Como parámetro \[ [**in,**](/windows/desktop/Midl/in) \] *achInOut* debe apuntar al almacenamiento válido en el lado cliente. El desarrollador asigna memoria asociada a la matriz en el lado cliente antes de realizar la llamada a procedimiento remoto.

Los códigos auxiliares usan el parámetro strsize del parámetro para asignar memoria en el servidor y, a continuación, usan el parámetro length es el parámetro \[ [**\_**](/windows/desktop/Midl/size-is) \]  \[ [**\_**](/windows/desktop/Midl/length-is) \] *pwSize* para transmitir los elementos de la matriz a esta memoria. El desarrollador debe asegurarse de que el código de cliente establece que **\[ la longitud \_ es \]** variable antes de llamar al procedimiento remoto.

En algunas situaciones, el uso de parámetros independientes en lugar de una sola cadena para la entrada y salida es más eficaz y proporciona flexibilidad. Esto se muestra en el ejemplo siguiente:

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

En el ejemplo anterior, la matriz de caracteres achInOut también se usa como parámetro \[ [**out.**](/windows/desktop/Midl/out-idl) \] En C, el nombre de la matriz es equivalente al uso de un puntero. De forma predeterminada, todos los punteros de nivel superior son punteros de referencia: no cambian de valor y apuntan al mismo área de memoria en el cliente antes y después de la llamada. Toda la memoria a la que accede el procedimiento remoto debe ajustarse al tamaño especificado por el cliente antes de la llamada, o bien los códigos auxiliares generarán una excepción.

Antes de volver, la función Analyze en el servidor debe restablecer el *parámetrobizSize* para indicar el número de elementos que el servidor transmitirá al cliente como se muestra:

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 