---
description: El método Seek establece las posiciones de inicio y detención de la secuencia.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Método CPullPin. Seek (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671381"
---
# <a name="cpullpinseek-method"></a>CPullPin. Seek (método)

El `Seek` método establece las posiciones de inicio y detención de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStart* 
</dt> <dd>

Especifica la posición inicial, en bytes multiplicada por 10 millones.

</dd> <dt>

*tStop* 
</dt> <dd>

Especifica la posición de detención, en bytes multiplicada por 10 millones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el método se ejecuta correctamente, o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

Si el subproceso de trabajo se está ejecutando, el método pausa el subproceso, vacía el gráfico de filtro y reanuda el subproceso. El subproceso empieza a extraer los datos de la nueva posición inicial. De lo contrario, los nuevos valores de posición entrarán en vigor cada vez que se inicie el subproceso.

Las posiciones son relativas al inicio del origen original. Multiplique los desplazamientos de bytes deseados por las unidades constantes, que se define en la biblioteca de clases base como 10 millones.

Cuando el PIN se conecta por primera vez, las posiciones de detención e inicio tienen como valor predeterminado el principio y el final de la secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




