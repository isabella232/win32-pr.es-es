---
description: El método Transform transforma un ejemplo en su lugar.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Método CTransInPlaceFilter. Transform (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681272"
---
# <a name="ctransinplacefiltertransform-method"></a>CTransInPlaceFilter. Transform (método)

El `Transform` método transforma un ejemplo en contexto.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | No entregue este ejemplo.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                    |



 

## <a name="remarks"></a>Observaciones

La clase derivada debe implementar este método. Transforme los datos de ejemplo en su lugar. Si el filtro usa dos asignadores, copia los datos del ejemplo de entrada a un nuevo ejemplo y pasa la copia a este método.

Si el filtro no debe proporcionar este ejemplo (por ejemplo, para admitir el control de calidad), el método debe devolver S \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




