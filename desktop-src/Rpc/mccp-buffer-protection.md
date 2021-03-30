---
title: Protección de búfer de MCCP
description: A partir de Windows Vista, el motor de serialización de RPC realiza pasos adicionales para intentar evitar las saturaciones del búfer del lado cliente debido a los datos devueltos. Esta característica se denomina protección de conformidad mínima (MCCP).
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d04de57974bd9665d659129590d72513eb83e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793498"
---
# <a name="mccp-buffer-protection"></a>Protección de búfer de MCCP

A partir de Windows Vista, el motor de serialización de RPC realiza pasos adicionales para intentar evitar las saturaciones del búfer del lado cliente debido a los datos devueltos. Esta característica se denomina protección de conformidad mínima (MCCP).

Cuando el cliente pasa un puntero a un búfer existente a un \[ [](/windows/desktop/Midl/out-idl) \] parámetro out o \[ [**in**](/windows/desktop/Midl/in),**out** \] , los datos devueltos para ese parámetro se copian en el búfer existente. Si los datos devueltos son mayores que el búfer pasado, se puede producir una saturación del búfer cuando RPC copia los datos devueltos en el búfer demasiado pequeño. Vea [punteros de nivel superior e incrustados](top-level-and-embedded-pointers.md).

Con MCCP, RPC intenta detectar esta condición y rechazar la llamada si se detecta. En el caso de los búferes con un valor de correlación, como el \[ [**tamaño \_ es**](/windows/desktop/Midl/size-is) \] , si los datos devueltos no caben en el tamaño de búfer especificado, se rechaza la llamada y \_ \_ \_ se genera una excepción de datos de código auxiliar erróneo de RPC X \_ . En el caso de las cadenas no de tamaño, se rechaza la llamada si el tamaño de cadena existente (longitud hasta el terminador **nulo** ) no es suficiente para contener la cadena devuelta, se rechaza la llamada. RPC no puede detectar saturaciones del búfer en todas las condiciones, por lo que se recomienda que el desarrollador siga tomando precauciones normales contra las saturaciones del búfer.

Si el cliente no pasa un búfer existente para un parámetro \[ [**out**](/windows/desktop/Midl/out-idl) \] , sino que, en su lugar, pasa un puntero desreferenciado a **null**, RPC seguirá las reglas normales para asignar un nuevo búfer en nombre del cliente. Este búfer se asignará con espacio suficiente para contener los datos devueltos.

Una segunda protección es que, para los parámetros correlacionados, RPC exigirá que se pase un búfer que no sea **null** cuando la variable de recuento de correlaciones no sea **null**.

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

Si el valor de la *cadena* es **null**, RPC rechazará la llamada a menos que la *longitud* esté establecida en 0. Tenga en cuenta que RPC permitirá que la *longitud* sea 0, mientras que el valor de la *cadena* no es **null**, y RPC tratará la *cadena* como una asignación de búfer de longitud 0.

 

 