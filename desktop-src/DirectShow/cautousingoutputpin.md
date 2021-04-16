---
description: La clase CAutoUsingOutputPin obtiene y libera el acceso a un objeto CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Clase CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671479"
---
# <a name="cautousingoutputpin-class"></a>Clase CAutoUsingOutputPin

La clase **CAutoUsingOutputPin** obtiene y libera el acceso a un objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .

**CAutoUsingOutputPin** tiene estos tipos de miembros:



| Métodos públicos                                                           | Descripción                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)   | Método de constructor. Obtiene acceso al punto de conexión especificado. |
| [**~ CAutoUsingOutputPin**](cautousingoutputpin--cautousingoutputpin.md) | Método de destructor. Obtiene acceso al punto de conexión especificado.  |



 

## <a name="remarks"></a>Observaciones

Cuando se llama a determinados métodos en [**CDynamicOutputPin**](cdynamicoutputpin.md), el autor de la llamada debe obtener acceso al pin y, a continuación, liberar ese acceso. Para obtener acceso, el llamador usa el método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) . Para liberar el acceso, llama al método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) . La clase **CAutoUsingOutputPin** es una clase auxiliar que controla estas tareas en sus métodos de constructor y destructor. En el ejemplo de código siguiente se muestra cómo utilizar esta clase:


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de clase base](base-class-reference.md)
</dt> </dl>

 

 




