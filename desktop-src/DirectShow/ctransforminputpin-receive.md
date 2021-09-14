---
description: 'Método CTransformInputPin.Receive: el método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el método IMemInputPin::Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Método CTransformInputPin.Receive (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a6a3c5dd4c9f11d45e1b719498d515a536e5ef8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255429"
---
# <a name="ctransforminputpinreceive-method"></a>Método CTransformInputPin.Receive

El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el [**método IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El pin se está vacíando actualmente; se rechazó el ejemplo.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) del pin, que comprueba el estado de streaming del pin y comprueba si hay cambios de formato en el tipo de medio. A continuación, llama al método [**CTransformFilter::Receive**](ctransformfilter-receive.md) del filtro, que procesa el ejemplo y lo entrega de nivel inferior.

Si el filtro necesita tener acceso al ejemplo después de que este método vuelva, debe contener un recuento de referencias llamando al método **IUnknown::AddRef** en el ejemplo. Por ejemplo, algunos filtros de descodificador necesitan el ejemplo actual para descodificar el ejemplo siguiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




