---
title: " in, size_is out, size_is Prototype"
description: El siguiente prototipo de función usa dos cadenas con recuento. El desarrollador debe escribir código en el cliente y el servidor para realizar un seguimiento de las longitudes de la matriz de caracteres y pasar parámetros que le digan a los códigos auxiliares cuántos elementos de matriz transmitir.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259879"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[in, size \_ is \] and \[ out, size is \_ \] Prototype

El siguiente prototipo de función usa dos cadenas con recuento. El desarrollador debe escribir código en el cliente y el servidor para realizar un seguimiento de las longitudes de la matriz de caracteres y pasar parámetros que le digan a los códigos auxiliares cuántos elementos de matriz transmitir.

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

Tenga en cuenta que los parámetros que describen la longitud de la matriz se transmiten en la misma dirección que las matrices: *cbIn* y *achIn* están en parámetros, mientras que los parámetros \[ [](/windows/desktop/Midl/in) \] de out y *achOut* son parámetros  \[ [](/windows/desktop/Midl/out-idl) \] out. Como parámetro **\[ out, \]** el parámetro *fueloout* debe seguir la convención de C y declararse como puntero.

El código de cliente cuenta el número de caracteres de la cadena, incluido el cero final, antes de llamar al procedimiento remoto como se muestra:

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

El procedimiento remoto en el servidor proporciona la longitud del búfer devuelto en *cbOut como* se muestra:

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

El atributo de cadena se puede utilizar cuando se sabe que un parámetro \[  \] es una cadena. Este atributo dirige el código auxiliar para calcular el tamaño de la cadena, lo que elimina la sobrecarga asociada a la \[ [**longitud de los**](/windows/desktop/Midl/size-is) parámetros \] . Además, dirigirá el código auxiliar para comprobar que la cadena termina en **NULL** antes de pasar el parámetro a la aplicación.

 

 