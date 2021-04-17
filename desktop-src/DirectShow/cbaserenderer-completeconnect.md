---
description: El método CompleteConnect completa la conexión del PIN de entrada con otro PIN.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Método CBaseRenderer. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660757"
---
# <a name="cbaserenderercompleteconnect-method"></a>CBaseRenderer. CompleteConnect, método

El `CompleteConnect` método completa la conexión del PIN de entrada con otro PIN.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del terminal de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El PIN de entrada del filtro llama a este método desde dentro de su propio `CompleteConnect` método, al que se llama para completar una conexión del PIN. (Para obtener más información, vea [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md)). El filtro llama al método [**CBaseRenderer:: SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) para habilitar los eventos de [**\_ Repaint de EC**](ec-repaint.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




