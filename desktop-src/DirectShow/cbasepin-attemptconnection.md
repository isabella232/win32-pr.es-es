---
description: El método AttemptConnection se conecta a otro pin mediante un tipo de medio especificado.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Método CBasePin.AttemptConnection (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e70683d5307b81db14d23fec2c163b085cccaf64b7926eb41efdb5dfe9ac7611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872405"
---
# <a name="cbasepinattemptconnection-method"></a>Método CBasePin.AttemptConnection

El `AttemptConnection` método se conecta a otro pin mediante un tipo de medio especificado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz IPin del [**pin receptor.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                          |
| <dl> <dt>**TIPO E VFW \_ \_ NO \_ \_ ACEPTADO**</dt> </dl> | El tipo de medio no es aceptable.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método intenta conectar los dos pines con un tipo de medio específico. Si el tipo no es aceptable, se produce un error en el método sin probar otros tipos de medios.

Si el tipo de medio es aceptable, este método llama al método [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del pin receptor. A continuación, llama [**al método CBasePin::CompleteConnect**](cbasepin-completeconnect.md) para completar la conexión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




