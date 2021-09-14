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
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062511"
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

## <a name="remarks"></a>Observaciones

El filtro debe llamar a este método cuando se une al gráfico de filtros. El administrador de gráficos de filtro **admite IGraphConfig.** Para el *parámetro hStopEvent,* cree un evento de restablecimiento manual. Cuando el filtro salga del gráfico de filtros, vuelva a llamar a este método **con NULL** para ambos parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




