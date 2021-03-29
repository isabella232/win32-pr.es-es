---
description: El método SetConfigInfo especifica el puntero IGraphConfig y el evento STOP.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Método CDynamicOutputPin. SetConfigInfo (Amfilter. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660509"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>CDynamicOutputPin. SetConfigInfo, método

El `SetConfigInfo` método especifica el puntero [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) y el evento STOP.

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

Puntero a la interfaz [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) o **null**.

</dd> <dt>

*hStopEvent* 
</dt> <dd>

Identificador de un evento que se señala cuando se detiene el filtro o **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro debe llamar a este método cuando se une al gráfico de filtro. El administrador de gráficos de filtros es compatible con **IGraphConfig**. Para el parámetro *hStopEvent* , cree un evento de restablecimiento manual. Cuando el filtro salga del gráfico de filtros, vuelva a llamar a este método con **null** para ambos parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




