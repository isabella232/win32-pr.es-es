---
description: Se llama al método OnError si se produce un error durante el streaming. La clase derivada debe implementar este método.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Método CPullPin. OnError (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671382"
---
# <a name="cpullpinonerror-method"></a>CPullPin. OnError (método)

`OnError`Se llama al método si se produce un error durante el streaming. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*h* 
</dt> <dd>

Especifica el valor **HRESULT** devuelto por el método en el que se produjo el error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El objeto llama a este método siempre que se produce un error que detiene el subproceso de extracción de datos. El filtro puede utilizar este método para recuperar los errores de transmisión por secuencias correctamente. En la mayoría de los casos, el error se devuelve desde el filtro de nivel superior, por lo que el filtro de nivel superior es responsable de notificarlo al administrador de gráficos de filtro. Si el error se produce en el método [**CPullPin:: Receive**](cpullpin-receive.md) , el filtro debe enviar un evento [**\_ ERRORABORT de EC**](ec-errorabort.md) . (Vea [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




