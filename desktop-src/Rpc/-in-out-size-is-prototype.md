---
title: " in, out, size_is Prototype"
description: '\in, out, size is\ prototype usa una matriz de caracteres de recuento único que se pasa de cliente a servidor y \_ de servidor a cliente.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361962"
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

Los códigos auxiliares usan el parámetro strsize de size para asignar memoria en el servidor y, a continuación, usan el parámetro \[ [**\_**](/windows/desktop/Midl/size-is) \] length  \[ [**\_ is**](/windows/desktop/Midl/length-is) \] *sizeSize* para transmitir los elementos de la matriz a esta memoria. El desarrollador debe asegurarse de que el código de cliente establece **\[ que la longitud \_ es \]** variable antes de llamar al procedimiento remoto.

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

En el ejemplo anterior, la matriz de caracteres achInOut también se usa como parámetro \[ [**out.**](/windows/desktop/Midl/out-idl) \] En C, el nombre de la matriz es equivalente al uso de un puntero. De forma predeterminada, todos los punteros de nivel superior son punteros de referencia: no cambian de valor y apuntan a la misma área de memoria en el cliente antes y después de la llamada. Toda la memoria a la que tiene acceso el procedimiento remoto debe ajustarse al tamaño especificado por el cliente antes de la llamada, o bien el código auxiliar generará una excepción.

Antes de volver, la función Analyze del servidor debe restablecer el *parámetrosize para* indicar el número de elementos que el servidor transmitirá al cliente como se muestra:

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 