---
description: 'Método CSource.FindPin: el método FindPin recupera el pin con el identificador especificado. Este método implementa el método IBaseFilter::FindPin.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Método CSource.FindPin (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daa1e2404e7c6fbf1d879d71374298103bdc621f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070042"
---
# <a name="csourcefindpin-method"></a>Método CSource.FindPin

El `FindPin` método recupera el pin con el identificador especificado. Este método implementa el método [**IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica el pin.

</dd> <dt>

*ppPin* 
</dt> <dd>

Recibe un puntero a la interfaz [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin. Si se produce un error en el \* *método, ppPin* se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>         | **Argumento de** puntero NULL.<br/>                 |
| <dl> <dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt> </dl> | No se encontró un pin con este identificador.<br/> |



 

## <a name="remarks"></a>Observaciones

El primer pin siempre se denomina "1"; el segundo pin se denomina "2"; etc. Para obtener más información, [**vea CSourceStream::QueryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSource (clase)**](csource.md)
</dt> </dl>

 

 




