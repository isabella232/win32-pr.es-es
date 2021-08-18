---
title: Protección del búfer MCCP
description: A partir de Windows Vista, el motor de marshalling rpc realiza pasos adicionales para intentar evitar saturaciones del búfer del lado cliente debido a los datos devueltos. Esta instalación se denomina Mini Compute Conformance Protection (MCCP).
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b95234eed76c3d8f0fdc34b0b53e9cf02bcae2fd6db62694e1a3aadd602076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928411"
---
# <a name="mccp-buffer-protection"></a>Protección del búfer MCCP

A partir de Windows Vista, el motor de marshalling rpc realiza pasos adicionales para intentar evitar saturaciones del búfer del lado cliente debido a los datos devueltos. Esta instalación se denomina Mini Compute Conformance Protection (MCCP).

Cuando el cliente pasa un puntero a un búfer existente a un parámetro out o en , los datos devueltos para ese parámetro se \[ [](/windows/desktop/Midl/out-idl) \] \[ [](/windows/desktop/Midl/in) \] copian en el búfer existente. Si los datos devueltos son mayores que el búfer pasado, puede producirse una saturación del búfer cuando RPC copia los datos devueltos en el búfer demasiado pequeño. Vea [Punteros de nivel superior e incrustados.](top-level-and-embedded-pointers.md)

Con MCCP, RPC intenta detectar esta condición y rechazar la llamada si se detecta. Para los búferes con un valor de correlación, como el tamaño es , si los datos devueltos no caben en el tamaño de búfer especificado, se rechaza la llamada y se genera la excepción RPC X BAD \[ [**\_**](/windows/desktop/Midl/size-is) \] STUB \_ \_ \_ \_ DATA. En el caso de las cadenas sin usar, la llamada  se rechaza si el tamaño de cadena existente (longitud hasta el terminador nulo) no es suficiente para contener la cadena devuelta, se rechaza la llamada. RPC no puede detectar saturaciones de búfer en todas las condiciones, por lo que se recomienda al desarrollador que siga tomando precauciones normales frente a saturaciones del búfer.

Si el cliente no pasa un búfer existente para un parámetro out, sino que pasa un puntero desreferenciado \[ [](/windows/desktop/Midl/out-idl) \] a **NULL,** RPC seguirá las reglas normales para asignar un nuevo búfer en nombre del cliente. Este búfer se asignará con espacio suficiente para contener los datos devueltos.

Una segunda protección es que para los parámetros correlacionados, RPC exigirá que se pase un búfer que no sea NULL cuando la variable de recuento de correlación no sea **null.**

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

Si *MyString* es **NULL,** RPC rechazará la llamada a menos *que Length* esté establecido en 0. Tenga en cuenta que RPC permitirá *que Length* sea 0 mientras *MyString* no sea **NULL** y RPC tratará *MyString* como una asignación de búfer de 0 longitud.

 

 