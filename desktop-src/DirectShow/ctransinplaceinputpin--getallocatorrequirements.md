---
description: 'El método GetAllocatorRequirements recupera las propiedades de asignador solicitadas por el código PIN. Este método implementa el método IMemInputPin:: GetAllocatorRequirements.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Método CTransInPlaceInputPin. GetAllocatorRequirements (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680739"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a>CTransInPlaceInputPin. GetAllocatorRequirements, método

El `GetAllocatorRequirements` método recupera las propiedades de asignador solicitadas por el código PIN. Este método implementa el método [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProps* 
</dt> <dd>

Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , que se rellena con los requisitos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto<br/>                                                                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | El PIN de salida no está conectado o el PIN de entrada de nivel inferior no admite el método.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo**<br/>                                                                 |



 

## <a name="remarks"></a>Observaciones

Si el PIN de salida está conectado, este método pasa la llamada al pin de entrada de nivel inferior. De lo contrario, devuelve E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




