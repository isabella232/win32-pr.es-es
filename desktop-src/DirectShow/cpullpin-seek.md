---
description: El método Seek establece las posiciones de inicio y de detenerse de la secuencia.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Método CPullPin.Seek (Pullpin.h)
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
ms.openlocfilehash: 65ea4deddd000d1064adf8b8caf5a636eed87105856d506191d677e70978d096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953994"
---
# <a name="cpullpinseek-method"></a>Método CPullPin.Seek

El `Seek` método establece las posiciones de inicio y de detenerse de la secuencia.

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

Especifica la posición inicial, en bytes multiplicado por 10 000 000.

</dd> <dt>

*tStop* 
</dt> <dd>

Especifica la posición de detenerse, en bytes multiplicado por 10 000 000.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el método se realiza correctamente o un código de error en caso contrario.

## <a name="remarks"></a>Comentarios

Si el subproceso de trabajo se está ejecutando, el método pausa el subproceso, vacía el gráfico de filtro y reanuda el subproceso. El subproceso comienza a extraer datos de la nueva posición inicial. De lo contrario, los nuevos valores de posición se vuelven efectivos cada vez que se inicia el subproceso.

Las posiciones son relativas al inicio del origen original. Multiplique los desplazamientos de bytes deseados por la constante UNITS, que se define en la biblioteca de clases base como 10 000 000.

Cuando el pin se conecta por primera vez, las posiciones de detención e inicio tienen como valor predeterminado el principio y el final de la secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




