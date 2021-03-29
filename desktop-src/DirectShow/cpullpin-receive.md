---
description: Se llama al método Receive cuando el objeto recibe un ejemplo multimedia del terminal de salida. La clase derivada debe implementar este método.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Método CPullPin. Receive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680831"
---
# <a name="cpullpinreceive-method"></a>CPullPin. Receive (método)

`Receive`Se llama al método cuando el objeto recibe un ejemplo multimedia del terminal de salida. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Si se devuelve un valor distinto de S \_ OK, se detendrá el subproceso de extracción de datos.

## <a name="remarks"></a>Observaciones

Se llama a este método siempre que llega un nuevo ejemplo del código PIN de salida. Escriba este método de la misma manera que el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

Las marcas de tiempo del ejemplo especifican los desplazamientos de bytes con respecto a la posición inicial original que se especificó en el método [**CPullPin:: Seek**](cpullpin-seek.md) .

La posición inicial se redondea hacia abajo hasta el límite de alineación más cercano y la posición de detención se redondea al límite de alineación más cercano. Además, si la posición de detención supera la duración total, se usa la duración en su lugar.

Todas las marcas de tiempo se proporcionan como un desplazamiento de bytes multiplicado por 10 millones, definidas como unidades de constantes. Por lo tanto, teóricamente un segundo es un byte. Para buscar los desplazamientos de bytes reales, llame a [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) y divida los resultados por unidades.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




