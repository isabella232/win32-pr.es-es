---
description: 'El método GetPreroll recupera la cantidad de datos que se pondrán en cola antes de la posición de inicio. Este método implementa el método IMediaSeeking:: GetPreroll.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Método CPosPassThru. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680509"
---
# <a name="cpospassthrugetpreroll-method"></a>CPosPassThru. GetPreroll, método

El `GetPreroll` método recupera la cantidad de datos que se pondrán en cola antes de la posición de inicio. Este método implementa el método [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pllPreroll* 
</dt> <dd>

Puntero a una variable que recibe el tiempo de prelanzamiento, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor **HRESULT** del PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




