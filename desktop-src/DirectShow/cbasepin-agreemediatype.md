---
description: El método AgreeMediaType busca un tipo de medio para realizar una conexión de pin.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Método CBasePin.AgreeMediaType (Amfilter.h)
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
ms.openlocfilehash: 60eff5a0654f991969f4d03cb6c8c975dfcc2d894b45fbb54f70bfea2870fadf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872535"
---
# <a name="cbasepinagreemediatype-method"></a>Método CBasePin.AgreeMediaType

El `AgreeMediaType` método busca un tipo de medio para realizar una conexión de pin.

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

Puntero a la interfaz IPin del [**pin receptor.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica un tipo de medio o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>                            |
| <dl> <dt>**VFW \_ E \_ NO \_ ACCEPTABLE \_ TYPES**</dt> </dl> | No se encontró ningún tipo de medio aceptable.<br/> |



 

## <a name="remarks"></a>Comentarios

Si el *parámetro pmt* no es **NULL** y especifica completamente un tipo de medio, este método intenta una conexión con ese tipo de medio. Si se produce un error en el intento, el método devuelve un error.

Si el *parámetro pmt* es **NULL** o especifica un tipo de medio parcial, este método intenta los tipos de medios en el orden siguiente:

1.  Tipos de medios preferidos del pin receptor.
2.  Tipos de medios preferidos de este pin.

Los tipos de medios preferidos se enumeran con el método [**CBasePin::EnumMediaTypes**](cbasepin-enummediatypes.md) y el enumerador resultante se pasa al método [**CBasePin::TryMediaTypes.**](cbasepin-trymediatypes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




