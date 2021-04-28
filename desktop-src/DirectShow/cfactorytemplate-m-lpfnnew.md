---
description: 'CFactoryTemplate::m_lpfnNew miembro: puntero a una función que crea una instancia del objeto .'
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: CFactoryTemplate::m_lpfnNew miembro (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee4ec8e1503d3b260e025d154624b2d7c09bb49b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095653"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>CFactoryTemplate::m \_ lpfnNew member

Puntero a una función que crea una instancia del objeto .

## <a name="syntax"></a>Sintaxis


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Comentarios

En el archivo DLL, declare una función estática que devuelva un puntero a una nueva instancia del objeto . En la plantilla de generador, establezca la variable miembro **m \_ lpfnNew** en la dirección de esta función estática.

El tipo de puntero de función [**es LPFNNewCOMObject**](lpfnnewcomobject.md).

En el ejemplo siguiente se muestra una función típica **para m \_ lpfnNew**:


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




