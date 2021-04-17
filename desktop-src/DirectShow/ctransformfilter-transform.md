---
description: El método Transform transforma una muestra de entrada para generar un ejemplo de salida.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Método CTransformFilter. Transform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679361"
---
# <a name="ctransformfiltertransform-method"></a>CTransformFilter. Transform (método)

El `Transform` método transforma una muestra de entrada para generar un ejemplo de salida.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Agujas* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo de entrada.

</dd> <dt>

*pOut* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La clase base devuelve E \_ inesperada.

La clase derivada debe devolver un valor **HRESULT** , que indica que se ha realizado correctamente o se ha producido un error. Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | No entregue este ejemplo.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                    |



 

## <a name="remarks"></a>Observaciones

Invalide este método para generar datos de salida. Lea los datos de entrada del ejemplo especificado por el parámetro *pIn* y escriba los datos nuevos en el ejemplo especificado por el parámetro *pOut* .

Antes de que el filtro llame a este método, copia las propiedades de la muestra de entrada en el ejemplo de salida. El `Transform` método debe establecer las propiedades que difieren entre los dos ejemplos, mediante métodos **IMediaSample** o la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (si está disponible).

Si el filtro no debe proporcionar este ejemplo (por ejemplo, para admitir el control de calidad), el método debe devolver S \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




