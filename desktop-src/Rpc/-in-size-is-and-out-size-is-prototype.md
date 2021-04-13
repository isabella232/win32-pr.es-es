---
title: " en, size_is y out, size_is prototipo"
description: El prototipo de función siguiente usa dos cadenas contadas. El desarrollador debe escribir código en el cliente y en el servidor para realizar un seguimiento de las longitudes de la matriz de caracteres y pasar parámetros que indiquen el número de elementos de la matriz que se van a transmitir.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421293"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[en, el tamaño \_ es \] y \[ fuera, el tamaño \_ es \] prototipo

El prototipo de función siguiente usa dos cadenas contadas. El desarrollador debe escribir código en el cliente y en el servidor para realizar un seguimiento de las longitudes de la matriz de caracteres y pasar parámetros que indiquen el número de elementos de la matriz que se van a transmitir.

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

Tenga en cuenta que los parámetros que describen la longitud de la matriz se transmiten en la misma dirección que las matrices: *cbIn* y *achIn* están \[ [**en**](/windows/desktop/Midl/in) \] parámetros mientras que *pcbOut* y *achOut* son parámetros de \[ [**salida**](/windows/desktop/Midl/out-idl) \] . Como parámetro **\[ out \]** , el parámetro *pcbOut* debe seguir la Convención de C y declararse como un puntero.

El código de cliente cuenta el número de caracteres de la cadena, incluido el cero final, antes de llamar al procedimiento remoto, como se muestra a continuación:

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

El procedimiento remoto en el servidor proporciona la longitud del búfer de retorno en *cbOut* , como se muestra a continuación:

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

El \[ atributo de **cadena** \] se puede usar cuando se sabe que un parámetro es una cadena. Este atributo dirige el código auxiliar para calcular el tamaño de la cadena, lo que elimina la sobrecarga asociada con la longitud de los \[ [](/windows/desktop/Midl/size-is) \] parámetros. Además, dirigirá el código auxiliar para comprobar que la cadena está terminada en **null** antes de pasar el parámetro a la aplicación.

 

 