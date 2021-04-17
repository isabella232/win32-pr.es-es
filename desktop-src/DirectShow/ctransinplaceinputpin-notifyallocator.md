---
description: 'El método NotifyAllocator especifica un asignador para la conexión. Este método implementa el método IMemInputPin:: NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Método CTransInPlaceInputPin. NotifyAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74578243ce780e09d7435f9dd4b70bd9497e1e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660360"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a>CTransInPlaceInputPin. NotifyAllocator, método

El `NotifyAllocator` método especifica un asignador para la conexión. Este método implementa el método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Marca que especifica si los ejemplos de este asignador son de solo lectura. Si **es true**, los ejemplos son de solo lectura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto<br/>                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Error<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo**<br/> |



 

## <a name="remarks"></a>Observaciones

El filtro intenta usar el mismo asignador para ambas conexiones de PIN.

-   Si el PIN de salida no está conectado, el PIN de entrada acepta automáticamente el asignador. Cuando el PIN de salida está conectado, el filtro volverá a conectar el PIN de entrada. En ese momento, el filtro intentará volver a utilizar un único asignador.
-   Si el PIN de salida está conectado, el PIN de entrada acepta el asignador. El PIN de salida también usa el mismo asignador. Llama a `NotifyAllocator` en el PIN de entrada de nivel inferior.

El caso anterior tiene la siguiente excepción:

-   Si el asignador propuesto es de solo lectura (es decir, el parámetro *bReadOnly* es **true**) y el filtro necesita modificar los ejemplos, el filtro debe utilizar dos asignadores diferentes. En este caso, si el filtro de nivel superior propone usar el asignador del filtro de bajada, el método devuelve E \_ Fail.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




