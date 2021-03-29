---
title: " in, out, prototipo de cadena"
description: El prototipo de función siguiente usa un solo parámetro \ in, out, String \ para las cadenas de entrada y salida.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995360"
---
# <a name="in-out-string-prototype"></a>\[in, out, prototipo de cadena \]

El prototipo de función siguiente usa un único \[ [**parámetro in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), de [**cadena**](/windows/desktop/Midl/string) \] para las cadenas de entrada y salida. La cadena contiene primero la entrada del paciente y, a continuación, se sobrescribe con la respuesta del médico, como se muestra a continuación:

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

Este ejemplo es similar al que emplea una cadena de un solo recuento para la entrada y la salida. Como en este ejemplo, el \[ [**atributo \_ size**](/windows/desktop/Midl/size-is) \] determina el número de elementos asignados en el servidor. El \[ atributo de [**cadena**](/windows/desktop/Midl/string) \] indica al código auxiliar que llame a **strlen** para determinar el número de elementos transmitidos.

El cliente asigna toda la memoria antes de la llamada como:

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

Tenga en cuenta que la función Analyze ya no debe calcular la longitud de la cadena devuelta tal como lo hacía en el ejemplo de cadena recuento donde no se usó el atributo de **\[ cadena \]** . Ahora, el código auxiliar calcula la longitud como se muestra:

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 