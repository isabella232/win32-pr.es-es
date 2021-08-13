---
description: 'Método CBaseOutputPin.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Método CBaseOutputPin.CheckConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca35cb98f279674285610fbd06b0399e93a68d59749fe4129475ab8bd970824a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658868"
---
# <a name="cbaseoutputpincheckconnect-method"></a>Método CBaseOutputPin.CheckConnect

El `CheckConnect` método determina si una conexión de pin es adecuada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                               | Descripción                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Correcto.<br/>                                                         |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>             | El pin de entrada no admite [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> |
| <dl> <dt>**VFW \_ E DIRECCIÓN NO \_ \_ VÁLIDA**</dt> </dl> | Las direcciones del pin no son compatibles.<br/>                               |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) de clase base y, a continuación, consulta el pin de entrada para su [**interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




