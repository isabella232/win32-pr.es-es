---
description: Puntero a una función que crea una instancia del objeto.
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Miembro CFactoryTemplate:: m_lpfnNew (ComBase. h)'
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
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671149"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>Miembro lpfnNew CFactoryTemplate:: m \_

Puntero a una función que crea una instancia del objeto.

## <a name="syntax"></a>Sintaxis


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Observaciones

En el archivo DLL, declare una función estática que devuelva un puntero a una nueva instancia del objeto. En la plantilla de generador, establezca la variable de miembro **m \_ lpfnNew** en la dirección de esta función estática.

El tipo de puntero de función es [**LPFNNewCOMObject**](lpfnnewcomobject.md).

En el ejemplo siguiente se muestra una función típica para **m \_ lpfnNew**:


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
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




