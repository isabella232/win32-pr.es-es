---
description: El método Run ejecuta el filtro. Este método implementa el método IMediaFilter::Run.
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Método CBaseFilter.Run (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361402"
---
# <a name="cbasefilterrun-method"></a>Método CBaseFilter.Run

El `Run` método ejecuta el filtro. Este método implementa el [**método IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStart* 
</dt> <dd>

Tiempo de referencia correspondiente al tiempo de secuencia 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Si se detiene el filtro, este método pausa el filtro llamando al método [**CBaseFilter::P ause.**](cbasefilter-pause.md) A continuación, llama [**al método CBasePin::Run**](cbasepin-run.md) en cada uno de los pines conectados del filtro. Por último, establece la variable [**miembro de estado CBaseFilter::m \_**](cbasefilter-m-state.md) en State \_ Running.

El tiempo de secuencia se calcula como el tiempo de referencia actual menos *tStart*. Un ejemplo multimedia con una marca de tiempo de cero debe representarse en el *momento tStart*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




