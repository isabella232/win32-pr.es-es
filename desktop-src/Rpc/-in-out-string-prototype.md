---
title: " in, out, string Prototype"
description: El siguiente prototipo de función usa un único parámetro \ in, out, string\ para las cadenas de entrada y salida.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fe0b2e39f6f3bda532b030cac1ec4c15a03b7bb5447401e0f1f43ebda466ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024315"
---
# <a name="in-out-string-prototype"></a>\[in, out, string \] Prototype

El siguiente prototipo de función usa un único parámetro de cadena en \[ [](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)y para las cadenas de entrada [](/windows/desktop/Midl/string) \] y salida. La cadena contiene primero la entrada del paciente y, a continuación, se sobrescribe con la respuesta del médico como se muestra:

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

Este ejemplo es similar al que empleó una cadena de recuento único para la entrada y la salida. Al igual que con ese ejemplo, \[ [**el atributo size \_ is**](/windows/desktop/Midl/size-is) \] determina el número de elementos asignados en el servidor. El \[ [**atributo string**](/windows/desktop/Midl/string) \] dirige el código auxiliar a llamar a **strlen** para determinar el número de elementos transmitidos.

El cliente asigna toda la memoria antes de la llamada como:

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

Tenga en cuenta que la función Analyze ya no debe calcular la longitud de **\[ \]** la cadena devuelta como lo hizo en el ejemplo de cadena con recuento en el que no se usó el atributo de cadena. Ahora, los códigos auxiliares calculan la longitud como se muestra:

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 