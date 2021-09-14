---
description: Se llama al método Receive cuando el objeto recibe un ejemplo multimedia del pin de salida. La clase derivada debe implementar este método.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Método CPullPin.Receive (Pullpin.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063298"
---
# <a name="cpullpinreceive-method"></a>Método CPullPin.Receive

Se `Receive` llama al método cuando el objeto recibe un ejemplo multimedia del pin de salida. La clase derivada debe implementar este método.

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

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Si se devuelve un valor distinto de S \_ OK, se detendrá el subproceso de extracción de datos.

## <a name="remarks"></a>Observaciones

Se llama a este método cada vez que llega un nuevo ejemplo desde el pin de salida. Escriba este método de la misma manera que el [**método IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

Las marcas de tiempo del ejemplo especifican los desplazamientos de bytes, en relación con la posición inicial original que se especificó en el método [**CPullPin::Seek.**](cpullpin-seek.md)

La posición inicial se redondea hacia abajo hasta el límite de alineación más cercano y la posición de detenerse se redondea al límite de alineación más cercano. Además, si la posición de detenerse supera la duración total, se usa la duración en su lugar.

Todas las marcas de tiempo se dan como un desplazamiento de bytes multiplicado por 10 000 000, definido como la constante UNITS. Por lo tanto, no obstante, un segundo es un byte. Para buscar los desplazamientos de bytes reales, llame [**a IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) y divida los resultados por UNITS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




