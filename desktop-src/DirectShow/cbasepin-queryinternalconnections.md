---
description: El método QueryInternalConnections recupera los pines que están conectados internamente a este pin (dentro del filtro). Este método implementa el método IPin::QueryInternalConnections.
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Método CBasePin.QueryInternalConnections (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 923081ed14b64b4e1c42b2b9e45f8733ad569c58face6dd7c1ea8dfec461eaa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001013"
---
# <a name="cbasepinqueryinternalconnections-method"></a>Método CBasePin.QueryInternalConnections

El `QueryInternalConnections` método recupera los pines que están conectados internamente a este pin (dentro del filtro). Este método implementa el [**método IPin::QueryInternalConnections.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*apPin* 
</dt> <dd>

Dirección de una matriz de [**punteros IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> <dt>

*nPin* 
</dt> <dd>

En la entrada, especifica el tamaño de la matriz. Cuando el método vuelve, el valor se establece en el número de punteros devueltos en la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Tamaño de matriz insuficiente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                 |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Error.<br/>                 |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Sin implementar.<br/>         |



 

## <a name="remarks"></a>Comentarios

En algunos filtros, los pines de entrada corresponden a pins de salida concretos. Para cada pin, este método rellena una matriz con punteros a los pines correspondientes. Si cada pin de entrada proporciona datos para cada pin de salida, devuelva E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




