---
description: El método SetConfigInfo especifica el puntero IGraphConfig y el evento stop.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Método CDynamicOutputPin.SetConfigInfo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23b492eaf4b5f712a51132eefcceac12a772b17b8285d8c6edb1a6cec268b1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074239"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>Método CDynamicOutputPin.SetConfigInfo

El `SetConfigInfo` método especifica el puntero [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) y el evento stop.

## <a name="syntax"></a>Sintaxis


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGraphConfig* 
</dt> <dd>

Puntero a la [**interfaz IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) o **NULL.**

</dd> <dt>

*hStopEvent* 
</dt> <dd>

Controlar a un evento que se señala cuando se detiene el filtro, o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El filtro debe llamar a este método cuando se une al gráfico de filtros. El administrador de gráficos de filtro **admite IGraphConfig.** Para el *parámetro hStopEvent,* cree un evento de restablecimiento manual. Cuando el filtro salga del gráfico de filtros, vuelva a llamar a este método **con NULL** para ambos parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




