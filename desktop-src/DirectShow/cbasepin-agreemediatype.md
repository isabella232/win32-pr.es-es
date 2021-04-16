---
description: El método AgreeMediaType busca un tipo de medio para crear una conexión de PIN.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Método CBasePin. AgreeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671641"
---
# <a name="cbasepinagreemediatype-method"></a>CBasePin. AgreeMediaType, método

El `AgreeMediaType` método busca un tipo de medio para crear una conexión de PIN.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN receptor.

</dd> <dt>

*p.p.* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica un tipo de medio, o **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto.<br/>                            |
| <dl> <dt>**VFW \_ E \_ no \_ hay \_ tipos aceptables**</dt> </dl> | No se encontró ningún tipo de medio aceptable.<br/> |



 

## <a name="remarks"></a>Observaciones

Si el parámetro *PMT* no es **null** y especifica totalmente un tipo de medio, este método intenta una conexión con ese tipo de medio. Si se produce un error en el intento, el método devuelve un error.

Si el parámetro *PMT* es **null** o especifica un tipo de medio parcial, este método probará los tipos de medios en el orden siguiente:

1.  Los tipos de medios preferidos del PIN receptor.
2.  Tipos de medios preferidos de este pin.

Los tipos de medios preferidos se enumeran con el método [**CBasePin:: EnumMediaTypes**](cbasepin-enummediatypes.md) y el enumerador resultante se pasa al método [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




